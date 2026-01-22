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
- Screenshot: `screenshots/Hospital_Standard_Wallpaper_GPO.png`
- Saved Wallpaper png file to SYSVOL folder so all users can access file through GPO and allow replication to other Domain Controllers
- Screenshot: `screenshots/SYSVOL_Standard_Wallpaper.png`
- Configured policies for GPO Standard Wallpaper and mapped path to Hospital_Standard_Wallpaper location
- Screenshot: `screenshots/Desktop_Wallpaper_Mapped_Path.png`
- Linked new Default_Wallpaper GPO to the domain root to allow routing to all OU's
- Screenshot: `screenshots/Hospital_Standard_Wallpaper_domain_root_link.png`
- Applied "Hospital_Standard_Wallpaper" GPO through gpupdate /force and gpresult /r to see if the GPO was applied successfully
- Screenshot: `screenshots/GPUpdate_GPresult.png`
- Verified that the Desktop Wallpaper changed from original to linked Hospital_Standard_Wallpaper
- Screenshots: `screenshots/Original_Wallpaper.png` `screenshots/Hospital_Standard_Wallpaper_Successful.png` 

## Create Department-Specific GPOs
- Created GPO for specificily Radiology Department to differentiate from default Hospital_Standard_Wallpaper GPO that covers all other OUs.
- Screenshot: `screenshots/Radiology_Desktop_Banner_GPO.png`
- Saved Wallpaper png file to SYSVOL folder so all users can access file through GPO and allow replication to other Domain Controllers
- Screenhot: `screenshots/SYSVOL_Radiology_Banner.png`
- Configured policies for GPO Standard Wallpaper and mapped path to Radiology_Desktop_Banner location
- Screenshot: `screenshots/Radiology_Wallpaper_Mapped_Path.png`
- Linked GPO to its respective OU (Radiology)
- Screenshot: `screenshots/OU_GPO_Link.png`
- Linked specific Group to GPO to limit least privledge on who can edit GPO (Radiology_Admins)
- Screenshot: `screenshots/Group_Link_Radiology_GPO.png`
- Ran Powershell Command "whoami"to verify user is part of different OU (IT)
- Screenshot: `IT_User.png`
- Ran Powershell Command "whoami" to verify user is part of the Radiology OU and ensured that Desktop Wallpaper changed to specific GPO that was linked to Radiology OU
- Screenshot: `Radiology_User_Successful.png`
  
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


