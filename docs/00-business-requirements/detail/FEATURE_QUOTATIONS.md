# Feature — Quotations (sales) (detailed BRD)

**Scope:** Formal **proposal document** for the customer: scope of work, **system configuration** (where applicable), **line items**, **pricing**, **subsidies**, **payment terms**, **warranty**, and **notes**. **Preview** and **PDF export** can **hide sections** without removing data from the form.  

**Out of scope here:** **Procurement / vendor requirement quotations** (RFQ to suppliers) — *separate discussion later*.  

**Related feature:** **Presets** (templates) — `FEATURE_PRESETS.md`. Quotation UI can **load** or **save** a quotation preset; preset types beyond quotation are defined there.

## 1) Purpose

- Produce a shareable **quotation** for **Solar** or **Other** (non-solar / minor works) sales.  
- Track **lifecycle** from draft work through **saved**, **shared**, **client decision**, and **project creation** when approved.  
- Support **listing** and **detail** views for operations.

## 2) Quotation types (sales)

| Type | Use | Content depth |
|------|-----|----------------|
| **Solar** | Rooftop / solar system sale | Full **client** block, **system configuration**, **items**, subsidies, payment terms, warranty, notes. |
| **Other** | e.g. staircase, small civil, other services | **Client** info, **title**, **description**, **items** (category, name, spec, qty, rate, total); **no** heavy solar system block. |

## 3) Document blocks — overview *(final field list TBD)*

### Client information

- Identity and contact for the proposal *(fields TBD; align with **Customers** when linked)*.

### System configuration *(Solar type — primary)*

- **Capacity** (kW)  
- **Panels:** type / wattage, **count**, brand as needed  
- **Inverter:** brand, **capacity**  
- **Structure** type  
- **Floors** / level (e.g. first floor, second floor)  
- **Category** (project or system category — *master TBD*)  
- **System notes**  

### Line items *(both types, structure may differ slightly)*

Each item may include:

- **Category**  
- **Item name**  
- **Size / specification** *(optional)*  
- **Quantity**  
- **Rate**  
- **Line total**  

Line items drive **price breakdown**.

### Price breakdown

- Subtotals as designed  
- **Discount** *(field(s) TBD)*  
- **GST** *(rates, split TBD)*  
- **Net / effective pricing**  

### Subsidy *(Solar — when applicable)*

- **Central subsidy** amount (e.g. ₹78,000 — illustrative)  
- **State subsidy** amount (e.g. Rajasthan ₹17,000 — illustrative)  
- **Effective price** to customer after subsidies *(definition TBD: before/after GST, etc.)*  

### Payment terms

- Milestones such as: **booking**, **design approval**, **before material**, **post-installation** — each with **percentage** or amount *(rules TBD)*.

### Warranty

- **Panel** warranty  
- **Inverter** warranty  
- **Structure** warranty  
- **Overall project** warranty  
- Wording / duration fields **TBD**.

### Additional notes

- Free-text **TBD** limits.

## 4) Preview and PDF export — visibility toggles

- The **form** holds **all** captured data.  
- For **preview** and **export (PDF)**, admin can **show/hide** sections, for example:  
  - System details  
  - Items  
  - Amounts / breakdown  
  - Warranty  
  - Terms and conditions  
  - Payment terms  
  - *(other blocks as product evolves)*  
- Exact toggle list and defaults **TBD**.

## 5) Persistence and status — business flow

- While the user is **editing without persisting**, the business treats the quotation as **Draft** (work in progress). **Where** unsaved data lives until save is an **implementation decision** — *TBD*.  
- **Save** → quotation is **stored** (backend / durable store); status reflects **saved** (exact label **TBD**).  
- **Shared to client** — **manual** action by admin (no automation in v1):  
  - Mark as shared.  
  - Record **how** it was shared: e.g. **WhatsApp (PDF)**, **Email**, **Print / handover**, **Other** *(pick list TBD)*.  
- After shared: client **approves** or **rejects** *(how captured in system TBD — manual update vs link)*.  
- **Approved** → business may **create a project** from the quotation *(flow with **Projects** feature TBD)*.  

> **TBD** — Exact status names, whether **Rejected** can become **revised** new version, expiry of quotation.

## 6) Creation sources

- From **inquiry** *(when inquiry is not Lost — see `FEATURE_INQUIRIES.md`)*.  
- **Direct** quotation without inquiry *(if allowed — TBD)*.  
- **Load preset** when creating *(see `FEATURE_PRESETS.md`)*.  

## 7) Presets (cross-feature)

- **Save** current solar configuration + item set as a **quotation preset**, or **load** preset into a new quotation — **Preset** feature owns definitions; quotation **triggers** those actions.  

## 8) Screens

### Listing

- Columns *(initial expectation):* **Quotation ID**, **type** (Solar / Other), **client name**, **phone**, **system amount** *(or total — label for Other TBD)*, **date**, **status**, **actions**.  
- **Filters / stats** — *TBD*.  

### Detail

- Full quotation view/edit, preview, export, share marking, status updates, link to **project** when approved.  

## 9) Dependencies

- **Customers** / client master *(linkage TBD)*.  
- **Inquiries** (optional source).  
- **Projects** (on approval).  
- **Presets** (`FEATURE_PRESETS.md`).  
- **GST / tax masters** *(TBD)*.  
- **Procurement quotations** — *not this document*.  

---

## 10) TBD tracker *(fill as we discover gaps)*

### Fields & validation

- [ ] **TBD** — Complete field list for Solar vs Other; mandatory vs optional per type.  
- [ ] **TBD** — Client: new inline vs pick existing customer.  
- [ ] **TBD** — Numeric validation (qty, rates, percentages for payment terms).  
- [ ] **TBD** — Multiple GST slabs on one quotation.  
- [ ] **TBD** — Discount approval rules (if amount > threshold).  
- [ ] **TBD** — Quotation number / ID generation and uniqueness.  
- [ ] **TBD** — Validity / expiry date on quotation.  

### Pricing & subsidy

- [ ] **TBD** — Formula for **effective price** (order of GST, discount, subsidy).  
- [ ] **TBD** — Subsidy “TBC” or zero when unknown.  
- [ ] **TBD** — Other type: hide subsidy block entirely.  

### Status & versioning

- [ ] **TBD** — Status enum and allowed transitions.  
- [ ] **TBD** — Edit after **Shared** or **Approved**; versioning / revision letter.  
- [ ] **TBD** — Draft autosave vs explicit save.  

### Share & client response

- [ ] **TBD** — Full channel list for “how shared”.  
- [ ] **TBD** — Who can mark shared; audit trail.  
- [ ] **TBD** — Client approve/reject: manual only v1? evidence upload?  

### Preview / PDF

- [ ] **TBD** — Default visibility set per type (Solar vs Other).  
- [ ] **TBD** — Company letterhead, signatures, terms PDF attachment.  
- [ ] **TBD** — Watermark for “Draft” on preview.  

### Permissions

- [ ] **TBD** — Who can create / edit / approve internally / mark shared.  
- [ ] **TBD** — Delete vs void cancelled quotations.  

### Listing & reporting

- [ ] **TBD** — “System amount” vs total for Other quotations.  
- [ ] **TBD** — Export list; conversion rate reports.  

### Edge cases

- [ ] **TBD** — Quotation without inquiry then customer duplicates inquiry.  
- [ ] **TBD** — Change customer on saved quotation.  
- [ ] **TBD** — Multi-currency *(if ever)*.  

### Procurement (separate feature later)

- [ ] **TBD** — RFQ to vendors — document when scoped.  
