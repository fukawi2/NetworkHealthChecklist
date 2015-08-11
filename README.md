# Network Health Checklist
A checklist of items to check, especially when inheriting a foreign network.

## Servers

- How many servers?
- What operating systems are installed?
  - Windows 2003 (!!):
  - Windows 2008:
  - Windows 2008 R2:
  - Windows 2012:
  - Windows 2012 R2:
  - Windows 2016:
  - Linux:
  - Solaris/HP-UX/Other Unix:

## Active Directory

- Is Active Directory installed?
- What is the:
  - Forest:
  - Domain(s):
- Are there any domain trusts configured?
- Are there any Group Policy objects:
  - Configured?
  - Linked to OU?

## Network

- Is there a permieter firewall in place?
- Check for rouge DHCP servers.
- Does the network have DNS redundancy?
- What IP subnet is being used on the LAN?
- Are there VLAN's in use?
- Are there mutliple Layer 3 networks on a sinple Layer 3?
- Check switch interfaces for dropped packets, CRC errors etc.
- Is there any Port Security enabled?
- Check STP is enabled
  - Is the STP root set correctly?
  - Is BPDU Guard enabled?

## Backups

- What backup software is in place?
- Have test restoration of backup been done?
- Are there off-site backups being made?

## Desktops and Laptops

- How many:
  - Desktops:
  - Laptops:

- What operating systems are installed?
  - Windows XP (!!):
  - Windows Vista (!!):
  - Windows 7:
  - Windows 8:
  - Windows 10:
  - OS X:
