# Master Business Requirements (Non-Technical)

This document is strictly for business requirements.
It should not include software engineering implementation details.

## 1) Business Overview

- Business name: Mahi Solar Solution
- Domain: Solar products and services
- Mission: [To be filled]
- Vision: [To be filled]

## 2) Business Goals

- Short-term goals:
  - [To be filled]
- Long-term goals:
  - [To be filled]

## 3) Target Customers

- Customer segments:
  - Residential
  - Commercial
  - Industrial
- Customer pain points:
  - [To be filled]
- Customer expectations:
  - [To be filled]

## 4) Core Offerings

- Products:
  - Solar panels
  - Inverters
  - Batteries
  - Mounting structures
  - Other electrical and energy products
- Services:
  - Site survey
  - Solar system design and consultation
  - Installation and commissioning
  - Annual maintenance contracts (AMC)
  - Repair and support for other electrical work
- Value proposition:
  - Reliable energy solutions with transparent pricing and service support

## 5) End-to-End Business Process

1. Lead generation
2. Inquiry and qualification
3. Site survey and assessment
4. Proposal and quotation
5. Customer approval and agreement
6. Installation planning
7. Installation execution
8. Testing and commissioning
9. Handover and training
10. After-sales service and maintenance

> Note: We will expand each process step with detailed business rules as requirements are shared.

## 5.1) Quotation Requirements

The business needs a standard quotation format to ensure consistent pricing and approvals.

### Quotation Types

- Solar Quotation
- Other Quotation (non-solar products/services)

### Common Quotation Fields (Applicable to All)

- Quotation number
- Quotation date
- Customer name and contact details
- Site/location details
- Sales owner
- Item-wise description
- Quantity and unit price
- Subtotal, tax, and final total
- Payment terms
- Delivery/installation timeline
- Warranty terms
- Validity period of quotation
- Notes and approval status

### Solar Quotation - Required Details

- System capacity (kW)
- Panel brand/model and quantity
- Inverter brand/model and quantity
- Battery details (if applicable)
- Structure and mounting details
- Estimated generation and savings
- Installation scope
- Net metering support (if applicable)
- Warranty split (product warranty vs installation warranty)
- Optional AMC plan

### Other Quotation - Required Details

- Category of offering (product/service)
- Brand/model/specification
- Service scope (if service-based)
- Material and labor breakup
- Delivery scope and exclusions
- Support and warranty commitment

### Quotation Business Rules (Initial)

- Every quotation must be assigned one quotation type: Solar or Other.
- Quotation numbering must be unique.
- Final quote must include tax and total amount.
- Discount, if any, requires approval above a defined threshold.
- Expired quotations cannot be directly converted into confirmed orders.

### Required Customer Documents

#### Solar Quotation Documents

- PAN Card
- Aadhaar Card
- Passbook (bank passbook copy)
- Electricity Bill (latest 6 months copy)

#### Other Quotation Documents

- PAN Card
- Aadhaar Card
- Passbook (bank passbook copy)
- Electricity Bill (latest 6 months copy)

## 5.2) Login, Subsidy, and Loan-to-Bank File Process

This section defines the business sequence for subsidy and loan-related processing.

### Step 1: Login

- User must complete login first.
- Without login, no subsidy or loan process can start.

### Step 2: Subsidy Flow (Cash Case)

If the project is in cash mode:

1. Login
2. Complete site installation
3. Start subsidy process
4. Apply for subsidy as per eligibility:
   - Central subsidy
   - State subsidy
   - Both Central and State subsidy (if allowed by policy)

### C) Subsidy Flow - Loan Case

1. Login
2. Apply for loan
3. Process vendorship
4. Complete site installation
5. Start subsidy process
6. Apply for subsidy as per eligibility:
   - Central subsidy
   - State subsidy
   - Both Central and State subsidy (if allowed by policy)

### D) Bank File Submission Order (Loan Case)

1. PM Surya app form
2. Subsidy details/form
3. Feasibility report
4. Required customer documents
5. Loan File Book (client signature, first installment, and second installment details for loan cases)

