# OU Structure & Delegated Administration — Notes

## Review Default OU Layout
- Opened Active Directory Users and Computers (ADUC)
- Reviewed default containers: Users, Computers, Domain Controllers, Builtin, etc.
- Screenshot: `screenshots/default-ou-layout.png`

## Create Departmental OU Structure
- Created top-level OU: `Departments`
- Added sub-OUs for each department (e.g., IT, HR, Finance, Sales)
- Created `Users` and `Groups` sub-OUs inside each department
- Screenshot: `screenshots/departments-ou-structure.png`

## Create Department Admin Groups
- Created security groups for delegated admins
- Placed these groups inside each department’s `Groups` OU
- Screenshot: `screenshots/department-admin-groups-creation.png`
- Confirmed Creation was successful
- Screenshot: `screenshots/department-admin-groups-creation-successful.png`

## Delegate Control to Department Admin Groups
- Used “Delegate Control” wizard in ADUC
- Assigned permissions such as:
  - Reset passwords
  - Create/delete/manage users
  - Read/write attributes
- Delegated at the department OU level
- Screenshot: `screenshots/delegation-wizard-part1.png`
- Confirmed Delegation was successful
- Screenshot: `screenshots/delegation-wizard-part2.png`

## Create Users and Add Them to Groups
- Created sample users inside each department’s `Users` OU
- Added users to:
  - Department security groups
  - Department admin groups (where appropriate)
- Screenshots: `screenshots/departments-ou-structure-new-user-creation.png``screenshots/departments-ou-structure-new-user-creation-successful.png``screenshots/user-added-to-group.png`

## Validate Delegation
- Logged in as a delegated admin
- Verified ability to manage only their department’s users
- Screenshots: `screenshots/delegation-validation.png`
