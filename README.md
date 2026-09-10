<div align="center">

  <img src="https://cdn.jsdelivr.net/gh/madeel931/invoiceflow-pro-showcase@main/assets/app_icon.png" width="96" height="96" alt="InvoiceFlow Pro Logo" style="border-radius: 20px;" />

  # InvoiceFlow Pro

  **Offline-first Flutter invoicing application built with Clean Architecture, Cubit state management, Isar persistence, PDF generation, RTL localization, financial analytics, and backup workflows.**

  [![Flutter](https://img.shields.io/badge/Flutter-3.x-02569B?style=flat-square&logo=flutter&logoColor=white)](https://flutter.dev)
  [![Dart](https://img.shields.io/badge/Dart-3.5%2B-0175C2?style=flat-square&logo=dart&logoColor=white)](https://dart.dev)
  [![State Management](https://img.shields.io/badge/BLoC%20%2F%20Cubit-8.1-blueviolet?style=flat-square)](https://bloclibrary.dev)
  [![Architecture](https://img.shields.io/badge/Architecture-Clean%20Architecture-2563EB?style=flat-square)](docs/ARCHITECTURE.md)
  [![Database](https://img.shields.io/badge/Database-Isar-50C878?style=flat-square)](https://isar.dev)
  [![PDF Engine](https://img.shields.io/badge/PDF-Vector%20Generation-red?style=flat-square)](docs/TECHNICAL_HIGHLIGHTS.md)
  [![RTL Support](https://img.shields.io/badge/RTL-Arabic%20%7C%20Urdu-teal?style=flat-square)](docs/TECHNICAL_HIGHLIGHTS.md)
  [![Testing](https://img.shields.io/badge/Automated%20Testing-Unit%2C%20Widget%20%26%20Regression-brightgreen?style=flat-square)](docs/TESTING.md)

</div>

---

## 📲 Try InvoiceFlow Pro

<p align="center">

<a href="https://github.com/madeel931/invoiceflow-pro-showcase/releases/download/demo-v1.0.1/InvoiceFlow-Pro-Demo-v1.0.1-arm64.apk">
  <img src="https://img.shields.io/badge/Download%20Android%20Demo-APK-0F172A?style=for-the-badge&logo=android&logoColor=white" alt="Download Android Demo APK">
</a>

</p>

<p align="center">
  <strong>Try the real app before purchasing the source code.</strong><br>
  Offline-first invoicing • PDF invoices • Arabic & Urdu RTL • Backup • Reports
</p>

<p align="center">
  <a href="https://github.com/madeel931/invoiceflow-pro-showcase/releases/tag/demo-v1.0.0">
    View Demo Release →
  </a>
</p>

> **Demo:** The Android demo uses the Free plan with a limit of **25 lifetime invoices**.

---

InvoiceFlow Pro is a commercial invoicing application designed for independent service businesses and contractors. This public repository serves as a **technical showcase and engineering case study**; the complete commercial source code is intentionally not included.

> **Technical Objective:** Designed to demonstrate production-oriented Flutter architecture, offline data management, financial workflows, document generation, and localization.

---

## 📱 Application Overview

<table>
  <tr>
    <td align="center" width="25%">
      <img src="https://cdn.jsdelivr.net/gh/madeel931/invoiceflow-pro-showcase@main/screenshots/01_dashboard_overview.png" alt="Executive Dashboard" width="100%" />
      <br /><strong>Dashboard</strong>
      <br /><sub>Financial overview, status counts, and KPIs</sub>
    </td>
    <td align="center" width="25%">
      <img src="https://cdn.jsdelivr.net/gh/madeel931/invoiceflow-pro-showcase@main/screenshots/02_create_invoice_flow.png" alt="Invoice Creation" width="100%" />
      <br /><strong>Invoice Creation</strong>
      <br /><sub>Structured customer, item, tax, and discount flow</sub>
    </td>
    <td align="center" width="25%">
      <img src="https://cdn.jsdelivr.net/gh/madeel931/invoiceflow-pro-showcase@main/screenshots/03_pdf_invoice_export.png" alt="Vector PDF Invoice" width="100%" />
      <br /><strong>PDF Generation</strong>
      <br /><sub>Vector document with QR code and share spooler</sub>
    </td>
    <td align="center" width="25%">
      <img src="https://cdn.jsdelivr.net/gh/madeel931/invoiceflow-pro-showcase@main/screenshots/04_analytics_financial_trends.png" alt="Financial Analytics" width="100%" />
      <br /><strong>Financial Trends</strong>
      <br /><sub>Interactive revenue curves and cash-flow reporting</sub>
    </td>
  </tr>
  <tr>
    <td align="center" width="25%">
      <img src="https://cdn.jsdelivr.net/gh/madeel931/invoiceflow-pro-showcase@main/screenshots/05_customers_management.png" alt="Customer CRM" width="100%" />
      <br /><strong>Customer CRM</strong>
      <br /><sub>Client directory with real-time balance tracking</sub>
    </td>
    <td align="center" width="25%">
      <img src="https://cdn.jsdelivr.net/gh/madeel931/invoiceflow-pro-showcase@main/screenshots/06_products_and_services.png" alt="Catalog Items" width="100%" />
      <br /><strong>Items & Services</strong>
      <br /><sub>Rate card catalog with pre-configured tax rates</sub>
    </td>
    <td align="center" width="25%">
      <img src="https://cdn.jsdelivr.net/gh/madeel931/invoiceflow-pro-showcase@main/screenshots/07_invoices_filtering.png" alt="Invoice Filtering" width="100%" />
      <br /><strong>Status Filtering</strong>
      <br /><sub>Compound status and date range filtering</sub>
    </td>
    <td align="center" width="25%">
      <img src="https://cdn.jsdelivr.net/gh/madeel931/invoiceflow-pro-showcase@main/screenshots/08_backup_google_drive.png" alt="Google Drive Backup" width="100%" />
      <br /><strong>Cloud Backup</strong>
      <br /><sub>Automated Google Drive AppData sync</sub>
    </td>
  </tr>
</table>

<details>
<summary><strong>View Additional Interface Screens (Dark Mode, Business Profile, Activity Trail)</strong></summary>
<br />

<table>
  <tr>
    <td align="center" width="25%">
      <img src="https://cdn.jsdelivr.net/gh/madeel931/invoiceflow-pro-showcase@main/screenshots/09_business_branding_profile.png" alt="Business Profile" width="100%" />
      <br /><strong>Business Profile</strong>
      <br /><sub>Logo, Tax ID, address, and base currency</sub>
    </td>
    <td align="center" width="25%">
      <img src="https://cdn.jsdelivr.net/gh/madeel931/invoiceflow-pro-showcase@main/screenshots/10_dark_mode_dashboard.png" alt="Dark Mode" width="100%" />
      <br /><strong>Dark Mode</strong>
      <br /><sub>AMOLED theme for low-light environments</sub>
    </td>
    <td align="center" width="25%">
      <img src="https://cdn.jsdelivr.net/gh/madeel931/invoiceflow-pro-showcase@main/screenshots/11_activity_audit_trail.png" alt="Activity Audit Trail" width="100%" />
      <br /><strong>Audit Trail</strong>
      <br /><sub>Chronological log of transactions and changes</sub>
    </td>
    <td align="center" width="25%">
      <img src="https://cdn.jsdelivr.net/gh/madeel931/invoiceflow-pro-showcase@main/screenshots/12_analytics_invoice_breakdown.png" alt="Analytics Breakdown" width="100%" />
      <br /><strong>Status Breakdown</strong>
      <br /><sub>Donut charts and volume distribution</sub>
    </td>
  </tr>
  <tr>
    <td align="center" width="25%">
      <img src="https://cdn.jsdelivr.net/gh/madeel931/invoiceflow-pro-showcase@main/screenshots/13_backup_local_storage.png" alt="Local Storage Backup" width="100%" />
      <br /><strong>Local Backup</strong>
      <br /><sub>Encrypted snapshot export and import</sub>
    </td>
    <td align="center" width="25%">
      <img src="https://cdn.jsdelivr.net/gh/madeel931/invoiceflow-pro-showcase@main/screenshots/14_backup_cloud_status.png" alt="Backup Status" width="100%" />
      <br /><strong>Backup Status</strong>
      <br /><sub>Storage summaries and device sync health</sub>
    </td>
    <td width="25%"></td>
    <td width="25%"></td>
  </tr>
</table>

</details>

---

## 🏗️ Architecture & System Design

The application implements a **feature-oriented Clean Architecture** enforcing unidirectional data flow and strict layer boundaries.

```mermaid
graph TD
    subgraph Presentation_Layer ["Presentation Layer"]
        UI["Flutter Widgets / Screens"] -->|User Actions| Cubit["Feature Cubits"]
        Cubit -->|Immutable States| UI
    end

    subgraph Domain_Layer ["Domain Layer - Pure Dart"]
        Cubit -->|Executes| UC["Use Cases"]
        UC -->|Coordinates| REPO_INTERFACE["Repository Interfaces"]
        UC -->|Operates on| ENTITIES["Domain Entities"]
    end

    subgraph Data_Layer ["Data Layer"]
        REPO_INTERFACE -.->|Implemented by| REPO_IMPL["Repository Implementations"]
        REPO_IMPL -->|CRUD / Queries| ISAR["Isar Local DB"]
        REPO_IMPL -->|OAuth AppData Sync| DRIVE["Google Drive API"]
        REPO_IMPL -->|Serializes / Deserializes| MAPPERS["Data Models & Mappers"]
    end
```

### Layer Responsibilities:
* **Presentation Layer:** State management handled via `flutter_bloc` (Cubit). Widgets subscribe to strongly typed states and dispatch user intents. Zero business or calculation logic resides in widgets.
* **Domain Layer:** Pure Dart module containing business entities, value objects, and granular use cases (`SaveInvoiceUseCase`, `CalculateTotalsUseCase`, `RestoreBackupUseCase`). Free from Flutter framework or database packages.
* **Data Layer:** Concrete repository implementations coordinating the embedded Isar database, file storage, and external Google Drive AppData synchronization.

---

## ⚙️ Key Engineering Highlights

### 1. Controlled Rounding & Monetary Calculations
Controlled rounding boundaries: monetary calculations (line subtotals, item-level compounding taxes, percentage discounts, and payment balances) are rounded consistently at defined domain/persistence boundaries to reduce cumulative rounding discrepancies. Overpayment guards protect against negative balances.

### 2. Embedded Offline-First Storage (Isar)
Utilizes an embedded database compiled to native C++ binaries. Complex invoice queries, status filters, and customer balance recalculations execute via indexed queries. Live query streams (`watchLazy`) automatically refresh views on write.

### 3. Native Vector PDF Compilation
Invoices and customer statements are generated directly on-device as vector PDFs using the `pdf` package. Dynamic layout pagination dynamically measures table rows to prevent orphaned elements and overlapping headers. Includes QR code generation for payment or invoice-related information.

### 4. Multilingual & Bidirectional Support (LTR / RTL)
Full support for English (`en`, LTR), Arabic (`ar`, RTL), and Urdu (`ur`, RTL). Custom script shaping (`arabic_reshaper`) and Unicode bidirectional analysis (`bidi`) ensure cursive Arabic and Urdu glyphs join correctly inside custom PDF canvases and UI components.

### 5. Dual-Layer Backup Engine
Combines local database snapshot export/import with automated Google Drive AppData synchronization. Backup integrity is validated with SHA-256 before restoration, reducing the risk of importing corrupted or altered archives.

---

## 🧩 Technical Challenges & Solutions

| Challenge | Problem | Engineering Approach | Verified Result |
|---|---|---|---|
| **Monetary Calculations** | Cumulative calculation drift in compound tax/discount math. | Evaluated taxes per item line before summing; rounded consistently at defined domain/persistence boundaries. | Consistent rounding behavior across multi-item statements. |
| **RTL PDF Typography** | Standard mobile PDF engines render Arabic/Urdu characters disconnected and in reverse order. | Passed strings through contextual character reshaping (`arabic_reshaper`) and bidirectional analysis (`bidi`) before canvas drawing. | Typographically correct, connected Arabic and Urdu text rendering on vector PDFs. |
| **Silent Restore Corruption** | Incomplete or interrupted backup file transfers could corrupt local database collections. | Calculated a SHA-256 checksum during creation and verified the digest against the archive prior to restore. | Corrupted or incomplete backup files fail validation before database writes are attempted. |
| **Android Alarm Constraints** | Android 13+ restricts `SCHEDULE_EXACT_ALARM`, risking crashes if permissions are withheld. | Wrapped scheduling in an error handler catching `exact_alarms_not_permitted` and falling back to inexact scheduling. | Graceful notification delivery fallback without unhandled exceptions on newer Android versions. |
| **Authentication UI Flicker** | Asynchronous Google Sign-In checks during initial page load caused transient "Disconnected" flashes. | Persisted the verified identity in local secure preferences and hydrated the UI state synchronously on launch. | Immediate, steady UI presentation with background token refresh. |

---

## 🛠️ Technology Stack

| Layer / Area | Technology | Purpose |
|---|---|---|
| **Framework** | Flutter 3.x | Multi-platform UI framework |
| **Language** | Dart 3.5+ | Core object-oriented programming language |
| **State Management** | flutter_bloc (Cubit) | Unidirectional reactive state management |
| **Architecture** | Clean Architecture | Separation of presentation, domain, and data |
| **Dependency Injection** | GetIt | Dependency injection / service locator |
| **Database** | Isar | Embedded local database with transactional writes |
| **Document Processing** | pdf & printing | Native vector PDF rendering and print spooling |
| **Internationalization** | arabic_reshaper & bidi | RTL glyph shaping and bidirectional text flow |
| **Data Visualization** | fl_chart | Interactive financial trend and donut charts |
| **Cloud Synchronization** | googleapis & google_sign_in | Private Google Drive AppData backup sync |
| **Notifications** | flutter_local_notifications | Local payment due date scheduling |
| **Routing** | GoRouter | Declarative, type-safe navigation stack |
| **Testing** | flutter_test & bloc_test | Comprehensive unit, widget, and state test suites |

---

## 🧪 Automated Testing

The codebase includes an extensive suite of automated tests verifying core business logic and UI behavior:

* **Suite Composition:** 93 automated test files are included in the project, covering domain calculations, repository mappings, state transition sequences, and layout mirroring.
* **Test Scope:** Unit, widget, and regression test suites validating domain calculations, Cubit state emissions, and bidirectional layout mirroring.
* **Static Analysis:** Clean pass under `flutter analyze` with 0 warnings, 0 errors, and strict `flutter_lints` adherence.

For detailed testing architecture and execution instructions, see [docs/TESTING.md](docs/TESTING.md).

---

## 📚 Technical Documentation

For in-depth architectural and implementation details, explore the documentation guides:

* [Technical Case Study](docs/CASE_STUDY.md) — Comprehensive design document detailing problem scope, data models, and decisions.
* [Architecture Guide](docs/ARCHITECTURE.md) — Deep dive into layer boundaries, dependency injection, and data flow diagrams.
* [Technical Highlights](docs/TECHNICAL_HIGHLIGHTS.md) — Detailed breakdown of financial math, PDF compilation, and RTL shaping.
* [Testing & Quality Assurance](docs/TESTING.md) — Overview of the test suite structure, Cubit tests, and regression harnesses.

---

## 💼 Commercial Availability

InvoiceFlow Pro is a commercial software product developed by **ADii Labs**.

The complete commercial source code is intentionally not included in this public showcase repository. 

For commercial licensing, white-label deployment, or custom Flutter software development inquiries:

* **Developer:** Muhammad Adeel
* **GitHub:** [@madeel931](https://github.com/madeel931)
* **Email:** [engineer.adeel.pk@gmail.com](mailto:engineer.adeel.pk@gmail.com)
* **LinkedIn:** [Muhammad Adeel](https://linkedin.com/in/muhammad-adeel-ab2a90144)

---

<div align="center">
  <sub>Engineered by <strong>Muhammad Adeel</strong> &bull; ADii Labs</sub>
</div>