### E) Required Documents (Applicable in Both Cash and Loan Cases)

- PAN Card
- Aadhaar Card
- Passbook (bank passbook copy)
- Electricity Bill (latest 6 months copy)

## 5.3) Structure Installation and Material List Form Process

This section defines the process for structure work, panel installation, and material tracking.

### Structure and Installation Flow

1. Login
2. Create/select site project
3. Start structure work at site
4. Install panels and required materials
5. Update used material quantities in material list form
6. Confirm site installation completion

### Structure Set, Electrical Setup, and Verification

1. Complete structure setup at site.
2. Install solar panels on approved structure.
3. Complete wiring connection for panel-to-inverter and inverter-to-meter path.
4. Install inverter, **meter** (meter installation per utility/DISCOM requirements), and related electrical accessories as per approved plan.
   - **Net metering:** complete net metering scope inside the meter work (correct meter type, import/export or bidirectional setup, and compliance with applicable utility and scheme rules).
5. Perform electrical check and verification using multimeter (including meter terminals and net metering-related checks where applicable).
6. Record verification outcome (pass/fail) with remarks.
7. Upload photos of complete plant installation.
8. Upload clear photo(s) of installed inverter.
9. Upload clear photo(s) of installed **meter(s)**, including net metering display (import/export or relevant readings) where applicable.

### Photo Verification

Uploaded photos must pass **photo verification** before the site step is treated as complete for reporting or subsidy/loan file use.

1. A designated verifier (for example: site supervisor, operations, or admin as per policy) reviews each required photo set: full plant, inverter, and meter(s) including net metering display where applicable.
2. Verification checks should include: photo clarity, correct site/project reference, visible key components, and alignment with the approved installation scope.
3. Each verification must have a status: **Approved**, **Rejected**, or **Resubmit requested**, with short remarks when not approved.
4. Rejected or incomplete photo sets must be re-uploaded and verified again.
5. Verification date, verifier name, and status must be stored for audit (same evidence may be referenced in DCR or work completion reports).

### DCR Report, Work Completion Report, and Vendor

After structure, electrical verification, photo upload, and **photo verification**:

1. Prepare and submit **DCR report** (as per scheme/bank or internal format).
2. Prepare and submit **work completion report** for the site.
3. Record **vendor** details and vendor confirmation linked to the project (where applicable).
4. Attach or reference supporting evidence (photos, multimeter readings, dates) with these reports.
5. Mark reports as submitted/approved before moving to subsidy or loan file steps.

### Material List Form (Per Site)

The material list form should capture:

- Site/project reference
- Material category (for example: Structure, Electrical, Panel Accessories)
- Material name
- Unit (pcs, foot, meter, etc.)
- Opening quantity
- Issued to site quantity
- Returned from site quantity
- Scrap quantity
- Installed/consumed quantity
- Available balance
- Buy price and sale price (if needed for business tracking)
- Last update date and updated by

### Existing Items Already Implemented (As per shared screen)

The following inventory/material management capabilities are already available and should be considered existing:

- Inventory -> Materials page
- Material search
- Category filter
- Group view toggle
- Issue to Site action
- Return from Site action
- Add to Scrap action
- View Scrap action
- Add Material action
- Stock summary cards (Total Items, Total Stock, Stock Value, Low Stock)

### Additional Material Screen Points (New from latest shared screen)

- Total units indicator should be visible at list level (for example: total units count on the right side).
- Group header should show group name with item count (for example: Structure + count).
- Material card/list entry should show specification/size text (for example: M12 thread, 75x75mm, 60x40mm).
- Material quantity display should support mixed units per item (pcs, foot, etc.).

### Change Requirements to Add/Improve

- Add direct linkage between site installation process and material list form entries.
- Ensure structure and panel installation cannot be marked complete without material usage update.
- Maintain per-site material consumption history for audit and subsidy/bank file support.
- Keep material unit consistency (pcs, foot, meter) across issue, return, and installation records.

## 5.4) Module-Wise Headings (Based on Current App)

Use the following heading structure for all business requirements and feature documents.



