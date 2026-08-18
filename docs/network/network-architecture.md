# Around-The-Horn Network Architecture

## Overview

The Around-The-Horn network is designed to support a self-hosted home cloud, virtualization environment, storage services, media services, secure remote access, and future expansion.

The network is being built with an emphasis on reliability, segmentation, security, and hands-on network engineering experience.

## Core Network Components

The ATH network includes the following major infrastructure components:

- Ubiquiti gateway and routing platform
- Managed Ubiquiti switching
- High-speed SFP+ connectivity between core network devices
- Structured Ethernet cabling for hardwired devices
- Wireless access for supported client devices
- Dedicated server infrastructure
- Network-attached storage
- Internet connectivity through the local ISP

## Network Design Goals

The network architecture is designed to:

- Provide reliable connectivity for local and remote services
- Support high-speed communication between network infrastructure, servers, and storage
- Separate devices and services according to function and trust level
- Limit unnecessary communication between network segments
- Provide centralized routing, firewalling, and network management
- Support future VLAN deployment and service expansion
- Maintain room for higher-bandwidth internet and internal network upgrades

## Core Connectivity

The gateway acts as the primary routing and security device for the ATH environment.

The managed switch provides wired connectivity for infrastructure, servers, storage, and other hardwired devices.

High-speed SFP+ connectivity is used between core network components where appropriate to avoid unnecessary bandwidth bottlenecks.

Structured Ethernet cabling is used for devices that benefit from reliable wired connections.

## Network Segmentation

ATH is being designed with network segmentation as a core security principle.

As the environment develops, devices and services can be separated into logical network segments based on their role, such as:

- Infrastructure and management
- Servers and hosted services
- Storage
- Trusted client devices
- Internet of Things devices
- Guest devices
- Lab and testing environments

Segmentation allows firewall policies to control communication between these groups rather than allowing every device unrestricted access to the entire network.

## Remote Access

Remote access to ATH services will be provided through secure methods rather than exposing internal management interfaces directly to the public internet.

Administrative access and user-facing services will be treated separately so that remote users receive access only to the services they require.

## Physical Infrastructure

The network is being organized around rack-mounted infrastructure and structured cabling.

Cable management, labeling, appropriate cable lengths, and documented connections are being used to improve maintainability and simplify troubleshooting.

Where practical, additional cabling capacity is planned during installation so future devices can be added without repeating unnecessary work.

## Security Considerations

Security is integrated into the network design through:

- Network segmentation
- Firewall policies
- Restricted management access
- Secure remote connectivity
- Strong authentication
- Regular firmware and software updates
- Controlled service exposure
- Configuration backups
- Physical organization and documentation

Detailed addressing, credentials, public endpoints, and other sensitive configuration information are intentionally excluded from this public repository.

## Future Development

The ATH network architecture will continue to evolve as additional services, storage, virtualization workloads, network segments, and remote-access capabilities are deployed.

Changes will be documented as the environment develops so the repository reflects both the technical design and the engineering decisions behind it.
