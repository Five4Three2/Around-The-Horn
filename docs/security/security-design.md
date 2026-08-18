# ATH Security Design

## Purpose

Security is treated as a core design requirement within Around-The-Horn (ATH), not as a feature added after deployment.

The ATH security model is intended to protect infrastructure, hosted services, stored data, administrative interfaces, and authorized users while still allowing the environment to remain practical for learning, testing, and future expansion.

This document distinguishes between controls that are currently implemented and controls that are planned for later phases.

## Current Security Controls

The following controls are currently part of the ATH environment:

- Centralized routing and firewall management through the UniFi gateway
- Dedicated infrastructure separate from everyday desktop computing
- Restricted administrative access to infrastructure services
- Strong credential handling practices
- Separation between infrastructure management and user-facing services
- Controlled local access to self-hosted services
- Regular software and firmware updates
- Configuration and data backup planning
- Public documentation that intentionally excludes sensitive operational details

## Planned Network Segmentation

Network segmentation is a major planned security improvement.

ATH is being designed to separate devices and services according to function and trust level rather than placing every device on the same unrestricted network.

Planned logical segments include:

- Infrastructure and management
- Servers and hosted services
- Storage
- Trusted client devices
- Internet of Things devices
- Guest devices
- Lab and testing environments

Specific VLAN identifiers, addressing schemes, and production configuration values are intentionally excluded from this public repository.

## Inter-VLAN Access Control

Once segmentation is implemented, communication between network segments will be controlled through firewall policies.

The goal is to allow only the traffic required for legitimate communication while preventing unnecessary access between systems.

Examples of the intended security model include:

- User devices accessing approved services without direct access to management interfaces
- IoT devices being restricted from infrastructure and server management networks
- Guest devices remaining isolated from trusted internal resources
- Storage access being limited to systems and users that require it
- Administrative interfaces being available only from trusted management locations

These policies are planned and will be documented after they are implemented and validated.

## Administrative Access

Administrative access is treated separately from normal user access.

Management interfaces for networking, virtualization, storage, and other infrastructure components should not be exposed unnecessarily to general client devices or the public internet.

Administrative access is intended to use:

- Trusted devices
- Strong authentication
- Limited management paths
- Least-privilege principles
- Secure remote-access methods when remote administration is required

## Credential Management

Credentials, authentication tokens, private keys, and other secrets are not stored in the public ATH repository.

The repository `.gitignore` includes rules intended to reduce the risk of accidentally committing common secret and credential file types.

However, `.gitignore` is treated only as an additional safeguard. Sensitive information should never be intentionally placed in the repository in the first place.

## Remote Access

Secure remote access is planned for authorized users and administrators.

The remote-access design will avoid unnecessary direct exposure of internal infrastructure and management interfaces.

User-facing remote access and administrative remote access will be treated as separate security concerns.

The final implementation will be documented only after the selected remote-access method has been deployed, tested, and validated.

## Data Protection

ATH is being designed with multiple layers of data protection.

Current and planned measures include:

- Centralized storage
- Local backup capabilities
- Configuration backups
- Controlled user access
- Planned network-attached storage
- Planned off-site disaster recovery
- Power protection for critical infrastructure
- Recovery testing and documentation

Backups are considered separate from primary storage so that loss or corruption of the primary environment does not automatically remove every available copy of important data.

## Infrastructure Hardening

Security hardening will continue as the environment grows.

Areas of focus include:

- Disabling unnecessary services
- Limiting exposed ports
- Maintaining firmware and operating-system updates
- Reviewing access permissions
- Monitoring network and service behavior
- Protecting administrative interfaces
- Maintaining configuration backups
- Reviewing firewall policies
- Documenting infrastructure changes

## Public Repository Security

The public ATH repository is intentionally designed as a sanitized engineering portfolio rather than a complete copy of the live environment.

The following information is excluded from public documentation:

- Public and private IP addresses where unnecessary
- Detailed addressing schemes
- VLAN identifiers used in production
- Usernames and passwords
- Authentication tokens
- Private SSH keys
- Internal hostnames
- Device serial numbers
- MAC addresses
- Private service endpoints
- Detailed firewall rules
- Personally identifying user information
- Private media or stored content

Architecture diagrams and build logs use generalized labels where appropriate so that the design can be demonstrated without publishing information that would unnecessarily expose the live environment.

## Security Philosophy

The ATH security model follows several guiding principles:

- Security by design
- Least privilege
- Network segmentation
- Controlled service exposure
- Separation of administrative and user access
- Defense in depth
- Regular updates and maintenance
- Backup and recovery planning
- Continuous testing and documentation

Security controls will evolve as ATH grows, and documentation will be updated when planned controls become operational.