## 5.5) Material Verification, Transportation, Return Policy, and Tools Condition

This section defines operational terms for material movement and tool quality checks.

### A) Material List Verification

1. Material list must be verified before issue to site.
2. Verification must include item name, quantity, unit, and condition.
3. Site supervisor and store/inventory owner must confirm verification.
4. Any mismatch must be recorded before dispatch.

### B) Transportation Terms (Materials)

1. Transport responsibility must be defined for each dispatch (company/vendor/site).
2. Dispatch record must include date, vehicle details, and reference number.
3. Materials must be checked at loading and unloading points.
4. Damaged or missing materials during transport must be logged immediately.
5. Transportation charges and liability terms must be documented in the record.

### C) Material Return Policy and Terms

1. Unused material must be returned from site with return entry.
2. Return entry must capture material quantity, condition, and reason for return.
3. Return categories:
   - Good reusable material
   - Damaged material
   - Scrap material
4. Good reusable material goes back to available stock.
5. Damaged and scrap material must follow approval and disposal process.
6. Financial adjustment rules (if applicable) must be recorded for damaged/lost material.

### D)  Common Compliance Terms

1. No issue/return/transport entry should be completed without mandatory fields.
2. All entries should maintain date-time and user audit trail.
3. Site-wise history must be available for material and tools for audit and dispute handling.

## 5.6) Tools Module Requirements (As per current screen)

This section captures tools tracking requirements based on the current Tools page.

### A) Tools Summary Cards

The module should display:

- Total Tools
- Available
- In Use
- Under Repair

### B) Tools Operations

The module should support:

- Issue Tool to Site
- Return to Warehouse
- Add Tool

### C) Search and Filters

The module should support:

- Search tools
- Status filter (All/Available/In Use/Under Repair)
- Category filter (for example: Power Tool, Hand Tool, Others)

### D) Tools List Columns

Each tool record should include:

- Tool Name
- Category
- Assigned To
- Site
- Status
- Condition
- Last Updated
- Value
- Actions

### E) Tool Status and Condition Rules

1. Tool status should be one of: Available, In Use, Under Repair.
2. Tool condition should support at least: Good, Minor Damage, Major Damage, Not Working.
3. If condition is "Not Working", status should move to "Under Repair" and tool should not be issued.
4. On issue/return, assigned user and site must be updated.
5. Each update should keep date-time and user audit trail.

### F) Existing Capabilities Already Available (As per shared screen)

- Tools page with summary cards
- Issue Tool to Site action
- Return to Warehouse action
- Add Tool action
- Search and filter controls
- Tool list with status and condition visibility

### G) Tools Verification and Condition Standards (Additional)

1. Every tool issue and return must include condition status.
2. Recommended condition types:
   - Good condition
   - Minor damage
   - Major damage
   - Not working
3. Tool handover must include issued by, received by, date, and signature/confirmation.
4. Damaged tools must be tagged and moved to maintenance/repair workflow.
5. Tools marked "not working" cannot be re-issued until verified after repair.

## 5.7) Bill to Book and Invoice

Commercial billing must follow a clear sequence from order to accounting record and tax document.

### Bill to Book

1. Every confirmed sale or service must be **entered in the bill book** (sales/order register) with a unique reference.
2. Bill-to-book entry must link to: customer, project/site, quotation or order reference, and payment mode (cash/loan).
3. Record date, line items or summary amount, taxes (if applicable), and responsible user.
4. Bill book entries must support audit: corrections only with approval and reason.

### Invoice

1. Issue a formal **invoice** for the customer for taxable or billable amounts as per company policy.
2. Invoice must include: invoice number, invoice date, customer billing details, item/description, quantity, rate, taxes, and total payable.
3. Invoice numbering must be continuous and unique (no gaps without documented reason).
4. Link each invoice to the related quotation, bill-to-book entry, and project where applicable.
5. Payment received must be reconciled against the invoice (full or partial) with date and mode.
6. Credit notes or revised invoices (if any) must reference the original invoice.

### Loan Installments (First and Second)

For **loan** projects, track customer payments in order:

