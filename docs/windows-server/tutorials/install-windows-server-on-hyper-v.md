# Install Windows Server on Hyper-V

## Purpose

This tutorial describes how to create a Windows Server virtual machine in Hyper-V and install Windows Server 2022 Standard Evaluation.

The VM is used as the first server in a local Windows Server lab environment.

## Prerequisites

- Windows 11 Pro host system
- Hyper-V enabled
- Internet connection
- Administrator permissions
- Sufficient local disk space
- Windows Server 2022 Evaluation ISO

## Download the Windows Server ISO

Download the Windows Server 2022 Evaluation ISO from the official Microsoft Evaluation Center.

In this lab, the following ISO was used:

```text
SERVER_EVAL_x64FRE_en-us.iso
```

## Important note about ISO files

An ISO file must contain a bootable operating system installation image.
During the lab setup, an incorrect ISO file was selected first:

```text
LOF Packages OEM
```

This file was not a bootable Windows Server installation medium.
As a result, the virtual machine could not start the Windows Server installation.

## VM configuration summary

The VM was configured with 4 GB memory, 2 virtual processors, a 70 GB virtual hard disk, and the LAB-SWITCH internal network.

The detailed VM hardware configuration is documented separately in:

configure-vm-on-hyper-v.md

## Procedure

 1. Open **Hyper-V Manager**
 2. Select the local Hyper-V host
 3. Create a new virtual machine.
 4. Enter the VM name DC01-Test.
 5. Select **Generation 1**.
 6. Assign 4 GB of memory.
 7. Connect the VM to the LAB-SWITCH virtual switch.
 8. Create a new virtual hard disk with 70 GB.
 9. Attach the Windows Server 2022 Evaluation ISO.
10. Start the VM.
11. Follow the Windows Server installation wizard.
12. Select **Windows Server 2022 Standard Evaluation with Desktop Experience**.
13. Complete the installation.

## Expected result

Windows Server 2022 Standard Evaluation is installed successfully as a Hyper-V virtual machine.

The VM can be started and accessed through Hyper-V Manager.

## Troubleshooting

If the VM does not boot from the ISO, check the following:

The ISO file is a bootable Windows Server installation image.
The ISO is attached to the virtual DVD drive.
The virtual DVD drive is included in the boot order.
Secure Boot settings are compatible with the selected VM generation.
The correct VM generation is used for the installation media.

## Lessons learned

Not every ISO file is a bootable operating system installation medium.

For a lab environment, recreating a VM can be faster than spending too much time troubleshooting a broken initial configuration.

Documenting failed attempts is useful because it explains why the final configuration was chosen.