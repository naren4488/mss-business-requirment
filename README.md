# MSS Business Requirement Docs

This repository contains end-to-end planning and documentation for the solar business.

## Documentation Principles

- Business-first clarity: capture what the business needs and why.
- Separation of concerns: keep pure business requirements separate from engineering details.
- Traceability: every feature should connect business goals to UI, backend, data, and API design.
- Iterative updates: docs are living artifacts and should evolve with each requirement discussion.

## Folder Structure

- `docs/00-business-requirements/` - master business requirements (non-technical)
- `docs/01-product-breakdown/` - feature-wise product behavior and acceptance criteria
- `docs/02-engineering/` - implementation-oriented docs (UI, backend, API, data)
- `docs/03-examples/` - examples, sample flows, sample payloads, and mock scenarios
- `docs/04-decisions/` - architecture and product decisions, assumptions, and trade-offs
- `docs/99-templates/` - reusable templates for adding new docs quickly

## Working Method

1. We add or update business requirements in the master business document.
2. We break each requirement into feature docs with clear scope.
3. We maintain engineering docs separately for UI/backend/API/data details.
4. We add examples for complex flows and edge cases.