1. **First installment** — amount, due date (if any), payment date, mode, reference, receipt, and confirmation in the Loan File Book.
2. **Second installment** — same fields as applicable under bank or company agreement; record when paid and reconcile against the loan schedule.
3. No installment entry should be marked complete without transaction reference or receipt where required by finance policy.

## 5.8) Presets (Quotations, Invoice, and Inventory Matching)

This section reflects the **Presets** area used to configure standard system bundles (material lists) for **quotations** and **invoice and inventory matching** (as per current screen).

### Summary and Categories

- Presets are grouped by segment, for example: **Residential**, **Commercial**, **Industrial**.
- Summary should show counts such as: total presets, residential count, commercial count, industrial count.

### Filters

- **All** presets
- **For Quotations**
- **For Invoice & Inventory Matching**

### Preset Card Content (Per Preset)

Each preset should show at least:

- System size (kW)
- Total line items count (for example: 17 items for a full BOM)
- Panel summary (brand, wattage, quantity — for example: Waaree 540W, quantity as per kW)
- Inverter summary (brand and kW rating — for example: Growatt matching system size)
- Structure type (for example: Elevated GI)
- Estimated cost (for example: ₹1,85,000 for 3 kW; ₹2,80,000 for 5 kW — illustrative from current presets)
- Purpose tag where applicable: **For Invoice & Inventory Matching** (and/or quotation use)

### Example Residential Presets (From Current Screen)

| System | Panels | Inverter | Structure | Notes |
|--------|--------|----------|-----------|--------|
| 3 kW | 6 × Waaree 540W | Growatt 3 kW | Elevated GI | 17 items; tagged for invoice and inventory matching |
| 5 kW | 10 × Waaree 540W | Growatt 5 kW | Elevated GI | 17 items; tagged for invoice and inventory matching |

Additional items (for example wiring, protection, meter-related materials) may be included inside the full item list even if not shown on the summary card.

### Actions

- Add Preset
- View preset
- Edit preset
- Delete preset

## 5.9) Files, Data, and Gallery (Online and Offline)

The system must support storing and viewing project **files**, structured **data**, and a **gallery** of images, with both **online** and **offline** working patterns where field teams may have poor connectivity.

### Files

1. Users can attach and store files against a customer, site, or project (for example: agreements, bank forms, subsidy papers, DCR, work completion).
2. Each file should have: name, type, upload date, uploaded by, and link to the correct project or milestone.
3. File access should follow role permissions (who can view, upload, or delete).
4. **Offline:** users should be able to queue new file uploads when connection returns, or save locally per app policy, without losing the link to the project.
5. **Online:** uploads should confirm success and show the file in the project file list immediately when connectivity is available.

### Data

1. Operational data (forms, checklists, material usage, installment records) should save reliably and stay linked to the right project.
2. **Online:** data should sync to the server in near real time when possible.
3. **Offline:** users should be able to enter or update data on site; the system should sync when the device is back online, with clear status (saved locally / pending sync / synced).
4. Conflicts or duplicate submissions should be avoided or flagged for review.

### Gallery (Photos and Visual Evidence)

1. **Gallery** should group site photos (plant, inverter, meter, structure, and other evidence) by project and category.
2. Photos should support the **photo verification** workflow (approved / rejected / resubmit).
3. **Online:** gallery view, full-size view, and download or share as per policy.
4. **Offline:** users should be able to capture photos on site; images should attach to the project and upload when online, with visible pending state until upload completes.
5. Thumbnail or preview may be available offline for recently opened projects if supported by the app, without exposing sensitive data to unauthorized users.

## 5.10) Team, Employees, and HR (Payroll and Attendance)

The **Team** area includes employee management and HR workflows. For **employees**, the business needs two linked areas: **Payroll** (money and month-end totals) and **Attendance** (day-to-day presence, which drives Present / Absent / Holiday in payroll).

The following reflects the current **HR** screen (**Payroll** tab) and the dedicated **Attendance** screen (as per shared UI).

### Navigation and Tabs

