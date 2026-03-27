# F-002 API Details - User Type and Role Management

## Suggested Endpoints

- `GET /user-types`
- `GET /roles?userType={userType}`
- `POST /users`
- `PUT /users/{id}`

## Example Request - Create User

```json
{
  "name": "Ravi Kumar",
  "email": "ravi@example.com",
  "userType": "EMPLOYEE",
  "roleCode": "SITE_SUPERVISOR"
}
```

## Example Success Response

```json
{
  "id": "USR-1023",
  "name": "Ravi Kumar",
  "userType": "EMPLOYEE",
  "roleCode": "SITE_SUPERVISOR",
  "status": "ACTIVE"
}
```

## Example Validation Error

```json
{
  "errorCode": "INVALID_ROLE_FOR_USER_TYPE",
  "message": "Role does not belong to selected user type."
}
```

## API Rules

- `userType` is required.
- `roleCode` is required.
- `roleCode` must be valid for provided `userType`.
