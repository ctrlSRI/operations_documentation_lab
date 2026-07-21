# Analyze server state

## Purpose

This tutorial describes how to inspect the current state of a Windows Server system before making configuration changes.

Checking the current state is important because server roles such as Active Directory, DNS, DHCP, and file services depend on correct system and network configuration.

## Prerequisites

- Windows Server VM installed
- Access to Server Manager
- Access to PowerShell
- Administrator permissions

## Procedure

1. Open **PowerShell**.
2. Check the current computer name.
3. Check the operating system information.
4. Check the current date and time.
5. Check the network adapter status.
6. Check the current IP address configuration.
7. Open **Server Manager**.
8. Go to **Local Server**.
9. Review the displayed server properties.
10. Open the network adapter settings if more detail is required.

## PowerShell commands

```powershell
hostname
Get-ComputerInfo
Get-Date
Get-NetAdapter
Get-NetIPAddress
```

## Expected result

The current server state is known before further configuration steps are performed.

The following information should be available:

Computer name
Windows Server edition and version
Date and time
Network adapter status
IP address configuration
Local Server overview in Server Manager

## Important IP address ranges

| Range | Meaning |
|---|---|
| 127.0.0.1 | Loopback |
| 169.254.x.x | DHCP not available |
| 192.168.x.x | Private network |
| 10.x.x.x | Private network |
| 172.16-31.x.x | Private network |

## Note

Troubleshooting often depends on knowing the current state of the server.

If the network adapter is disconnected or the server receives an APIPA address, network configuration should be checked before continuing with Active Directory, DNS, or DHCP setup.

## Related concepts

- PowerShell command reference
- PowerShell system inspection
- Basic networking concepts
- Check network adapter status