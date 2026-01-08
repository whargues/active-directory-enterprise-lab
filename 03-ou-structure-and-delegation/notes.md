# OU Structure & Delegated Administration — Notes

## 1. Review Default OU Layout
- Opened Active Directory Users and Computers (ADUC)
- Reviewed default containers: Users, Computers, Domain Controllers, Builtin, etc.
- Screenshot: `screenshots/default-ou-layout.png`

## 2. Create Departmental OU Structure
- Created top-level OU: `Departments`
- Added sub-OUs for each department (e.g., IT, HR, Finance, Sales)
- Created `Users` and `Groups` sub-OUs inside each department
- Screenshot: `screenshots/departments-ou-structure.png`

## 3. Create Department Admin Groups
- Created security groups for delegated admins (e.g., IT-Admins, HR-Admins)
- Placed these groups inside each department’s `Groups` OU
- Screenshot: `screenshots/department-admin-groups.png`

## 4. Delegate Control to Department Admin Groups
- Used “Delegate Control” wizard in ADUC
- Assigned permissions such as:
  - Reset passwords
  - Create/delete/manage users
  - Read/write attributes
- Delegated at the department OU level
- Screenshot: `screenshots/delegation-wizard.png`

## 5. Create Users and Add Them to Groups
- Created sample users inside each department’s `Users` OU
- Added users to:
  - Department security groups
  - Department admin groups (where appropriate)
- Screenshot: `screenshots/user-added-to-group.png`

## 6. Validate Delegation
- Logged in as a delegated admin (optional)
- Verified ability to manage only their department’s users
- Screenshot: `screenshots/delegation-validation.png`
