# MSS Business Requirement Docs

This repository contains planning and business requirements for the solar business (admin product and related scope).

## Documentation principles

- Business-first: capture what the business needs and why.
- Keep the working BRD lean; longer feature notes live beside it with clear links.
- Iterate: documents grow as requirements are discussed.

## Folder structure

All documentation lives under **`docs/00-business-requirements/`**:

| Path | Purpose |
|------|---------|
| `MASTER_BUSINESS_REQUIREMENTS.md` | Large consolidated business requirements reference (legacy / full capture). |
| `MASTER_BUSINESS_REQUIREMENTS_BUILD.md` | Step-by-step working BRD: platform context, end-to-end flow, feature index with links. |
| `detail/` | Per-feature detailed BRD files (e.g. employees, agents, inquiries, quotations, presets) plus TBD trackers. |

Add new feature specs as `detail/FEATURE_<NAME>.md` and link them from `MASTER_BUSINESS_REQUIREMENTS_BUILD.md`.

## Working method

1. Extend **`MASTER_BUSINESS_REQUIREMENTS_BUILD.md`** with short summaries and links.
2. Put depth, field lists, rules, and **TBD** checklists in **`detail/`** feature files.
3. Update **`MASTER_BUSINESS_REQUIREMENTS.md`** when you want a single long-form snapshot of the same content.
