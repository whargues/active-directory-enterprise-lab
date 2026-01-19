# Client Domain Join — Notes

## Enter Domain Credentials to Join
- Opened System Properties → Domain Join
- Entered domain: `testdomain.local`
- Provided domain admin credentials for authorization
- Screenshot: `screenshots/domain-join-credentials.png`

## Successful Domain Join Confirmation
- Received confirmation popup indicating the machine successfully joined the domain
- System prompted for reboot to complete the process
- Screenshot: `screenshots/domain-join-success.png`

## Verify Computer Object in ADUC
- Opened Active Directory Users and Computers
- Navigated to `Computers` container
- Confirmed new client machine object appeared
- Screenshot: `screenshots/aduc-client-object.png`

## Validate Domain Identity on Client
- Logged into the domain from the client machine
- Ran `whoami` in PowerShell to confirm domain context
- Screenshot: `screenshots/whoami-domain.png`

## Join Second Client (If Applicable)
- Repeated domain join process for second machine
- Verified second computer object appears in ADUC
- Screenshot: `screenshots/aduc-second-client.png`
