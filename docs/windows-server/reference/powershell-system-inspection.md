# PowerShell system inspection

## Powershell explanation

Powershell is a command-line and scripting language from Microsoft.
It is commonly used for system administration and automation. 

Unlike the traditional Command Prompt, PowerShell works with objects, not only plain text. 
This makes it useful for inspecting, filtering, and configuring Windows systems. 

## Purpose

This reference page lists basic PowerShell commands used to inspect the current state of a Windows Server system before making configuration changes.

The goal is to understand the server name, operating system information, network adapters, IP configuration, date and time, and basic network status.

## Commands

| Command | Purpose |
|---|---|
| `hostname` | Shows the current computer name |
| `Get-ComputerInfo` | Shows detailed operating system and system information |
| `Get-NetAdapter` | Lists available network adapters and their status |
| `Get-NetIPAddress` | Shows configured IP addresses |
| `Get-Date` | Shows the current system date and time |

## Example workflow

Run the commands before changing important server settings:

```powershell
hostname
Get-ComputerInfo
Get-NetAdapter
Get-NetIPAddress
Get-Date
```