- Main area title: **HR**
- Primary action: **Add Employee**
- Tabs:
  - **Payroll** (salary and payment tracking)
  - **Site Deployment Board** (site assignment view — separate from payroll detail)

### Attendance Screen (As per Current UI)

**Header**

- Page title: **Attendance**
- **Selected Date** with a date picker (for example: 27-03-2026) and helper text: **(Select past dates to edit)** — user can pick a past date to correct marks.
- Action: **+ Mark Holiday** — record a holiday for the selected date (or scope defined by policy).

**Per-Employee Card**

Each employee appears as a card with:

- Role label (for example: SITE SUPERVISOR, SENIOR INSTALLER, ELECTRICIAN) and an **Active** status badge.
- Profile: avatar, **name**, and **phone number**.
- **Monthly summary** for the month in view (for example: **MARCH 2026 SUMMARY**):
  - **Active Days:** `marked days / days in month` (for example: 0 / 27).
  - **Per day rate** (₹) used to calculate earnings from attendance.
  - Short **attendance breakdown** (for example: P = Present, H = Holiday, PL = Paid Leave).
- **Money snapshot on the card:**
  - **Current earnings** (from attendance × per day rate for the period).
  - **Last month pending** (carry-over), when applicable.
  - **Total payable** (current + pending where the product shows it).
- **Paid leave** line for the month (for example: **Paid Leave (Mar)**) with availability (for example: **1/1 Available**).
- **Daily actions** for the **selected date:** **Present** and **Absent**.

**Attendance and Payroll Link**

1. Marks from this screen must roll up to monthly **Present**, **Absent**, and **Holiday** on **Salary & Payroll**.
2. **Per day rate**, **active days**, and **total payable** on cards must stay consistent with payroll **Pending** / **Advance** after month-end rules.
3. **Past-date edits** follow the “select past dates to edit” rule, with audit/approval if your policy requires it.
4. **Offline:** attendance may be captured without network and synced later with correct date, time, and employee.

### Salary and Payroll (By Month)

- Section title pattern: **Salary & Payroll** with a selected month and year (for example: December 2024).
- Payroll should be viewable and manageable per month for all employees.

### Payroll Table Columns

Each employee row should support at least:

| Column | Purpose |
|--------|---------|
| Employee | Name and role (for example: Site Supervisor, Senior Installer, Electrician) |
| Salary | Base monthly salary amount |
| Present | Count of present days in the month |
| Absent | Count of absent days in the month |
| Holiday | Count of holidays in the month |
| Pending | Salary amount still pending to be paid |
| Advance | Amount already paid in advance or adjusted |
| Actions | Operational actions (see below) |

### Row Actions (Per Employee)

- **Pay** — record or process salary payment toward pending balance.
- **Expense** — add or link an expense entry for that employee.
- **Task** — open or assign tasks related to that employee (for example site or follow-up work).

### Example Roles Shown on Screen (Illustrative)

Roles may include: Site Supervisor, Senior Installer, Electrician, Installer, Helper, Driver — with salaries and attendance tracked in the same payroll table.

### Business Rules (Initial)

1. Employee master data (name, role, salary) should be maintained before monthly payroll is run.
2. Present, absent, and holiday counts should drive or reconcile with **Pending** and **Advance** for the month.
3. Payment actions should leave an audit trail (who paid, when, and amount).
4. Access to payroll and employee financial data should be restricted to authorized roles.

## 5.11) Finance and Accounts

**Scope:** Company-level money: income, expense, payables to suppliers, lender loans and repayments, and partner profit and capital. Customer **quotations**, **bill to book**, **invoices**, and **customer loan installments** (Loan File Book) stay aligned with this module where amounts are recorded or exported.

**Surface name:** Finance and Accounts — *Manage transactions, invoices, and financial reports.*

### Global Actions (All Finance Areas)

| Action | Business meaning |
|--------|------------------|
| Add Expense | Record money going out (operational or project cost). |
| Add Income | Record money coming in (receipts, fees, recoveries). |
| Export Finances | Export data for accounting, audit, or backup; access controlled. |

### Main Sections (Navigation Headings)

