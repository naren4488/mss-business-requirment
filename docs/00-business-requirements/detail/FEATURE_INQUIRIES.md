# Feature — Inquiries / Leads (detailed BRD)

**Scope:** First contact from a potential client — track **source**, **priority**, **ownership**, **follow-up**, and **status** until the lead is **won (converted)**, **lost**, or still **in pipeline**. Managed in the **admin** product. **Quotation** creation from an inquiry is referenced here; **quotation rules** are in the **Quotations** feature later.

## 1) Purpose

- Capture every **lead** (social media, referral, agent, salesperson, walk-in, website, phone, etc.).
- Run a **listing** with **filters** and **stats** for pipeline visibility.
- Open an **inquiry details** page for full history: edits, status, assignee, meetings, notes, and (when allowed) **create quotation**.

## 2) Status values (initial)

Track each inquiry through its lifecycle until closed out:

| Status (working name) | Meaning |
|----------------------|---------|
| **New** | Just captured; not yet worked or default entry. |
| **In progress** | Actively being worked (calls, visits, quotes in draft, etc.). |
| **Converted** | Won — typically aligned to customer + deal / project / quotation accepted *(exact link TBD with Customers & Projects)*. |
| **Lost** | Closed without conversion. |

> **TBD** — Whether “completed” is the same as **Converted** / **Lost** or a separate terminal state.

## 3) Create inquiry — fields

### Mandatory

- **Customer name**  
- **Phone number**  
- **Type of inquiry** — e.g. **Individual** vs **Company** *(exact labels in UI TBD)*  
- **Source** — how the lead arrived (see §4)  
- **Priority** — level for triage *(values from master list TBD)*  

### Optional

- **Email**  
- **Address**  
- **System capacity** (e.g. kW interest)  
- **Estimated budget**  
- **Notes** (initial free-text)  
- **Follow-up date** — next action (call, visit, prep) for tracking  

## 4) Source (mandatory pick list — initial examples)

Examples the business uses (full master list **TBD**):

- Phone call  
- Website  
- Referral *(person’s referral — link to referrer **TBD**)*  
- Walk-in  
- Social media  
- Other  

> **TBD** — Optional link to **Agent** when source is agent-led (aligned with **Agents** feature). Optional link to **internal salesperson** as source vs **assignee** (see §6).

## 5) Screens

### Inquiries listing

- Table or list of all inquiries.  
- **Filters** — *which dimensions TBD* (status, source, priority, assignee, date range, follow-up due, type, …).  
- **Stats** — *definitions TBD* (e.g. count by status, new this week, follow-ups due today).  

### Inquiry details page

- Full view of one inquiry: all fields, current **status**, **assignee**, **meetings**, **notes**, actions (**edit**, **change status**, **assign**, **schedule meeting**, **create quotation** when allowed).  

## 6) Actions after creation

- **Edit** — update fields (rules for editing after converted **TBD**).  
- **Change status** — among allowed values (e.g. New → In progress → Converted / Lost).  
- **Assign** — assign inquiry to a responsible person; link to **employee** (or internal user id — **TBD** exact entity: “employee ID” as stated).  
- **Schedule meeting** — **calendar date** + **note** for that meeting.  
- **Notes** — ability to **keep adding notes** over time *(timeline / author / timestamp **TBD**)*.  
- **Create quotation** — from inquiry when it is **not Lost**; can be done from other statuses (New, In progress, Converted — **TBD** if Converted still allows new quote or only from earlier states). **Quotation content** — **Quotations** feature.  

## 7) Business rules (initial)

- **Customer name** and **phone** are always required on create.  
- **Type**, **source**, and **priority** are required on create.  
- All other fields listed are optional unless you extend the rule later.  
- **Lost** inquiries: **TBD** — block quotation only, or block other actions too.  

## 8) Dependencies

- **Employees** (or user directory) for **assignee**.  
- **Quotations** (action from inquiry).  
- **Customers / Projects** when status becomes **Converted** *(flow TBD)*.  
- **Agents** *(optional attribution on inquiry — TBD)*.  
- **Masters** for source, priority, inquiry type.  

---

## 9) TBD tracker *(fill as we discover gaps)*

### Form fields — create / edit

- [ ] **TBD** — Final labels for **type** (Individual / Company / more).  
- [ ] **TBD** — Priority levels and default.  
- [ ] **TBD** — Full **source** master list + “Other” free text or not.  
- [ ] **TBD** — Optional: **agent** reference, **campaign**, **UTM**, **location** fields.  
- [ ] **TBD** — Duplicate detection (same phone / name).  

### Validations

- [ ] **TBD** — Phone format (India / international).  
- [ ] **TBD** — Email format when provided.  
- [ ] **TBD** — Follow-up date cannot be in past on create, or allowed.  
- [ ] **TBD** — System capacity and budget units and max values.  
- [ ] **TBD** — Required fields on **edit** (can phone be cleared?).  

### Listing & stats

- [ ] **TBD** — Default sort; columns on list.  
- [ ] **TBD** — Stat cards: exact KPIs and date ranges.  
- [ ] **TBD** — Saved views or quick filters (“My inquiries”, “Due today”).  

### Assignee

- [ ] **TBD** — Only **employee-type** users or any admin-type with sales role.  
- [ ] **TBD** — Reassignment audit; notify assignee.  
- [ ] **TBD** — Unassigned bucket and permissions.  

### Meetings

- [ ] **TBD** — One meeting per row vs multiple meetings (history).  
- [ ] **TBD** — Time of day or date-only.  
- [ ] **TBD** — Reminder / calendar integration.  

### Notes

- [ ] **TBD** — Threaded notes vs single stream; rich text or plain.  
- [ ] **TBD** — Who can delete or edit a note.  

### Status & quotation

- [ ] **TBD** — Allowed status transitions (diagram).  
- [ ] **TBD** — **Converted**: auto-create customer? link to project? manual only?  
- [ ] **TBD** — **Create quotation** visible for which statuses; multiple quotes per inquiry?  
- [ ] **TBD** — Edit inquiry after **Converted** or **Lost**.  

### Permissions

- [ ] **TBD** — Who can create / edit / change status / assign / see all vs own inquiries.  
- [ ] **TBD** — Delete inquiry vs archive.  

### Audit & compliance

- [ ] **TBD** — Full activity log (field-level vs event-level).  
- [ ] **TBD** — Export list for reporting.  

### Edge cases

- [ ] **TBD** — Same person multiple inquiries (new project vs reopen).  
- [ ] **TBD** — Inquiry without quotation path (direct project) — how recorded.  
