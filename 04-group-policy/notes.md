# Group Policy — Notes

## 1. Review Existing Default GPOs
- Viewed Default Domain Policy and Default Domain Controllers Policy
- Confirmed no modifications were made
- Screenshot: `screenshots/default-gpos.png`

## 2. Create Baseline GPO
- Created new GPO: `Baseline-Workstation`
- Configured core settings (e.g., password policy, audit policy, Windows Update settings)
- Linked to the domain root or Workstations OU
- Screenshot: `screenshots/baseline-gpo-created.png`

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