| Section | What the business uses it for |
|---------|------------------------------|
| Dashboard | One place to see health of revenue, expenses, profit, and latest movements. |
| Transactions | Detailed ledger-style list of income and expense entries; supports drill-down from approval and export needs. |
| Vendors | Who we buy from, how much we still owe, and how vendors are grouped by category (panels, inverter, structure, etc.). |
| Loans and Repayments | Loans **to the company** from banks or NBFCs (or formal one-off dues): principal, EMI, outstanding, and payment actions. |
| Partners | Investors, co-owners, contractors: invested capital, profit shared, and what is still pending to pay. |

---

### Dashboard

**Goal:** Answer four questions at a glance, then show trend and freshness of data.

1. **Total Revenue** — income recognized in the chosen reporting window (period definition is a product rule; must be consistent with Transactions).
2. **Total Expenses** — expenditure in the same window.
3. **Outstanding** — receivables or payables still open (definition must match Transactions and Vendors/Loans where relevant).
4. **Net Profit** — revenue minus expenses per the same rules (before tax if that is a later enhancement, state clearly in product).

**Trend:** **Revenue vs Expenses** over time (for example by month) so leadership can compare months.

**Activity:** **Recent Transactions** — latest income and expense lines with enough fields to identify amount, type, and link to project or category without opening another system.

---

### Vendors

**Goal:** One vendor master, clear **payables**, and categories that match how you buy for solar (material type).

**Rollups on the list**

- Total vendors | Vendors **with outstanding** | **Total outstanding** (sum due) | **Categories** count

**Finding records**

- Search by name or keyword.
- Filter by category (for example All Categories or one category).

**Minimum data per vendor**

- Name, phone, email, city/state.
- **Categories** supplied (examples: solar panels, inverter, battery, cable, tools, structure).
- **Amount due** (outstanding to that vendor).
- **View** full record | **Edit** master data | **Add Vendor** for new suppliers.

**Business expectation:** Vendor outstanding should reconcile with purchase and payment entries recorded through Transactions (or linked flows) so Finance totals stay trustworthy.

---

### Loans and Repayments

**Goal:** Track **organization loans** (not the same as customer EMIs on the Loan File Book unless you explicitly link them in a future rule).

**Rollups**

- Active loan count | **Total principal** | **Total outstanding** | **Combined monthly EMI** (EMI-type loans only, per product rule)

**Finding records**

- Search | Filter **Status** | Filter **Type** (for example EMI vs One-Time)

**Register columns**

| Column | Meaning |
|--------|---------|
| Source | Lender or bank name (or counterparty for one-time). |
| Type | EMI loan vs one-time / bullet repayment. |
| Principal | Original disbursed amount. |
| Rate | Interest rate where applicable. |
| Payment Info | INR per month for EMI, or **due date** for one-time. |
| Outstanding | Remaining principal or balance to close. |
| Status | For example Active, Closed. |
| Actions | **Pay EMI** or **Record Payment** as appropriate. |

**Add Loan** creates a new facility row; every repayment must reduce outstanding and leave an audit trail.

---

### Partners

**Goal:** Track **capital** and **profit-share obligations** to contractors, investors, and co-owners.

**Rollups**

- Partner count | **Total invested** | **Profit shared** (paid out) | **Pending profit** (still owed)

**Finding records**

- Search | Filter **All Types** (or one type: Contractor, Investor, Co-Owner, etc.)

**Minimum data per partner**

- Type, **share percent**, name, contact or reference id.
- **Invested**, **profit paid** to date, **pending** amount.
- **Pay** — post a payout against pending | **Details** — history and full profile.

**Add Partner** for new relationships; payout actions require authorized role.

---

### Cross-Cutting Finance Rules

1. **Single source of truth:** Dashboard KPIs must be derivable from Transactions (and linked entities), not manual-only overrides without audit.
2. **Audit:** Who created or changed an amount, when, and which project or vendor or loan it touched.
3. **Access:** Finance tabs, export, and payment actions are role-restricted.
4. **Naming:** Customer-facing loan installments remain documented in **Loan File Book** and subsidy/bank sections; **Loans and Repayments** here = **company** borrowings unless you later define an explicit link.

