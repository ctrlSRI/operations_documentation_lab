# What is PowerShell

## General

PowerShell is a command-line shell and scriping language from Microsoft. It is commonly used for system administration, automation, and configuration tasks. PowerShell is especially useful when tasks must be repeated, documented, and executed in a consistent way.

Instead of clicking trough graphical user interfaces, administrators can describe actions as commands and scripts. This makes processes easier to repeat, automate, and troubleshoot. 

## Use of PowerShell

PowerShell is used for tasks such as:

- Inspecting system information
- Managing Windows Server configuration
- Automating repeated administration tasks
- Working with services, users, files, and network settings
- Processing and exporting data from different sources

In a Windows Server lab, PowerShell is useful because it allows the current system state to be checked before making configuration changes.

## PowerShell-syntax

PowerShell commands are called cmdlets. Cmdlets usually follow a verb-noun structure.

Example:

```powershell
Get-Process
``` 
In this example:

Get is the verb
Process is the noun

## Object-based pipeline

Unlike the traditional Command Prompt, PowerShell does not only work with plain text. PowerShell works with objects.

Objects contain properties that can be filtered, sorted, selected, exported, or passed to another command.

Example:
```powershell
Get-Process|Sort-Object CPU -Descending|Select-pbject -First 10
```  
This command gets running processes, sorts them by CPU usage, and shows the first ten results.

## Exporting data

PowerShell can export command output into different formats, for example CSV or JSON.

Example:

Example:
```powershell
Get-Service | Export-Csv -Path .\services.csv -NoTypeInformation
```
This command exports service information into a CSV file.

## Scripts and modules

PowerShell commands can be combined into scripts. Scripts are useful when a task should be repeated or documented.

Reusable logic can also be organized into modules. Modules can contain functions, variables, and commands that can be reused across different scripts or projects.   

## Summary

PowerShell is an important tool for Windows Server administration because it combines command-line usage, scripting, automation, and structured data processing.

For this lab, PowerShell is used to inspect the server state, configure system settings, and document administration workflows.
