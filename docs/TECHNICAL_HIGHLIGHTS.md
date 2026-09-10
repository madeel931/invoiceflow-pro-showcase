# InvoiceFlow Pro — Technical Highlights

This document highlights the key engineering decisions, patterns, and technical mechanisms implemented in InvoiceFlow Pro.

---

## 1. Deterministic Financial Arithmetic & Precision

Client-side financial systems are vulnerable to subtle floating-point inaccuracies when calculating tax rates, multi-item subtotals, and currency conversions.

### Implementation:
* **Strict Calculation Order:** Taxes and discounts are evaluated on individual line items before summing, reducing discrepancies between line-item inspection and invoice summary cards.
* **Controlled Rounding Boundaries:** Monetary calculations are rounded consistently at defined domain/persistence boundaries to reduce cumulative rounding discrepancies over extended multi-invoice statements.
* **Overpayment Guards:** Business rules enforce non-negative balances and prevent recorded payments from exceeding remaining debt without explicit user confirmation.

---

## 2. High-Performance Local-First Persistence (Isar)

Rather than using basic SQLite wrappers or key-value stores, InvoiceFlow Pro leverages **Isar**, an embedded database compiled to native C++ binaries.

### Key Advantages:
* **Indexed Local Queries:** Efficient filtering across historical invoices by status or date range.
* **Reactive Database Streams:** Views subscribe directly to Isar queries (`watchLazy`), reducing manual cache synchronization between screens.
* **Transactional Writes:** Invoice creations, item edits, and related ledger updates execute inside transactions where required, safeguarding database integrity.

---

## 3. On-Device Vector PDF Compilation with QR Generation

Generating professional PDF documents directly on a mobile device without relying on server-side rendering engines reduces operational dependencies and keeps document generation local.

### Pipeline:
1. **Domain Model Extraction:** Raw invoice domain entities and business branding settings are passed to the document builder.
2. **Dynamic Multi-Page Flow:** The layout engine dynamically measures item rows and computes page breaks to prevent orphaned elements and overlapping headers/footers.
3. **QR Code Integration:** Includes QR code generation for payment or invoice-related information.
4. **Platform Print/Share Spooling:** Integrates directly with native mobile share sheets (`share_plus`) and system print dialogs (`printing`).

---

## 4. Complex Bidirectional Typography (Arabic, Urdu, English)

Supporting both Left-to-Right (LTR) and Right-to-Left (RTL) scripts in mobile applications presents non-trivial challenges—particularly in custom PDF canvases where system-level font shaping is not automatically applied.

### Engineering Solution:
* **Contextual Glyphs & Reshaping:** Arabic and Urdu strings undergo glyph reshaping (`arabic_reshaper`) to join isolated characters into contextually correct cursive script forms.
* **Unicode Bidirectional Algorithm:** A bidirectional analysis step (`bidi`) handles mixed-script strings (e.g., English product codes embedded inside Arabic item descriptions) ensuring correct logical-to-visual character ordering.
* **Embedded Font Assets:** Explicit bundling of `NotoSansArabic` (Regular and Bold) ensures consistent typographic rendering across supported runtimes.

---

## 5. Dual-Layer Backup Engine with Integrity Verification

Data durability is critical in an offline-first application where no remote server maintains automatic duplicates.

### Architecture:
1. **Google Drive Cloud Sync:**
   * Uses official Google OAuth APIs to synchronize database backup archives directly to the user's private Google Drive `appDataFolder`.
   * Completely isolated from the user's regular Google Drive files.
2. **Local Archive Export/Import:**
   * Users can generate standalone backup archives for local storage or device migration.
3. **SHA-256 Checksum Verification:**
   * Every backup archive generates a cryptographic SHA-256 digest at creation.
   * During restore operations, the engine recalculates the digest and validates it before touching live database tables, helping prevent corrupt or truncated files from entering active database storage.

> **Integrity note:** SHA-256 provides integrity verification; it is not encryption. Backup archives should not be described as encrypted unless encryption is separately implemented.

---

## 6. Functional Error Handling with `dartz`

To keep error handling explicit and reduce exception handling in presentation layers:

* **Pure Domain Results:** Use cases return an `Either<Failure, T>` type where applicable.
* **Explicit Failure Mapping:** Data source exceptions are handled at repository boundaries and mapped to strongly typed domain failures.
* **Declarative Presentation Handling:** Cubits fold over the result:
  ```dart
  final result = await saveInvoiceUseCase(invoice);
  result.fold(
    (failure) => emit(InvoiceErrorState(failure.message)),
    (savedInvoice) => emit(InvoiceSavedSuccessState(savedInvoice)),
  );
  ```

---

## 7. Decoupled Service Architecture & Testability

Major subsystems—including notifications, billing/licensing, PDF generation, and persistence—are designed behind clean interface abstractions where appropriate.

* **Layer Separation:** Presentation widgets interact with Cubits; Cubits coordinate Use Cases; Use Cases depend on repository contracts rather than concrete storage implementations.
* **Test Isolation:** Services such as Google Sign-In and local notifications can be substituted with test doubles where interfaces permit.
