# InvoiceFlow Pro — Interface Mockups & Screenshots

This directory contains high-resolution application screenshots demonstrating the core workflows, UI architecture, and design system of **InvoiceFlow Pro**.

All mockups are rendered from active application builds featuring sample business data, real-time balances, multi-currency formatting, and localized typography.

---

## 📱 Core Commercial Workflows

| Screen | Workflow & Architecture Highlights |
|:---:|:---|
| <img src="https://cdn.jsdelivr.net/gh/madeel931/invoiceflow-pro-showcase@main/screenshots/01_dashboard_overview.png" alt="Dashboard Overview" width="280" /> | **01 — Executive Dashboard**<br />• Aggregated revenue and outstanding balance summaries.<br />• Real-time KPI cards driven by reactive Isar query streams.<br />• Quick-action entry points for invoices, customers, and exports. |
| <img src="https://cdn.jsdelivr.net/gh/madeel931/invoiceflow-pro-showcase@main/screenshots/02_create_invoice_flow.png" alt="Invoice Creation Flow" width="280" /> | **02 — Invoice Builder & Tax Flow**<br />• Structured multi-step creation flow (customer, line items, discounts, taxes).<br />• Controlled rounding boundaries evaluated per item.<br />• Instant subtotal and balance recalculation with consistent rounding. |
| <img src="https://cdn.jsdelivr.net/gh/madeel931/invoiceflow-pro-showcase@main/screenshots/03_pdf_invoice_export.png" alt="PDF Invoice Export" width="280" /> | **03 — Native Vector PDF Generation**<br />• Multi-page document compilation using the `pdf` vector engine.<br />• Dynamic QR code generation for payment and invoice-related information.<br />• Contextual font shaping (`NotoSansArabic` / `arabic_reshaper`) for LTR & RTL. |
| <img src="https://cdn.jsdelivr.net/gh/madeel931/invoiceflow-pro-showcase@main/screenshots/04_analytics_financial_trends.png" alt="Financial Analytics" width="280" /> | **04 — Financial Trends & Analytics**<br />• Interactive monthly cash-flow and revenue progression curves.<br />• Status-segmented income metrics.<br />• Localized date range filtering and aggregation. |

---

## 👥 Customer CRM & Operations

| Screen | Workflow & Architecture Highlights |
|:---:|:---|
| <img src="https://cdn.jsdelivr.net/gh/madeel931/invoiceflow-pro-showcase@main/screenshots/05_customers_management.png" alt="Customer CRM" width="280" /> | **05 — Customer Management CRM**<br />• Client directory with real-time balance tracking and invoice histories.<br />• Instant search and contact association.<br />• Individual customer statement generation. |
| <img src="https://cdn.jsdelivr.net/gh/madeel931/invoiceflow-pro-showcase@main/screenshots/06_products_and_services.png" alt="Products & Services Catalog" width="280" /> | **06 — Products & Services Rate Card**<br />• Item catalog with pre-configured unit prices and tax rates.<br />• Rapid auto-fill integration inside invoice creation.<br />• Support for service and product units. |
| <img src="https://cdn.jsdelivr.net/gh/madeel931/invoiceflow-pro-showcase@main/screenshots/07_invoices_filtering.png" alt="Invoice Filtering" width="280" /> | **07 — Advanced Status & Date Filtering**<br />• Compound status filtering: `Draft`, `Unpaid`, `PartiallyPaid`, `Paid`, `Cancelled`.<br />• Date range queries on indexed Isar fields.<br />• Reactive list updates. |
| <img src="https://cdn.jsdelivr.net/gh/madeel931/invoiceflow-pro-showcase@main/screenshots/08_backup_google_drive.png" alt="Google Drive Backup" width="280" /> | **08 — Google Drive Cloud Backup**<br />• OAuth AppData folder synchronization.<br />• Background authentication handling.<br />• SHA-256 snapshot integrity verification. |

---

## ⚙️ Customization & Reliability

| Screen | Workflow & Architecture Highlights |
|:---:|:---|
| <img src="https://cdn.jsdelivr.net/gh/madeel931/invoiceflow-pro-showcase@main/screenshots/09_business_branding_profile.png" alt="Business Profile" width="280" /> | **09 — Business Branding & Profile**<br />• Configurable company details, logo, Tax/VAT ID, and address.<br />• Base currency selection and number format preferences.<br />• Embedded into generated PDF headers. |
| <img src="https://cdn.jsdelivr.net/gh/madeel931/invoiceflow-pro-showcase@main/screenshots/10_dark_mode_dashboard.png" alt="Dark Mode" width="280" /> | **10 — High-Contrast Dark Mode**<br />• Dark theme designed for comfortable low-light use and OLED displays.<br />• Dynamic color token switching via `ThemeCubit`.<br />• Material 3 design system. |
| <img src="https://cdn.jsdelivr.net/gh/madeel931/invoiceflow-pro-showcase@main/screenshots/11_activity_audit_trail.png" alt="Activity History" width="280" /> | **11 — Activity History**<br />• Chronological transaction and application event log.<br />• Traceability for invoice status changes, payments, and backup events. |
| <img src="https://cdn.jsdelivr.net/gh/madeel931/invoiceflow-pro-showcase@main/screenshots/12_analytics_invoice_breakdown.png" alt="Invoice Breakdown" width="280" /> | **12 — Status & Volume Breakdown**<br />• Visual distribution charts across invoice stages.<br />• Quick identification of overdue and pending invoices.<br />• Summary reporting. |
| <img src="https://cdn.jsdelivr.net/gh/madeel931/invoiceflow-pro-showcase@main/screenshots/13_backup_local_storage.png" alt="Local Storage Backup" width="280" /> | **13 — Local Database Snapshot Export**<br />• Offline database snapshot export and restore.<br />• SHA-256 integrity verification before restoration.<br />• No cloud dependency for local backup ownership. |
| <img src="https://cdn.jsdelivr.net/gh/madeel931/invoiceflow-pro-showcase@main/screenshots/14_backup_cloud_status.png" alt="Backup Status" width="280" /> | **14 — Backup Health & Sync Status**<br />• Status cards for local and cloud snapshots.<br />• Last synced timestamp and archive size information.<br />• Manual sync trigger. |
