# Operations Documentation Lab

This repository documents practical system administration workflows in a local lab environment.

The current focus is on Windows Server administration with Hyper-V, PowerShell, Active Directory, DNS, DHCP, Group Policy, and file services. The lab will later be extended with Ubuntu Server documentation to cover Linux-based operations workflows as well.

## Goals

- Build a documented Windows Server lab environment
- Practise common system administration tasks
- Document procedures in a clear and reproducible way
- Create operations-focused documentation using a docs-as-code workflow
- Build a public technical writing portfolio

## Current scope

- Hyper-V setup
- Virtual networking
- Windows Server installation
- PowerShell-based system inspection
- Basic network troubleshooting
- Active Directory and DNS setup planned

## Lab environment

| Component | Value |
|---|---|
| Host OS | Windows 11 Pro |
| Virtualization | Hyper-V |
| Windows Server VM | Windows Server 2022 Standard Evaluation |
| Network type | Internal Hyper-V switch |
| Lab switch | LAB-SWITCH |
| First server | DC01-Test |

## Documentation approach

The documentation is structured around different types of content:

- Tutorials for guided learning
- How-to guides for specific tasks
- Explanations for background knowledge
- Reference pages for commands, settings, and troubleshooting

## Repository structure

```text
docs/
  windows-server/
  ubuntu-server/
screenshots/
CHANGELOG.md
README.md
```