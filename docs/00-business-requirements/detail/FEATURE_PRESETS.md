# Feature — Presets (detailed BRD)

**Scope:** Reusable **templates** that speed up repeated work. **Not** the same as a single quotation or project record — presets are **definitions** you **load** into flows or **save** from them.

This feature is **separate** from **Quotations** but **connected**: quotation screens can **create**, **update**, or **apply** a **quotation preset**.

## 1) Purpose

- Store reusable bundles so users avoid re-entering the same **system configuration** and **item lists** (and similar data) many times.  
- Support **multiple preset kinds** over time; only some exist in early releases.

## 2) Preset types *(roadmap)*

| Type | Purpose | Where used *(examples)* |
|------|---------|-------------------------|
| **Quotation preset** | Saved **system configuration** + **material / line items** (and related defaults) for sales quotations. | **New quotation** — load preset; **from quotation** — save as preset. |
| **Inventory / BOM preset for project** | Standard material bundle matched to a system size or segment *(e.g. residential 3 kW)*. | Project planning, issue to site, invoice/inventory matching *(align with inventory module — TBD)*. |
| **Task preset** | Standard task checklist or pack for a project phase. | Project / installation planning *(TBD)*. |

> **v1 focus:** **Quotation preset** is the first type to specify in depth; others are **placeholders** until those modules are discussed.

## 3) Quotation preset — business behaviour

- **Create** a preset from a quotation’s **system block + items** *(exact fields snapshotted TBD)*.  
- **Load** a preset when starting a **new quotation** — user can still edit after load.  
- **Name / segment / metadata** for presets *(e.g. Residential 3 kW — TBD)*.  
- **List / search / edit / delete or deactivate** presets *(policy TBD)*.  

Technical **APIs or services** that power create/load are **implementation** — tracked as **TBD** for engineers, not specified here.

## 4) Dependencies

- **Quotations** (`FEATURE_QUOTATIONS.md`) for quotation-linked create/load.  
- **Inventory / Projects / Tasks** when non-quotation preset types are built.  
- **Masters** (categories, units, segments) as needed.  

---

## 5) TBD tracker

### Quotation presets

- [ ] **TBD** — Fields included in snapshot vs live link to materials master.  
- [ ] **TBD** — One preset per segment vs many; tagging (Residential / Commercial / Industrial).  
- [ ] **TBD** — Pricing in preset: fixed amounts vs “template only” rates.  
- [ ] **TBD** — Permissions: who can create / publish preset.  
- [ ] **TBD** — Versioning when master items change.  

### Inventory / project presets *(later)*

- [ ] **TBD** — Relationship to **Presets** in inventory UI (existing product names).  
- [ ] **TBD** — Sync with quotation preset or separate only.  

### Task presets *(later)*

- [ ] **TBD** — Granularity (per project type vs per kW band).  

### General

- [ ] **TBD** — Duplicate preset; import/export.  
- [ ] **TBD** — Audit log on preset change.  