## 5.12) Analytics and Reports

**Purpose:** *Business insights and performance metrics* for the solar business — one screen with filters, KPIs, segment mix, top performers, and export.

**Period filter:** This month | This quarter | This year | Yearly (full selected year). All metrics follow the selected period unless a card states its own comparison (e.g. vs last year).

**Actions:** **Export report** for the current view (role-restricted).

**KPIs (₹ where money):** Total revenue (align with Finance) | Active projects (align with Projects) | Total employees (align with HR / Team) | Stock value (align with Inventory valuation). Optional short trend text per card.

**Project distribution:** Share of projects across **Residential, Commercial, Industrial, Other** (chart + %); percentages for one view must **total 100%**.

**Top performers:** Rank by task completion in the period — name, completed/assigned, %; same task definition as Projects/Team.

**Rules:** Revenue, stock, and headcount must match source modules for the same dates. Analytics and export only for authorized roles.

## 5.13) Notifications

**Purpose:** *Manage approval requests from employees* — one place for approvers to see what needs action, with **counts** so workload is visible at a glance (same idea as a total **pending** number on the screen).

### Pending Counts (Notification Numbers)

- Show **total pending** across all types (for example: **8 pending**).
- Each tab shows its **own count**: **Leave (n)**, **Expenses (n)**, **Blockages (n)**. Counts update when items are approved, rejected, or closed.

### Tabs and What Each Covers

| Tab | What it is for |
|-----|----------------|
| **Leave** | Employee leave requests pending approval. |
| **Expenses** | Employee expense claims pending approval. |
| **Blockages** | Site or project blockers reported by the team (delays, dependencies, risks). |

### Leave — Reason / Type

Each leave request must record a **reason or leave type** (pick list + optional note), for example:

- Sick leave  
- Casual leave  
- Earned / privilege leave  
- Emergency leave  
- Other (free text with approver visibility)

### Expenses — Reason / Category

Each expense request must record a **category or reason**, for example:

- Food  
- Medical  
- Travel / fuel  
- Lodging  
- Tools or small materials  
- Other (with short description)

### Blockages — Reason / Type

Each blockage must record a **type or reason** so management can filter and fix patterns, for example:

- Weather (rain, heat, unsafe conditions)  
- Site not ready / work not completed upstream  
- Workload / crew availability  
- Material delay or transport  
- Client decision or approval pending (layout change, sign-off)  
- Technical issue (for example cable routing, structure, grid)  
- Other (short description)

*(Examples from the field: Weather delay, cable routing pending client sign-off, material transport delay.)*

### Each Item in the List (Card or Row)

- **Title** — short label (leave type, expense headline, or blockage type).  
- **Project** — site name and system size where relevant (for example **Verma Bungalow 8 kW**).  
- **Description** — what happened and current status.  
- **Resolved by** — name of person who cleared it (when applicable).  
- **Date** — submitted or last updated date.  
- **View details** — full record, attachments, and approve/reject or mark resolved.  
- **Reference** — optional **notification or ticket number** per item for support and audit (in addition to tab counts).

### Rules

1. Counts on tabs and header must match the number of items still **pending** in that queue.  
2. Approvers see only queues their role is allowed to act on.  
3. Approved leave should flow to **Attendance / HR**; approved expenses to **Finance** where payment is recorded.

## 5.14) Settings

**Purpose:** Central place for **profile**, **company**, **team and roles**, **master lists** (dropdowns and categories), and other global configuration. Headings match the product navigation.

### Settings — Main Sections (Sidebar)

| Section | What it is for |
|---------|----------------|
| **Profile** | Logged-in user’s own details. |
| **Company** | Legal and billing identity of the business. |
| **Team** | Members, roles, and inviting or adding users. |
| **Masters** | **Master Data Management** — dropdowns and categories used across the app. |
| **Appearance** | Theme (light / dark / system) and accent colors. |
| **Security** | Change password and related account security. |
| **User Flow** | Workflow or step configuration where the product supports it. |

### Profile

