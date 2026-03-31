# Platform context — admin app vs employee app

## Two products

- **Admin project (this BRD):** Web or app used by the business to run operations — sales, projects, inventory, finance, HR configuration, etc.
- **Employee project (separate codebase):** Dedicated experience for people who work in the field or on tasks — not the same application as the admin side.

## Who is created where

- **All users** (admin type and employee type) are **created and maintained from the admin project**.
- Credentials, roles, and profile linkage for the employee app are administered from here.

## User types (high level)

Each **real person** has **exactly one** user type: **admin** or **employee** — **not both** on the same account.

1. **Employee type** — may access **only** the **employee** panel (field / task experience). Master record and HR data are still owned and edited from the **admin** product by staff.
2. **Admin type** — may access the **admin** panel (access level depends on admin-side role). They may also access the **employee** panel when the product allows it, so **admin-type users can use both panels**; **employee-type users cannot** use the admin panel.

## Roles on the admin side (examples)

Same product, different permission levels. Examples discussed:

- Super Admin, Admin, CEO, Manager, Accountant, Site Supervisor *(and similar — list is extensible).*

## Roles on the employee side (examples)

Used in the **employee** app. Examples discussed:

- Site Supervisor, Installation worker, Civil worker, Welder, *(and similar — list is extensible).*

> **Note:** The same **job title** may appear as a **role** name on admin side and on employee side; **which panels** a person can open follows **only** their **user type** (employee → employee panel only; admin → admin panel, and employee panel when enabled).

## Open points (for later)

*(Many are expanded as checkboxes in **TBD tracker** below.)*

- Mapping table: admin-side **role** → permissions on admin panel vs entry to employee panel (if not all admin roles get employee access).
- Default landing after login for admin type.
- Whether **creation** of employees should later be restricted to certain admin roles only *(current rule: any admin-type user — see Employees feature doc)*.

---

## TBD tracker *(platform / access — gaps to close)*

### Authentication & sessions

- [ ] **TBD** — Same identity provider for admin and employee apps or separate; SSO between panels for admin type.  
- [ ] **TBD** — Password reset / forgot password (per app).  
- [ ] **TBD** — Session timeout; force logout; device limit.  
- [ ] **TBD** — First admin bootstrap process (already high-level in master BRD).  

### Admin vs employee panel access

- [ ] **TBD** — Matrix: admin **role** → can open employee panel (yes/no).  
- [ ] **TBD** — Default home after login for each role (admin app vs employee app).  
- [ ] **TBD** — Deep link from admin to “view as employee” or separate login.  

### Roles & masters

- [ ] **TBD** — Canonical list of admin-side roles vs employee-side roles (master data).  
- [ ] **TBD** — Who can create admin-type users vs only employee-type.  

### Security & compliance

- [ ] **TBD** — Data residency / PII handling between two apps.  
- [ ] **TBD** — Audit: user type and role changes.  

### Edge cases

- [ ] **TBD** — Account recovery if email/phone lost.  
- [ ] **TBD** — Merging duplicate person records (if ever needed).  
