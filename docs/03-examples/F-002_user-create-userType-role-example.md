# F-002 Example - Create User with User Type and Role

## Scenario

Create an employee user with the Site Supervisor role.

## Input

- User type selected: Employee
- Role selected: Site Supervisor
- Name: Ravi Kumar
- Email: ravi@example.com

## Expected System Behavior

- System validates user type and role.
- System verifies role belongs to Employee user type.
- System creates user and stores mapped references.

## Expected Result

- User is saved successfully.
- User appears in user list with:
  - User Type: Employee
  - Role: Site Supervisor

## Invalid Scenario

If user type is Employee and role is CEO, creation should fail with a validation error.
