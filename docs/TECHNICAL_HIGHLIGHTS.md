# InvoiceFlow Pro — Technical Highlights

This document highlights the key engineering decisions, patterns, and technical mechanisms implemented in InvoiceFlow Pro.

---

## 1. Deterministic Financial Arithmetic & Precision

Client-side financial systems are vulnerable to subtle floating-point inaccuracies when calculating tax rates, multi-item subtotals, and currency conversions.

### Implementation:
* **Strict Calculation Order:** Taxes and discounts are evaluated on individual line items before summing, eliminating discrepancies between line-item inspection and invoice summary cards.
* **Controlled Rounding Boundaries:** All monetary values maintain standard 2-decimal-place precision using fixed-point representation at persistence boundaries, preventing cumulative cent drift over extended multi-invoice statements.
* **Overpayment Guards:** Business rules enforce non-negative balances and prevent recorded payments from exceeding remaining debt without explicit user confirmation.

---

## 2. High-Performance Local-First Persistence (Isar)

Rather than using basic SQLite wrappers or key-value stores, InvoiceFlow Pro leverages **Isar**, an embedded database compiled to native C++ binaries.

### Key Advantages:
* **Indexed Local Queries:** Efficient filtering across historical invoices by status or date range.
* **Reactive Database Streams:** Views subscribe directly to Isar queries (`watchLazy`), eliminating manual cache synchronization or state-stretching bugs between screens.
* **Transactional Writes:** All invoice creations, item edits, and ledger updates execute inside transactions, safeguarding database integrity.

---

## 3. On-Device Vector PDF Compilation with QR Generation

Generating professional PDF documents directly on a mobile device without relying on server-side rendering engines (e.g., Puppeteer, Chromium, or remote microservices) significantly reduces operational cost and respects user privacy.

### Pipeline:
1. **Domain Model Extraction:** Raw invoice domain entities and business branding settings are passed to the document builder.
2. **Dynamic Multi-Page Flow:** The layout engine dynamically measures item rows and automatically computes page breaks to prevent orphans and overlapping headers/footers.
3. **QR Code Integration:** Includes QR code generation for payment or invoice-related information.
4. **Platform Print/Share Spooling:** Integrates directly with native mobile share sheets (`share_plus`) and system print dialogs (`printing`).

---

## 4. Complex Bidirectional Typography (Arabic, Urdu, English)

Supporting both Left-to-Right (LTR) and Right-to-Left (RTL) scripts in mobile applications presents non-trivial challenges—particularly in custom PDF canvases where system-level font shaping is not automatically applied.

### Engineering Solution:
* **Contextual Glyphs & Reshaping:** Arabic and Urdu strings undergo glyph reshaping (`arabic_reshaper`) to join isolated characters into contextually correct cursive script forms.
* **Unicode Bidirectional Algorithm:** A bidirectional analysis step (`bidi`) handles mixed-script strings (e.g., English product codes embedded inside Arabic item descriptions) ensuring correct logical-to-visual character ordering.
* **Embedded Font Assets:** Explicit bundling of `NotoSansArabic` (Regular and Bold) ensures consistent typographic rendering across Android, iOS, and desktop preview runtimes.

---

## 5. Dual-Layer Backup Engine with Cryptographic Verification

Data durability is critical in an offline-first application where no remote server maintains automatic duplicates.

### Architecture:
1. **Google Drive Cloud Sync:**
   * Uses official Google OAuth APIs to silently synchronize encrypted/compressed database archives directly to the user's private Google Drive `appDataFolder`.
   * Completely isolated from the user's regular Google Drive files to prevent accidental deletion.
2. **Local Archive Export/Import:**
   * Users can generate standalone backup archives for local storage or device migration.
3. **SHA-256 Checksum Verification:**
   * Every backup archive generates a cryptographic SHA-256 digest at creation.
   * During restore operations, the engine recalculates the digest and validates it before touching live database tables, preventing corrupt or truncated files from entering active database storage.

---

## 6. Functional Error Handling with `dartz`

To avoid unhandled exceptions crashing the user interface or polluting presentation layers with try-catch blocks:

* **Pure Domain Results:** All use cases return an `Either<Failure, T>` type.
* **Explicit Failure Mapping:** Data source exceptions (e.g., `IsarError`, `PlatformException`, `SocketException`) are caught at the repository boundary and mapped to strongly-typed domain failures (`DatabaseFailure`, `NetworkFailure`, `AuthenticationFailure`).
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

Every major system subsystem—including notifications, billing/licensing, PDF generation, and persistence—is designed behind clean interface abstractions:

* **Zero Hardware Coupling:** Presentation widgets interact solely with Cubits; Cubits interact solely with Use Cases; Use Cases interact solely with Repository Interfaces.
* **Test Isolation:** Any service (such as Google Sign-In or local push notifications) can be cleanly swapped with lightweight test mocks or fakes without touching application code.
