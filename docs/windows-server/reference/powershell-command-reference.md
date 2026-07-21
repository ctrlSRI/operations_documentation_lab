# PowerShell command reference

## Purpose

This reference page lists PowerShell commands used in the Windows Server lab.

The commands are grouped by topic and include a short explanation of what each command is used for.

## Basic system information

| Command | Purpose |
|---|---|
| `hostname` | Shows the current computer name |
| `Get-ComputerInfo` | Shows detailed operating system and system information |
| `Get-Date` | Shows the current system date and time |

## Network inspection

| Command | Purpose |
|---|---|
| `Get-NetAdapter` | Lists available network adapters and their current status |
| `Get-NetIPAddress` | Shows configured IP addresses |
| `Get-NetIPConfiguration` | Shows IP configuration, DNS server, and default gateway information |
| `Resolve-DnsName <name>` | Tests DNS name resolution |
| `Test-Connection <target>` | Sends ICMP echo requests, similar to `ping` |

## Examples

Show the current computer name:

```powershell
hostname
```

Show network adapters:

```powershell
Get-NetAdapter
```

Show IP addresses:

```powershell
Get-NetIPAddress
```

Test local loopback:

```powershell
Test-Connection 127.0.0.1
```

Test DNS resolution:

```powershell
Resolve-DnsName google.com
```

## Notes

These commands are useful before changing server settings.

Checking the current system state first helps to identify configuration problems and makes troubleshooting easier.