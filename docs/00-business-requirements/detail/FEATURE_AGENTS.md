# Feature — Agents (detailed BRD)

**Scope:** External parties who **bring projects** (business) to the company and earn **commission**. Maintained in the **admin** product. **How commission attaches when a project is created** is defined with the **Projects** feature later.

## 1) Purpose

- Register and manage **agents**.
- Support **different commission models** so payout can follow agreement (per capacity, per file, etc.).
- Track **earned commission vs paid vs pending** per agent, including **overpayment** (negative balance / advance to agent).

## 2) What an agent is (business)

- Not an employee; brings leads or deals that become **projects**.
- Commission is agreed per agent using rules below.

## 3) Commission models (initial)

The business needs at least these patterns (exact formulas and masters TBD):

| Type (working name) | Meaning | Example |
|---------------------|---------|---------|
| **Per kW** | Commission scales with **project system capacity** (kW). | 3 kW → ₹3,000; 5 kW → ₹5,000 *(e.g. ₹1,000 per kW)* |
| **Per file / per project** | **Flat amount per linked project** (or “file”), **independent of kW**. | ₹1,000 per project regardless of size |

> Other variants (e.g. **fixed amount for a specific capacity band**, slabs, or hybrids) can be added when you define them.

**Agent master** should store enough to know **which model applies** and the **rates** (e.g. commission **rate type**, **amount per kW**, **flat per file**, etc.).

## 4) Agent master data (admin — create / edit)

**Typical fields** (final mandatory set TBD):

- Photo  
- Name  
- Phone  
- Email  
- Address  
- **Commission configuration:** e.g. **rate type** (per kW vs per file, …), **rate per kW** where relevant, **flat per file** where relevant  

**Operations:** full **CRUD** (create, read, update, delete or deactivate — policy TBD for delete vs inactive).

## 5) Per-agent view (summary + detail)

For each agent, the business needs visibility of:

- **Projects** linked to that agent (list; count of projects done / in progress — definitions TBD).  
- **Total commission earned** (accrued from linked projects, per agreed rules).  
- **Total paid** to the agent (commission payouts recorded).  
- **Pending** = earned minus paid (or equivalent business definition).  
- **Overpayment:** if paid **more** than owed, show **negative** pending / **dues** (agent owes back or it is carried as advance — accounting treatment TBD).

## 6) Link to projects

- An agent is **associated when creating a project** (and possibly edited later — rules TBD).  
- **Project creation flow** (when to pick agent, how commission is calculated and frozen) — **deferred** to the **Projects** feature discussion.

## 7) Dependencies

- **Projects** (linkage, capacity for per-kW commission).  
- **Finance / payouts** (where commission payments are posted — align with Transactions or a dedicated agent payout flow TBD).

## 8) Open questions

*(Also listed as TBD items in §9 where applicable.)*

- **Delete vs inactive** for agents with historical projects.  
- Whether commission is **locked at project creation** or **recalculates** if kW changes.  
- **Payment** workflow: who records payout, approval, and link to bank/cash.  
- Slab / tier pricing beyond per-kW linear and flat-per-file.

---

## 9) TBD tracker *(fill as we discover gaps)*

### Form fields — create / edit agent

- [ ] **TBD** — Complete master field list (photo, name, phone, email, address, commission fields — any more: PAN, GST, bank for payout, agreement date, referral code).  
- [ ] **TBD** — Mandatory vs optional per field.  
- [ ] **TBD** — Commission UI when **multiple models** or **overrides per project** are allowed.  
- [ ] **TBD** — Effective dates for rate changes (new projects only vs retroactive).  

### Validations

- [ ] **TBD** — Phone / email format; uniqueness (same agent twice).  
- [ ] **TBD** — Numeric rules: rate per kW ≥ 0; flat per file ≥ 0; max caps.  
- [ ] **TBD** — Required commission type when saving agent.  
- [ ] **TBD** — Cannot delete agent with linked projects (or force inactive only).  

### Listing page

- [ ] **TBD** — Columns; sort; filters (active only, by region, …).  
- [ ] **TBD** — Search fields.  
- [ ] **TBD** — Summary cards (total agents, total pending commission — if shown here).  

### Per-agent detail view

- [ ] **TBD** — Project list columns; status filter (won, lost, in progress).  
- [ ] **TBD** — How **project count** is defined (all time vs financial year).  
- [ ] **TBD** — Earned vs paid: calculation timing (on project complete vs invoice paid).  
- [ ] **TBD** — Statement or ledger view for agent (export PDF/Excel).  
- [ ] **TBD** — Negative balance label and next-step workflow (adjustment, carry forward).  

### Commission calculation

- [ ] **TBD** — Rounding rules (per project, per payment).  
- [ ] **TBD** — Partial kW or change order after commission set.  
- [ ] **TBD** — Multiple agents on one project (split %) — if ever allowed.  
- [ ] **TBD** — Currency and tax on commission (TDS, GST on services) — if applicable.  

### Payments to agents

- [ ] **TBD** — Who can record payout; approvals.  
- [ ] **TBD** — Link to Finance (expense category, bank / cash).  
- [ ] **TBD** — Partial payouts; advance to agent before project close.  

### Permissions

- [ ] **TBD** — Which admin roles CRUD agents vs view-only vs payout-only.  

### Link to projects

- [ ] **TBD** — Optional vs mandatory agent on project.  
- [ ] **TBD** — Change agent after project created; effect on earned commission.  
- [ ] **TBD** — Agent on enquiry only vs project only vs both — **Projects** feature.  

### Audit & compliance

- [ ] **TBD** — Audit trail on rate changes and payouts.  
- [ ] **TBD** — Agreement document storage per agent.  

### Edge cases

- [ ] **TBD** — Agent exits mid-project.  
- [ ] **TBD** — Dispute on commission amount.  