- **Photo** (avatar), **name**, **phone**, **email**, and other standard user fields the product supports.
- User can update their own profile where policy allows; some fields may be read-only if managed by admin.

### Company

- **Company name**, **GST number**, **address**, and other company master fields needed for invoices, compliance, and reports.
- Only authorized roles may edit company data.

### Team (Settings)

- List every **member** with **name** and **role** (for example **Admin**, **Supervisor**, **Site Supervisor**, and other roles defined in the product).
- **Add member** (or equivalent) to create a user and assign **role** in one flow, or add member then assign role — as implemented, but both capabilities must exist for admins.
- Role changes should be audited (who changed, when).

### Master Data Management

**Surface name:** *Master Data Management* — *Configure dropdowns and categories used across the app.*

**Actions (top of Masters area)**

- **Expand all** — open every master group for quick review.
- **Collapse** — close groups for a compact view.
- **Create Master** — add a new top-level master or category where the product allows (green primary action on screen).

**Master area tabs (horizontal)** — same headings as the app:

1. **Projects** — project-related pick lists (example groups: **Project Types**, **Project Categories**, **Project Owner Types**, **Project Sources**). Each group shows **item count**, can **expand/collapse**, and has **Add item** for new values.
2. **Expenses** — expense types or categories used in Finance and employee expenses.
3. **Inventory and Tools** — material categories, tool categories, units, or similar lists used in **Inventory**.
4. **Finance** — finance-specific dropdowns (payment modes, cost heads, etc.) as defined by the product.
5. **Quotations** — quotation-related masters (types, terms templates, etc.).
6. **HR and Team** — leave types, expense claim categories linked to HR, designation labels, or other HR pick lists.
7. **GST and Tax** — tax rates, HSN/SAC groups, or GST-related options used on invoices and purchases.
8. **System** — application-wide system codes or technical masters the product exposes here.

**Rules**

- Values edited under **Masters** must appear consistently wherever that dropdown is used (Projects, Finance, HR, etc.).
- Deleting or deactivating a master value should not break old records; prefer **inactive** flag over hard delete where possible.
- Only **admin** (or a dedicated **settings** role) may change Masters and company-level Team membership.

### Appearance

- **Theme:** user chooses **Light**, **Dark**, or **System** (match device or OS setting).
- **Accent colors:** user (or company default, if the product defines hierarchy) selects **accent / primary color** for highlights, primary buttons, and key UI emphasis.

### Security

- **Change password:** user enters **current password**, **new password**, and **confirm new password**; enforce policy (minimum length, complexity) and show clear success or error.
- Password change applies to the logged-in account only unless admin reset is a separate admin-only flow elsewhere.

### User Flow

- Last item in Settings sidebar: configure **user flow** or **process steps** where the application allows (for example default order of stages for solar projects, or which approval gates apply). Exact fields depend on product; extend this section when workflow screens are finalized.

## 6) Key Business Rules

- Pricing rules: [To be filled]
- Discount rules: [To be filled]
- Eligibility rules: [To be filled]
- SLA and turnaround expectations: [To be filled]
- Warranty and service commitments: [To be filled]

## 7) Roles and Responsibilities (Business View)

- Sales
- Survey Team
- Operations
- Installation Team
- Service Team
- Finance
- Management

Each role's responsibilities will be added as we capture detailed requirements.

## 11) User Types and Role Structure

The business will have two main user types:

- Admin
- Employee

Each user type will have role-based classification.

### Admin Type - Roles

- Admin
- CEO
- Additional admin roles can be added as needed

### Employee Type - Roles

- Site Supervisor
- Welder
- Civil Worker
- Additional employee roles can be added as needed

### Core Requirement

- Every user must belong to exactly one user type.
- Every user must be assigned a role under that user type.
- User creation and management should always be done based on user type and user role.

## 8) Reporting and KPIs

- Lead conversion rate
- Proposal acceptance rate
- Installation completion time
- Customer satisfaction
- Service resolution time
- Revenue and margin indicators

## 9) Risks and Constraints (Business View)

- [To be filled]

## 10) Open Business Questions

- [To be filled]
