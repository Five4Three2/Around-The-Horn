# Build Log 01 — Initial Infrastructure

## Objective

Establish the initial physical and compute infrastructure for Around-The-Horn (ATH), creating the foundation for a self-hosted home cloud and network engineering lab.

This phase focused on moving from project planning into a working environment with dedicated networking, compute, virtualization, and service-hosting capabilities.

## Initial Infrastructure

The first phase of ATH introduced the following core components:

### Network Infrastructure

- UniFi Dream Machine Pro gateway
- UniFi Pro Max managed switch
- 10 Gb SFP+ connection between core network devices
- Structured Ethernet cabling for hardwired devices
- Centralized network management through the UniFi platform

### Compute Infrastructure

- Dell OptiPlex 7070 SFF dedicated lab server
- Intel Core i7 processor
- 32 GB RAM
- 512 GB SSD
- Proxmox Virtual Environment
- Linux-based workloads
- Docker container support for current and future services

### Initial Services

- Jellyfin media server
- Local network access from multiple client platforms
- Foundation for additional self-hosted services

## Deployment Approach

ATH was intentionally deployed in stages rather than attempting to configure the entire environment at once.

Core network connectivity was established first, followed by the dedicated lab server, virtualization environment, Linux workloads, and initial self-hosted services. Each layer was tested before additional components were introduced.

This approach made it easier to isolate problems, validate individual components, and develop a better understanding of how each layer of the environment interacts with the others.

## Current Validation

The initial infrastructure has been validated through normal operation and client testing.

- Core UniFi network devices are online and communicating.
- The 10 Gb SFP+ connection between core network devices is operational.
- The Dell lab server successfully runs the Proxmox virtualization environment.
- Linux workloads remain available following system startup.
- Jellyfin is accessible across multiple client types, including desktop, mobile, and streaming-device clients.

## Security and Documentation

Sensitive infrastructure details are intentionally excluded from this public build log. This includes IP addressing, credentials, authentication tokens, device identifiers, and other configuration details that are not necessary to demonstrate the architecture or deployment process.

Detailed technical documentation will continue to be added as ATH expands.

## Next Steps

Following the initial infrastructure deployment, development will continue with:

- Network segmentation
- Firewall policy development
- Structured cabling expansion
- Centralized network-attached storage
- Additional virtualized and containerized services
- Secure remote access
- Backup and disaster-recovery capabilities
- Continued testing, monitoring, and documentation
