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
4. Apply for subsidy type(s) as per eligibility:
   - Central subsidy
   - State subsidy
   - Both Central and State subsidy (if allowed by policy)

### Step 3: Loan-Based Flow

If the project is in loan mode:

1. Login
2. Apply for loan
3. Process vendorship
4. Complete site installation
5. Start subsidy process
6. Apply for subsidy as per eligibility (Central, State, or both Central and State where allowed)
7. Prepare and submit file with bank

### Step 4: Bank File Purpose and Document Sequence

For bank file submission, follow this order:

1. PM Surya app form
2. Subsidy details/form
3. Feasibility report
4. Required customer documents

### Required Customer Documents for Bank File

These documents are applicable in both payment modes:
- Cash case
- Loan case

- PAN Card
- Aadhaar Card
- Passbook (bank passbook copy)
- Electricity Bill (latest 6 months copy)

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
