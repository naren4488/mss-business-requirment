# Master Business Requirements — Working Document

This file is built **step by step**. Each pass adds one structured block. The authoritative detailed BRD remains in `MASTER_BUSINESS_REQUIREMENTS.md` until this document replaces or mirrors it.

**Longer explanations** sit under `detail/` and are linked from here — this file stays **short**. Each linked feature doc includes a **TBD tracker** (checkbox-style list) for fields, validations, permissions, and other gaps to close later.

---

## Platform context (summary)

- This document describes the **admin** product. The **employee** product is a **separate project**.
- **Every user** (admin type and employee type) is **created and maintained from the admin product**.
- **Employee-type** users: **employee app only** (field/ops roles, e.g. Site Supervisor, installation worker, civil worker, welder — list can grow).
- **Admin-type** users: **admin app**, and they **can also use the employee app** when needed — **both panels** for admins; **not** both user types on one account.
- **One user type per person** — admin **or** employee, never both on the same login.
- **Admin-type** access level still differs by role (e.g. Super Admin, Admin, CEO, Manager, Accountant, Site Supervisor — list can grow).
- **Full detail:** [Admin vs employee apps and user model](detail/PLATFORM_CONTEXT_ADMIN_AND_EMPLOYEE_PROJECTS.md)

---

## 1) End-to-end flow (steps only)

1. Lead generation  
2. Inquiry and qualification  
3. Site survey and assessment  
4. Proposal and quotation  
5. Customer approval and agreement  
6. **Scheme / portal login and filing** — complete required **file login** and submissions on the relevant **government or scheme portal** (for example **PM Surya** / PM Surya Ghar), as applicable to the project.  
7. **Loan path (when the customer is on loan):** prepare the **loan file** and **process loan documents** per bank or lender requirements.  
8. Installation planning  
9. Installation execution  
10. Testing and commissioning  
11. **Net metering** — complete net metering with the utility / DISCOM (meter work, import–export or bidirectional setup, and related approvals) as applicable.  
12. **Loan path (when the customer is on loan):** **second installment** of the loan process (per bank / Loan File Book rules, after the agreed milestone — typically after commissioning / net metering).  
13. **DCR report** and **subsidy application** (portal steps and documentation per scheme).  
14. **Subsidy granted** — subsidy approved and settled per scheme and finance process.  
15. Handover and training  
16. After-sales service and maintenance  

> **Notes:**  
> - Step 7 (early loan file) and step 12 (second installment) apply only to **loan** projects; **cash** projects skip loan-specific steps.  
> - Step 6 and steps 13–14 depend on **scheme / subsidy** eligibility; ineligible projects may skip or shorten those steps per policy.  
> - **Handover (step 15)** may partly overlap steps 11–14 in day-to-day work; this list follows your **post-commissioning** order first, then formal handover, then ongoing after-sales.

---

## 2) Main product features (titles)

### Sales and customers

- **Enquiries / inquiries** — leads; mandatory name, phone, type, source, priority; optional email, address, capacity, budget, notes, follow-up; statuses (new, in progress, converted, lost); assign to employee; meetings + notes; create quotation when not lost. **Detail:** [Inquiries feature](detail/FEATURE_INQUIRIES.md)  
- Customers  
- **Agents** — commissions (per kW, per file, …), CRUD, per-agent projects and earned/paid/pending (dues can go negative if overpaid). **Detail:** [Agents feature](detail/FEATURE_AGENTS.md)  
- **Quotations (sales)** — Solar vs Other; client + system config + items + pricing + subsidy + payment terms + warranty; draft/save/share/approve flow; preview/PDF with section toggles. **Detail:** [Quotations feature](detail/FEATURE_QUOTATIONS.md)  
- **Presets** — reusable templates (quotation presets first; inventory/task presets later). **Detail:** [Presets feature](detail/FEATURE_PRESETS.md)  

### Billing

- Invoices (bills)  

### Delivery and visibility

- Projects  
- Active sites *(progress view of ongoing work)*  

### Inventory

- Inventory management  
  - Stock / materials  
  - Tools  

### People

- **Employees** — list + **employee details** hub (profile, attendance summary, tasks, expenses, salary/dues/finance). **Detail:** [Employees feature](detail/FEATURE_EMPLOYEES.md)  
- **Attendance** — daily presence, linked to payroll. **Detail:** [Employees feature](detail/FEATURE_EMPLOYEES.md)  

### Finance (day-to-day operations)

- Finance — vendors, loans, partners, expenses, and related operational money flows *(detail to be expanded later)*  

### Finance audit and compliance

- Finance audit *(umbrella)*  
  - Dashboard  
  - Chart of accounts  
  - Profit and loss  
  - Inventory audit  
  - Debtors and creditors  
  - GST compliance  
  - Cash and banks  
  - Expense audits  
  - Fixed assets  
  - Audit logs  
  - Reports and exports  
  - Data flow diagrams  

### Cross-cutting

- Analytics  
- Notifications  

---

*Further sections will be added here as we go.*
