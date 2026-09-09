# LinkedIn Project Description — InvoiceFlow Pro

> **Usage Note:** This write-up can be copied directly into your LinkedIn "Projects" or "Featured" section. It is written specifically for technical recruiters, Saudi Arabian engineering hiring managers, and international remote teams looking for evidence of senior Flutter software engineering capabilities.

---

### Project Title
**InvoiceFlow Pro — Offline-First Mobile Invoicing Application**

### Associated Role
**Lead Mobile Application Developer / Flutter Architect**

### Project Overview
InvoiceFlow Pro is a production-oriented, offline-first mobile invoicing and client accounting application built with Flutter and Dart. Designed for contractors and independent service professionals, the application executes core financial workflows—including invoice creation, complex tax calculations, vector PDF document generation, and customer ledgers—entirely on the client device without requiring persistent internet access.

### Core Engineering Responsibilities & Achievements:
* **Architecture:** Architected the entire system using feature-oriented Clean Architecture, enforcing strict separation across presentation (Cubit / flutter_bloc), domain (pure Dart use cases and entities), and data layers (Isar NoSQL).
* **Deterministic Financial Engine:** Engineered client-side financial computation rules ensuring fixed-point mathematical accuracy across compounding taxes, discounts, partial payments, and balance calculations.
* **On-Device Vector PDF Compilation:** Built a high-performance document rendering pipeline (`pdf`, `printing`) that dynamically formats multi-page invoices with embedded payment QR codes and native share spoolers (WhatsApp, Mail, Print).
* **RTL & Bidirectional Localization:** Implemented robust Left-to-Right and Right-to-Left script shaping (`arabic_reshaper`, `bidi`) for English, Arabic (العربية), and Urdu (اردو), including automatic UI mirroring and localized document typography.
* **Resilient Data Persistence & Backup:** Implemented embedded NoSQL storage via Isar for sub-millisecond querying, coupled with a dual-tier backup engine supporting cryptographic SHA-256 local database snapshots and private Google Drive AppData synchronization.
* **Automated Quality Assurance:** Authored a comprehensive automated test suite consisting of 508 passing unit and widget tests covering financial domain logic, state transition sequences, and layout mirroring, maintaining zero static analysis issues under strict lint rules.

### Technologies & Competencies:
* **Languages & Frameworks:** Dart, Flutter SDK
* **State Management:** BLoC / Cubit (`flutter_bloc`)
* **Architecture:** Clean Architecture, Domain-Driven Layering, SOLID Principles, Unidirectional Data Flow
* **Persistence & Storage:** Isar NoSQL Database, SharedPreferences
* **Document Processing:** Vector PDF Generation, Embedded QR Generation, Print/Share Spooling
* **Internationalization:** LTR / RTL Bidirectional Shaping, Multi-Currency Formatting
* **Cloud & OS Integration:** Google Drive OAuth API (`googleapis`), Local Background Notification Scheduling
* **Testing & Tools:** `flutter_test`, `bloc_test`, Git, CI-ready Architecture
