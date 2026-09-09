# InvoiceFlow Pro — Interface Mockups & Screenshots

This directory contains high-resolution application screenshots demonstrating the core workflows, UI architecture, and design system of **InvoiceFlow Pro**.

All mockups are rendered from active application builds featuring sample business data, real-time balances, multi-currency formatting, and localized typography.

---

## 📱 Core Commercial Workflows

| Screen | Workflow & Architecture Highlights |
|:---:|:---|
| <img src="https://cdn.jsdelivr.net/gh/madeel931/invoiceflow-pro-showcase@main/screenshots/01_dashboard_overview.png" alt="Dashboard Overview" width="280" /> | **01 — Executive Dashboard**<br />• Aggregated revenue and outstanding balance summaries.<br />• Real-time KPI cards driven by reactive Isar query streams.<br />• Quick-action entry points for invoices, customers, and exports. |
| <img src="https://cdn.jsdelivr.net/gh/madeel931/invoiceflow-pro-showcase@main/screenshots/02_create_invoice_flow.png" alt="Invoice Creation Flow" width="280" /> | **02 — Invoice Builder & Tax Flow**<br />• Structured multi-step creation flow (customer, line items, discounts, taxes).<br />• Deterministic fixed-point financial arithmetic evaluated per item.<br />• Instant subtotal and balance recalculation without round-off drift. |
| <img src="https://cdn.jsdelivr.net/gh/madeel931/invoiceflow-pro-showcase@main/screenshots/03_pdf_invoice_export.png" alt="PDF Invoice Export" width="280" /> | **03 — Native Vector PDF Generation**<br />• Multi-page document compilation using the `pdf` vector engine.<br />• Dynamic QR code generation for payment and verification.<br />• Contextual font shaping (`NotoSansArabic` / `arabic_reshaper`) for LTR & RTL. |
| <img src="https://cdn.jsdelivr.net/gh/madeel931/invoiceflow-pro-showcase@main/screenshots/04_analytics_financial_trends.png" alt="Financial Analytics" width="280" /> | **04 — Financial Trends & Analytics**<br />• Interactive monthly cash-flow and revenue progression curves.<br />• Status-segmented income metrics.<br />• Localized date range filtering and aggregation. |

---

## 👥 Customer CRM & Operations

| Screen | Workflow & Architecture Highlights |
|:---:|:---|
| <img src="https://cdn.jsdelivr.net/gh/madeel931/invoiceflow-pro-showcase@main/screenshots/05_customers_management.png" alt="Customer CRM" width="280" /> | **05 — Customer Management CRM**<br />• Client directory with real-time balance tracking and invoice histories.<br />• Instant search and contact association.<br />• Individual customer statement generation. |
| <img src="https://cdn.jsdelivr.net/gh/madeel931/invoiceflow-pro-showcase@main/screenshots/06_products_and_services.png" alt="Products & Services Catalog" width="280" /> | **06 — Products & Services Rate Card**<br />• Item inventory catalog with pre-configured unit prices and tax rates.<br />• Rapid auto-fill integration inside invoice creation.<br />• Support for tiered pricing and service units. |
| <img src="https://cdn.jsdelivr.net/gh/madeel931/invoiceflow-pro-showcase@main/screenshots/07_invoices_filtering.png" alt="Invoice Filtering" width="280" /> | **07 — Advanced Status & Date Filtering**<br />• Compound status filtering: `Draft`, `Unpaid`, `PartiallyPaid`, `Paid`, `Cancelled`.<br />• Custom date range queries executed on indexed Isar fields.<br />• Real-time reactive list updates. |
| <img src="https://cdn.jsdelivr.net/gh/madeel931/invoiceflow-pro-showcase@main/screenshots/08_backup_google_drive.png" alt="Google Drive Backup" width="280" /> | **08 — Google Drive Cloud Sync**<br />• Automated OAuth AppData folder synchronization.<br />• Silent token refresh with zero UI disruption.<br />• SHA-256 cryptographic snapshot verification. |

---

## ⚙️ Customization & Reliability

| Screen | Workflow & Architecture Highlights |
|:---:|:---|
| <img src="https://cdn.jsdelivr.net/gh/madeel931/invoiceflow-pro-showcase@main/screenshots/09_business_branding_profile.png" alt="Business Profile" width="280" /> | **09 — Business Branding & Profile**<br />• Configurable company details, logo, Tax/VAT ID, and address.<br />• Base currency selection and number format preferences.<br />• Embedded directly into generated PDF headers. |
| <img src="https://cdn.jsdelivr.net/gh/madeel931/invoiceflow-pro-showcase@main/screenshots/10_dark_mode_dashboard.png" alt="AMOLED Dark Mode" width="280" /> | **10 — High-Contrast Dark Mode**<br />• Pure dark theme optimized for OLED/AMOLED displays and battery conservation.<br />• Dynamic color token switching via `ThemeCubit`.<br />• Fully compliant with Material 3 design specifications. |
| <img src="https://cdn.jsdelivr.net/gh/madeel931/invoiceflow-pro-showcase@main/screenshots/11_activity_audit_trail.png" alt="Activity Audit Trail" width="280" /> | **11 — Activity & Audit Trail**<br />• Immutable chronological transaction log.<br />• Traceability for invoice status changes, payments, and backup events.<br />• Debugging and compliance support. |
| <img src="https://cdn.jsdelivr.net/gh/madeel931/invoiceflow-pro-showcase@main/screenshots/12_analytics_invoice_breakdown.png" alt="Invoice Breakdown" width="280" /> | **12 — Status & Volume Breakdown**<br />• Visual distribution charts across invoice stages.<br />• Quick identification of overdue and pending invoices.<br />• Exportable summary reports. |
| <img src="https://cdn.jsdelivr.net/gh/madeel931/invoiceflow-pro-showcase@main/screenshots/13_backup_local_storage.png" alt="Local Storage Backup" width="280" /> | **13 — Local Database Snapshot Export**<br />• Offline export and restore of encrypted Isar database archives.<br />• Integrity checksum confirmation prior to restoration.<br />• Zero cloud dependencies for complete data ownership. |
| <img src="https://cdn.jsdelivr.net/gh/madeel931/invoiceflow-pro-showcase@main/screenshots/14_backup_cloud_status.png" alt="Cloud Sync Health" width="280" /> | **14 — Backup Health & Sync Status**<br />• Detailed status cards for local and cloud snapshots.<br />• Last synced timestamp and archive size verification.<br />• One-tap manual sync triggers. |
