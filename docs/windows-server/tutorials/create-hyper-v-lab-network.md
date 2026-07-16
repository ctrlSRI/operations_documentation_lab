# Create an isolated Hyper-V lab network

## Purpose

This tutorial describes how to create an isolated virtual network in Hyper-V for a local Windows Server lab environment.

The lab network is used to connect virtual machines inside the lab without directly exposing them to the external network.

## Prerequisites

- Windows 11 Pro
- Hyper-V enabled
- Administrator permissions
- Basic familiarity with Hyper-V Manager

## Lab configuration

| Setting | Value |
|---|---|
| Virtual switch name | LAB-SWITCH |
| Switch type | Internal network |
| Purpose | Isolated communication between the host and lab virtual machines |

## Procedure

1. Open **Hyper-V Manager**.
2. Select the local Hyper-V host.
3. Open **Virtual Switch Manager**.
4. Select **Internal** as the switch type.
5. Click **Create Virtual Switch**.
6. Enter the name `LAB-SWITCH`.
7. Apply the changes.

## Expected result

A new internal virtual switch named `LAB-SWITCH` is available in Hyper-V.

Virtual machines connected to this switch can communicate with the host and with other virtual machines connected to the same switch.

## Notes

An internal switch allows communication between the host and the virtual machines while it keeps the test network isolated from the external network.

This setup is useful for testing Windows Server roles such as Active Directory, DNS, DHCP, and Group Policy without affecting the normal home or work network.

It does not provide direct access to the external physical network or internet to the virtual machines.
If internet access is required later, additional routing, NAT, or a different switch configuration must be added.

## Related concepts

- Install Windows Server on Hyper-V
- External virtual switch
- Internal virtual switch
- Private virtual switch
- Isolated lab environment