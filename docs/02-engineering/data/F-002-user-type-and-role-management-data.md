# F-002 Data Details - User Type and Role Management

## Entities

- UserType
- Role
- User

## Suggested Fields

### UserType

- `id`
- `code` (example: ADMIN, EMPLOYEE)
- `name`
- `isActive`

### Role

- `id`
- `userTypeId` (FK to UserType)
- `code` (example: CEO, SITE_SUPERVISOR)
- `name`
- `isActive`

### User

- `id`
- `name`
- `email`
- `userTypeId` (FK)
- `roleId` (FK)
- `status`
- `createdAt`
- `updatedAt`

## Constraints

- Each role must belong to one user type.
- Each user must have exactly one user type and one role.
- `role.userTypeId` must match `user.userTypeId` during assignment.

## Reporting Impact

- Total users by user type
- Total users by role
- Active/inactive distribution across roles
