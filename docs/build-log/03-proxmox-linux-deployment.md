# Build Log 03 — Proxmox & Linux Deployment

## Objective

Establish a dedicated virtualization platform for Around-The-Horn (ATH) using the Dell OptiPlex 7070 SFF and Proxmox Virtual Environment.

The goal of this phase was to separate server workloads from everyday desktop computing and create a dedicated environment for Linux systems, containers, self-hosted services, testing, and future infrastructure projects.

## Server Platform

A Dell OptiPlex 7070 SFF was selected as the initial ATH lab server.

The system provides:

- Intel Core i7 processor
- 32 GB RAM
- 512 GB SSD
- Gigabit Ethernet connectivity
- Dedicated hardware for virtualization and self-hosted workloads

Using dedicated hardware allows ATH services to operate independently from a primary desktop computer and provides a platform that can remain available for network services and experimentation.

## Proxmox Virtual Environment

Proxmox Virtual Environment was deployed as the virtualization platform for the server.

Rather than installing individual applications directly onto the physical server, virtualization provides a layer between the hardware and the workloads running within ATH.

This architecture provides several benefits:

- Isolation between workloads
- Centralized virtual machine management
- More efficient use of physical hardware
- Easier testing and experimentation
- Ability to add or remove workloads without rebuilding the physical server
- Foundation for future backup and recovery strategies

## Linux Environment

Linux-based workloads were deployed within the virtualized environment to provide the operating-system foundation for ATH services.

Linux provides a flexible platform for:

- Self-hosted applications
- Docker containers
- Network services
- Administrative tools
- Automation
- Infrastructure experimentation

Separating services into virtualized Linux workloads also allows individual systems to be maintained or modified without directly affecting the Proxmox host.

## Container Support

Docker support was introduced within the Linux environment to provide an additional layer of application isolation.

The architecture separates the major layers of the compute environment as follows:

1. Physical server hardware
2. Proxmox virtualization platform
3. Linux workloads
4. Containers and applications
5. User-facing services

This layered approach makes it easier to understand where individual services operate and provides flexibility as the environment grows.

## Startup and Availability Validation

The environment was tested through normal system startup and operation.

Validation confirmed that:

- The Dell server successfully boots into the Proxmox environment.
- Proxmox remains accessible for management.
- The Linux environment becomes available following server startup.
- Hosted services can operate independently from the primary desktop computer.
- Network connectivity to the server remains available through the ATH network.

These tests established that the virtualization environment could function as persistent infrastructure rather than requiring manual reconstruction after each restart.

## Lessons Learned

Deploying the virtualization environment reinforced several infrastructure concepts:

- A hypervisor provides separation between physical hardware and hosted workloads.
- Virtualization makes a single physical server useful for multiple independent systems.
- Linux provides a flexible foundation for self-hosted infrastructure.
- Containers and virtual machines solve different isolation and deployment problems.
- Service availability should be validated after host startup rather than assumed.
- Separating infrastructure into layers simplifies future troubleshooting and expansion.

## Security Considerations

Administrative access to the virtualization environment is treated separately from access to user-facing services.

Sensitive information such as management addresses, credentials, authentication information, internal hostnames, and detailed configuration values is intentionally excluded from this public repository.

Future security work will include additional network segmentation, access controls, backup procedures, and infrastructure hardening as ATH develops.

## Next Steps

With the virtualization foundation operational, the next phase focuses on deploying and validating self-hosted services within the environment.

Initial service deployment includes Jellyfin, followed by additional services as ATH expands.
