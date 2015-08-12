# Network Health Checklist
A checklist of items to check, especially when inheriting a foreign network.

This list is meant to be a prompt sheet for getting an overview of a network
in order to understand and make recommendations, as well as perform basic
health check. It is not a survey that you can get a client to complete.

## Servers
- How many servers?
- Is virtualization being used?
  - Virtual platform? (VMware/Xen/HyperV etc)
- What operating systems are installed?
  - Windows NT4 (!!), 2003 (!!), 2008, 2008 R2, 2012, 2012 R2, 2016
  - Linux
  - Solaris/HP-UX/Other Unix
- File Servers
- NAS devices
- Is there a SAN? Fibre Channel or iSCSI?
- Check disk utilization of File Servers / NAS / SAN.
- Are there UPS units installed? Operational?

### All Servers
Check the following items:
- free disk space
- disk health
  - RAID health
  - RAID level; none (!!), RAID0 (!!), RAID1, RAID5, RAID6, RAID10
- running processes
- memory utilization
- pending updates
- multi-homing

### Windows Servers
Check the following items:
- disk fragmentation
- network file shares
- local admin accounts

### Linux Servers
Check the following items:
- load average
- mountpoints (local and remote)
- listening ports
- logged in users
- host firewall
- uptime

### Website
- Website hosting provider? (External/Internal)
- Website deceloper(s)?

### Email
- Email hosting platform? (Google Apps, Rackspace, Self-hosted etc)
- Self-hosted platform? (Exchange, Kerio Connect etc)
- Server Address, Ports
- Anti-spam and Anti-virus protection?
- Public MX records?
- SPF records? DKIM?

## Active Directory
- Is Active Directory installed?
- What is the:
  - Forest:
  - Domain(s):
- Is the domain(s) public or private?
  - Public: Is the domain registered to the business?
- Is there any OU structure in place?
- Are there any domain trusts configured?
- Are there any Group Policy Objects:
  - Configured?
  - Linked to OU?
- Is there a password policy in place?
  - Change every X days
  - Complexity?
  - Number of passwords remembered?
- Are there DFS namespaces being used for file shares?

## Network
- What IP subnet is being used on the LAN?
- Router/Gateway IP address:
- Are there VLAN's in use?
- Are there mutliple Layer 3 networks on a single Layer 3?

### Firewall
- Is there a permieter firewall in place?
- Is egress traffic filtered?

### DNS
- Does the network have DNS redundancy? (2 or more working DNS servers)
- Locally authorative DNS zones:

### DHCP
- DHCP server:
- DHCP scope:
- Check for rouge DHCP servers.

### Switches
- How many switches are installed
  - Make/Models
  - Utilization (port usage) of each switch
- Speed/capabilities
  - 10/100mbps -- Gigabit?
  - Copper -- Fibre?
  - SFP's or Media Converters in place?
- Switch topology:
  - Star
  - Daisy-chain
  - Mesh
- Managed Switches:
  - Check interfaces for:
    - Dropped packets.
    - CRC errors.
    - Forced speed/duplex.
  - Is there any Port Security enabled?
  - Check STP is enabled
    - Is the STP root set correctly?
    - Is BPDU Guard enabled?

### Wireless
- Wireless network installed?
- What are the SSID's?
- Security:
  - Open / No Security (!!)
  - WEP (!!)
  - WPA/WPA2 PSK
  - WPA2 Enterprise
  - Mac Filtering
- Hardware:
  - Make/Models
  - 802.11a/b/g/n/ac
- Management method (individual AP's, central management etc)
- Is coverage sufficient?

## Security
- Do users have Local Admin rights?
- Do any users have remote access?
  - Remote Desktop
  - Citrix
- Are there VPN services in place?
  - Site-to-site
  - Road warrior
  - IPSec / PPTP / SSL
- Are there SSL/TLS protections in place for:
  - Corporate website
  - Email retrieval (POP3/IMAP/ActiveSync)
  - Email sending (SMTPS)
  - Public or self-signed certificates?
  - What are the SSLLabs test results?
- Is there any form of NAC (eg, 802.1x)?

### Active Directory
- Do users have Domain Admin rights?
- Are there additional enterprise/domain admin accounts besides "Administrator"?
- Are old users/computers disabled/deleted from Active Directory?

## Backups
- What backup processes are in place?
- Have test restoration of backup been done?
- Are there off-site backups being made?
- Shadow Copies enabled on Windows file servers?

## End-user Devices
- How many:
  - Desktops
  - Laptops
  - Tablets
  - Smartphones

### Software
- Operating systems:
  - Windows XP (!!)
  - Windows Vista (!!)
  - Windows 7
  - Windows 8
  - Windows 10
  - OS X
  - Linux
- Productivity software (eg Microsoft Office)?
- Anti-virus protection?
- Business/Industry specific applications?
- Are there any instances of Dropbox, OneDrive, Google Drive etc?
  - If yes, is it authorized or is it Shadow IT?
- Are there any instances of TeamViewer, LogMeIn etc?
  - If yes, is it authorized or is it Shadow IT?
