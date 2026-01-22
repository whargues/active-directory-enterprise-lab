# Group Policy — Notes

##  Review Existing Default GPOs
- Viewed Default Domain Policy and Default Domain Controllers Policy
- Confirmed no modifications were made

## Create Baseline GPO
- Created new GPO: "Domain_Logon_Banner"
- Screenshot: `screenshots/default-gpos.png`
- Configured Logon Title to display to users when attempting to access login screen
- Screenshot: `screenshots/GPO_Logon_Title_Display.png`
- Configuured Interactive logon message to users attempting access login screen
- Screenshot: `screenshots/GPO_Logon_Interactive_Message.png`
- Linked to the GPO OU 
- Screenshot: `screenshots/Domain_Logon_Banner_Link_to_GPO_OU.png`
- Tested functionality of Domain Logon Banner after creation
- Screenshot: `screenshots/Domain_Logon_Banner_Successful.png`

## Create default wallpaper GPO to manage uniformity across all users
- Craeated new GPO: "Hospital_Standard_Wallpaper"
- Screenshot: `screenshots/Standard_Wallpaper.png`
- Saved Wallpaper png file to SYSVOL folder so all users can access file through GPO and allow replication to other Domain Controllers
- Screenshot: `screenshots/SYSVOL_Standard_Wallpaper.png`
- Configured policies for GPO Standard Wallpaper and mapped path to Standard_Wallpaper location
- Screenshot: `screenshots/Desktop_Wallpaper_Mapped_Path.png`
- Linked new Default_Wallpaper GPO to the domain root to allow routing to all OU's
- Screenshot: `screenshots/Hospital_Standard_Wallpaper_domain_root_link.png`
- Applied "Hospital_Standard_Wallpaper" GPO through gpupdate /force and gpresult /r to see if the GPO was applied successfully
- Screenshot: `screenshots/GPUpdate_GPresult.png`
- Verified that the Desktop Wallpaper changed from original to linked Hospital_Standard_Wallpaper
- Screenshots: `screenshots/Original_Wallpaper.png` `screenshots/Hospital_Standard_Wallpaper_Successful.png` 

## Create Department-Specific GPOs
- Created GPO for specificily Radiology Department to differentiate from default GPO Wallpaper that covers all other OUs.
- Linked each GPO to its respective OU
- Screenshot: `screenshots/department-gpos-created.png`

## 4. Configure Department Policies
- Applied settings such as:
  - Desktop wallpaper
  - Drive mappings
  - Logon banner
  - Software restrictions
- Screenshot: `screenshots/department-gpo-settings.png`

## 7. Validate GPO Application on Clients
- Ran `gpupdate /force`
- Verified settings applied
- Screenshot: `screenshots/gpupdate.png`

## 8. Run gpresult /r
- Verified correct GPOs applied to each client
- Screenshot: `screenshots/gpresult.png`


