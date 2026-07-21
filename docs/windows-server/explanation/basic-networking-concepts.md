# Basic networking concepts

## General

Basic networking knowledge is required before configuring Windows Server roles such as Active Directory, DNS, DHCP, and file services.

In this lab, the first networking tasks were used to understand how the virtual machine communicates inside the Hyper-V lab environment.

## IP address

An IP address identifies a device inside a network.

Example:

```text
192.168.100.10
```

In a Windows Server lab, IP addresses are important because servers usually need stable addresses. A domain controller or DNS server should not randomly receive a different IP address after a restart.

## DHCP

DHCP stands for Dynamic Host Configuration Protocol.

DHCP automatically assigns network configuration to devices, for example:

IP address
Subnet mask
Default gateway
DNS server

In a lab environment, DHCP can be provided by a router, by Windows Server, or by another configured DHCP service.

## APIPA

APIPA stands for Automatic Private IP Addressing.

Windows uses APIPA when no DHCP server is available and no static IP address is configured.

APIPA addresses usually look like this:

```text
169.254.x.x
```

If a server receives an APIPA address, it usually means that it did not receive a valid IP configuration from DHCP.

## DNS

DNS stands for Domain Name System.

DNS translates names into IP addresses.

Example:

```text
google.com -> IP address
```

In an Active Directory environment, DNS is especially important because domain members use DNS to find domain controllers and other services.

## Hosts file

The hosts file is a local file that can map hostnames to IP addresses.

It can be used before DNS is available or for simple local name resolution tests.

On Windows, the hosts file is located here:

C:\Windows\System32\drivers\etc\hosts

## DNS cache

Windows stores recently resolved DNS names in a local DNS cache.

This can make repeated name resolution faster, but it can also cause confusion during troubleshooting if old entries are still cached.

## Loopback address

The loopback address points back to the local computer.

The most common IPv4 loopback address is:

127.0.0.1

The hostname localhost also points to the local system.

This is useful for testing whether the local network stack is working.

## IPv4 and IPv6

IPv4 and IPv6 are two versions of the Internet Protocol.

IPv4 addresses look like this:

192.168.100.10

IPv6 addresses look different and are longer:

fe80::1

The main difference of IPv6 to IPv4 is the larger number of possible addresses.

In this lab, the main focus is IPv4 because it is easier to understand at the beginning and commonly used in small lab networks.

## Default gateway

A default gateway is the device that forwards traffic to other networks.

In a home network, the default gateway is usually the router.

In an isolated Hyper-V internal network, a default gateway may not be available at first. This means the VM can communicate inside the lab network, but not necessarily with the internet.

## Interface alias and interface index

Windows identifies network interfaces with names and numbers.

The interface alias is the readable name of the network adapter.

Example:

Ethernet

The interface index is a number used by Windows to identify the network adapter.

PowerShell commands often use the interface alias or interface index when changing network settings.

## Summary

Before configuring Active Directory, DNS, or DHCP, the current network configuration should be checked.

Important questions are:

Does the network adapter exist?
Is the adapter connected?
Does the server have an IP address?
Was the IP address assigned by DHCP?
Is the address an APIPA address?
Can the server resolve names?
Can the server reach other systems?