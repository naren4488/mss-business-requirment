# Feature — Employees (detailed BRD)

**Scope:** People records and HR-related processes that the **admin** product manages. Employee-facing actions (tasks, daily use) live primarily in the **employee** product; data and configuration are sourced from the admin side.

## 1) Purpose

- Maintain everyone the business treats as an **employee** (or field user) in one place.
- Support **attendance**, **salary / payroll**, and **employee master data** (and related areas as we add them).

## 2) Admin product — screens (structure)

### Employees listing

- A **listing page** of employees (search, filters, and actions as you define later).

### Employee details page (single employee hub)

Opening one employee opens their **profile / details** area. From this page the business can see **everything for that person in one place**, including at least:

- **Profile details** — identity, role, contact, employment info, documents *(fields TBD)*  
- **Attendance (summary view)** — rolled-up view for that employee *(link to full attendance tooling if separate)*  
- **Finance (employee-centric)** — money side for that person: **salaries**, **dues**, and related totals *(exact widgets TBD)*  
- **Tasks** — assigned work and status *(cross-feature)*  
- **Expenses** — claims or expenses tied to that employee *(cross-feature)*  

Further lines (inventory of tools, site deployment, etc.) can be added here as you confirm them.

## 3) Creation and lifecycle

- New employees are **created from the admin project** as **employee type** (with **role**, per platform rules). **One person = one user type** — not admin and employee together; see `PLATFORM_CONTEXT_ADMIN_AND_EMPLOYEE_PROJECTS.md`.
- **Who can create (current rule):** Any user who is **admin type** may create employees *(subject to change if you later limit this to Super Admin / HR only)*.
- **Credentials:** Login details are communicated **outside the platform** for now (e.g. phone, WhatsApp, in person) — **no automated invite** in v1.
- **Activation:** There is **no separate “activate user”** step. Once the account exists with credentials, **employee-type** users **log in to the employee app only** (they do not get the admin panel).
- **Fields at creation (initial list — final mandatory set TBD):** name, phone number, email, password, address, **role** *(and any other fields you add later)*.
- After creation, the **employee details page** is the main place to review and manage that person’s attendance, money, tasks, and expenses.

## 4) Sub-areas (to expand step by step)

- **Profile / master data** — identity, contact, role, employment status, documents *(detail TBD)*  
- **Attendance** — daily marks, holidays, corrections; **summary on employee details** *(detail TBD)*  
- **Salary / payroll / dues / payments** — *deferred: detailed rules to be discussed later*  
- **Tasks** — *deferred: detailed rules to be discussed later*  
- **Expenses** — claims and approvals *(detail TBD)*  
- **Linkage** — projects, sites, tools *(cross-feature; detail TBD)*  

## 5) Dependencies

- User type / role model (`PLATFORM_CONTEXT_ADMIN_AND_EMPLOYEE_PROJECTS.md`).
- Masters and finance where payroll posts *(TBD)*.
- Tasks and expenses features for deep links from employee details *(TBD)*.

## 6) Open questions

*(Captured as TBD items in §7 where applicable.)*

- Final **mandatory vs optional** fields on create (beyond the initial list in §3).
- **Employee details** layout: tabs vs single page; **Finance** block structure once salaries / dues / payments are defined.
- Any data **hidden** from certain admin roles on the employee details page.
- **Tasks, dues, payments, and salaries** — business rules and UI detail **deferred** to a later discussion.

---

## 7) TBD tracker *(fill as we discover gaps)*

Use this section to track anything not yet specified. Check off or move to body text when decided.

### Form fields — create employee

- [ ] **TBD** — Full field list (beyond name, phone, email, password, address, role): e.g. joining date, employee code, emergency contact, bank details, ID documents, photo.  
- [ ] **TBD** — Mandatory vs optional per field.  
- [ ] **TBD** — Default values (e.g. role, status).  
- [ ] **TBD** — Password rules (length, complexity, reset flow on admin side).  
- [ ] **TBD** — Duplicate checks (same phone / email).  

### Form fields — edit / profile

- [ ] **TBD** — Which fields editable after create; which need approval or are admin-only.  
- [ ] **TBD** — Document uploads (types, size limits, mandatory docs).  
- [ ] **TBD** — Employment status values (active, suspended, exited, …).  

### Validations

- [ ] **TBD** — Phone / email format and uniqueness rules.  
- [ ] **TBD** — Address required or optional.  
- [ ] **TBD** — Role must be from master list; any role restrictions by creator.  
- [ ] **TBD** — Blocking rules (e.g. cannot delete employee with open payroll).  

### Listing page

- [ ] **TBD** — Columns to show; default sort.  
- [ ] **TBD** — Filters (role, status, site, date joined, …).  
- [ ] **TBD** — Search fields (name, phone, code, …).  
- [ ] **TBD** — Bulk actions (if any).  
- [ ] **TBD** — Pagination / export.  

### Employee details page (blocks)

- [ ] **TBD** — Layout: tabs vs sections; order of blocks.  
- [ ] **TBD** — Attendance summary: default period; drill-through to full attendance.  
- [ ] **TBD** — Finance block: definition of dues; tabs for salary / advance / loan to company.  
- [ ] **TBD** — Tasks: filters (open only vs history); link to project.  
- [ ] **TBD** — Expenses: pending vs approved visibility by role.  
- [ ] **TBD** — Optional blocks: tools issued, site deployment, documents gallery.  

### Permissions & visibility

- [ ] **TBD** — Which admin roles can create / edit / view employees.  
- [ ] **TBD** — Field-level or block-level hide for sensitive data (salary, bank).  
- [ ] **TBD** — Who can reset password or unlock account.  

### Lifecycle & status

- [ ] **TBD** — Exited / inactive employees: list visibility; data retention.  
- [ ] **TBD** — Rehire or duplicate person policy.  

### Cross-feature & integrations

- [ ] **TBD** — Payroll posting to Finance (timing, accounts).  
- [ ] **TBD** — Attendance → payroll calculation rules.  
- [ ] **TBD** — Employee app: what employee can self-edit vs read-only.  
- [ ] **TBD** — Notifications (e.g. payroll paid, task assigned).  

### Audit & compliance

- [ ] **TBD** — Audit log fields (who changed what, when).  
- [ ] **TBD** — Export / reports for statutory needs (if any).  

### Edge cases

- [ ] **TBD** — Same phone shared across family / wrong entry handling.  
- [ ] **TBD** — Mid-month join; pro-rata rules (with payroll TBD).  
