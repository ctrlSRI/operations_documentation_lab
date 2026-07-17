## VM hardware configuration

The Windows Server VM was configured according to the available resources of the physical host system and the expected lab workload.

| Setting | Value |
|---|---|
| VM name | DC01-Test |
| VM generation | Generation 1 |
| Memory | 4 GB |
| Virtual processors | 2 |
| Virtual disk | 70 GB VHDX |
| Network adapter | LAB-SWITCH |
| Installation type | Windows Server 2022 Standard Evaluation with Desktop Experience |

## Configuration notes

The VM uses 4 GB of memory because Windows Server with Desktop Experience requires more resources than a minimal Server Core installation.

The virtual disk was configured with 70 GB to provide enough space for the operating system, updates, server roles, and later lab files.

The VM was assigned 2 virtual processors in this lab setup. For basic Active Directory, DNS, and DHCP testing, a configuration with 2 to 4 virtual processors is reasonable.

Generation 1 was used after the initial Generation 2 VM did not boot successfully with the available installation media and firmware configuration.

