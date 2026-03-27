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
5. Loan File Book (client signature and first installment details for loan cases)

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
