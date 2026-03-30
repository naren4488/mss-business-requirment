# F-002 User Type and Role Management

## Business Objective

Establish a clear user hierarchy so all system users are organized by type and role for proper access control, accountability, and operations management.

## User/Stakeholder Flow

1. Admin creates or updates user type definitions (Admin, Employee).
2. Admin defines roles under each user type.
3. Admin creates users by selecting user type first.
4. Admin assigns role from the selected user type.
5. User record is saved with user type + role mapping.

## Scope

- In scope:
  - User type definition (Admin, Employee)
  - Role definition under each user type
  - User creation based on user type and role
  - Role updates for existing users
- Out of scope:
  - Detailed permission matrix per role (to be handled in a future feature)

## Functional Requirements

- System should support user type as a primary classification.
- System should support multiple roles under each user type.
- A user cannot be created without user type and role.
- Role options shown during user creation should depend on selected user type.
- System should allow adding new roles in the future for both user types.

## Initial Role Setup

- Admin type roles:
  - Super Admin
  - Admin
  - CEO
  - Manager *(future scope)*
- Employee type roles:
  - Site Supervisor
  - Welder
  - Civil Worker
  - Technician *(future scope)*

## Non-Functional Expectations

- Role selection should be simple and error-resistant.
- User data should remain consistent even when role names are updated.
- Auditability should be maintained for user role changes.

## Acceptance Criteria

- [ ] User type list includes Admin and Employee.
- [ ] Admin roles include Super Admin, Admin, and CEO (Manager when in scope).
- [ ] Employee roles include Site Supervisor, Welder, and Civil Worker.
- [ ] User creation requires both user type and role.
- [ ] Role dropdown updates based on chosen user type.

## Dependencies

- Core user management module
- Master data setup for role configuration

## Open Questions

- Should one user be allowed to hold multiple roles in future phases?
- Should inactive roles be hidden or selectable for historical users?
