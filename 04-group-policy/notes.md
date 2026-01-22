# Group Policy — Notes

##  Review Existing Default GPOs
- Viewed Default Domain Policy and Default Domain Controllers Policy
- Confirmed no modifications were made

## Create Baseline GPO
- Created new GPO: `Domain_Logon_Banner`
- Screenshot: `screenshots/default-gpos.png`
- Configured Logon Title to display to users when attempting to access login screen
- Screenshot: `screenshots/GPO_Logon_Title_Display`
- Configuured Interactive logon message to users attempting access login screen
- Screenshot: `screenshots/GPO_Logon_Interactive_Message`
- Linked to the GPO OU 
- Screenshot: `screenshots/Domain_Logon_Banner_Link_to_GPO_OU`
- Tested functionality of Domain Logon Banner after creation
- Screenshot: `screenshots/Domain_Logon_Banner_Successful`

## 3. Create Department-Specific GPOs
- Created GPOs for each department (e.g., IT-Workstation, HR-Workstation, Finance-Workstation)
- Linked each GPO to its respective OU
- Screenshot: `screenshots/department-gpos-created.png`

## 4. Configure Department Policies
- Applied settings such as:
  - Desktop wallpaper
  - Drive mappings
  - Logon banner
  - Software restrictions
- Screenshot: `screenshots/department-gpo-settings.png`

## 5. Link GPOs to OUs
- Linked Baseline GPO to Workstations OU
- Linked department GPOs to their department OUs
- Screenshot: `screenshots/gpo-links.png`

## 6. Enforce or Block Inheritance (If Applicable)
- Enforced Baseline GPO
- Blocked inheritance on specific OUs if needed
- Screenshot: `screenshots/enforced-gpo.png`

## 7. Validate GPO Application on Clients
- Ran `gpupdate /force`
- Verified settings applied
- Screenshot: `screenshots/gpupdate.png`

## 8. Run gpresult /r
- Verified correct GPOs applied to each client
- Screenshot: `screenshots/gpresult.png`

## 9. Resultant Set of Policy (RSoP)
- Generated RSoP report
- Confirmed Baseline + Department GPOs applied
- Screenshot: `screenshots/rsop.png`

## 10. Validate Delegation
- Confirmed department admins cannot modify global GPOs
- Verified they can only manage GPOs linked to their department OUs
- Screenshot: `screenshots/delegation-gpo.png`

