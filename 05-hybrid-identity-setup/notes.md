# Hybrid Identity Setup — Notes

## Create New UPN Suffix
- Opened Active Directory Domains and Trusts
- Added new UPN suffix (e.g., `frightnight.com`)
- Verified suffix available in ADUC for user accounts
- Screenshot: `screenshots/upn-suffix-created.png`

## Prepare Users for Sync (Pre‑Sync Configuration)
- Verified users have:
- Correct UPN suffix
- Valid sAMAccountName
- Screenshot: `screenshots/user-upn-updated.png`

## Install Entra Connect
- Launched Entra Connect installer on domain-joined server
- Selected Customize setup depending on environment
- Screenshot: `screenshots/entra-connect-install.png`

## Configure Entra Connect
- Signed in with Entra Global Admin credentials
- Selected on-prem AD forest
- Configured:
- UPN suffix routing
- OU filtering (if applicable)
- Password hash sync (default)
- Screenshot: `screenshots/entra-connect-config.png`

## Initial Sync Setup
- Completed configuration wizard
- Verified sync scheduler enabled
- Screenshot: `screenshots/entra-connect-ready.png`

## Validate Sync Status
- Opened Synchronization Service Manager
- Viewed:
- Connectors
- Import/Sync/Export status
- Screenshot: `screenshots/sync-service-status.png`

## Confirm No Users Synced Yet (Expected)
- Checked Entra ID → Users
- Verified no synced users appear yet (pre‑sync state)
- Screenshot: `screenshots/entra-no-users-yet.png`

