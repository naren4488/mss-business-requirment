# F-002 Backend Details - User Type and Role Management

## Core Services

- UserTypeService
- RoleService
- UserService

## Business Logic Flow

1. Validate incoming user type.
2. Validate selected role exists and belongs to user type.
3. Create or update user with user type and role references.
4. Record audit event for user role changes.

## Rules Enforcement

- Reject user creation if user type is missing.
- Reject user creation if role is missing.
- Reject user creation if role does not map to selected user type.

## Future Extensibility

- Support role activation/inactivation.
- Support additional role categories under each user type.
- Keep role mapping logic centralized for maintainability.
