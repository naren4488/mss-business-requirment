# F-002 UI Details - User Type and Role Management

## Pages/Screens Involved

- User List Page
- Create User Page
- Edit User Page
- Role Master Page (optional admin config screen)

## UI Components

- User Type selector (Admin, Employee)
- Role selector (dynamic based on selected user type)
- User form fields (name, contact, status, etc.)
- Role chips/badges in user list

## Interaction Logic

- User selects user type first.
- Role selector loads only the roles for that selected type.
- If user type changes, role field resets and requires fresh selection.

## Validation Rules

- User type is mandatory.
- Role is mandatory.
- Role must belong to selected user type.

## States

- Loading state while fetching role list
- Empty state if no roles configured for selected type
- Error state if roles fail to load
- Disabled submit until required fields are valid
