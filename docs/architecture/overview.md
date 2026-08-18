# Around-The-Horn Architecture Overview

## Project Purpose

Around-The-Horn (ATH) is a self-hosted home cloud and network engineering lab designed to provide secure storage, private services, remote access, media streaming, and hands-on experience with enterprise-style infrastructure.

The project is being built in phases so that individual components can be deployed, tested, documented, and improved without requiring the entire environment to be completed at once.

## Architecture Goals

ATH is designed around several core goals:

- Build practical experience with networking, virtualization, Linux, containers, storage, and security.
- Maintain control of locally hosted data and services.
- Provide secure access to authorized remote users.
- Separate devices and services based on their purpose and security requirements.
- Create an environment that can be expanded and upgraded over time.
- Document the design, deployment, testing, and troubleshooting process as an engineering portfolio.

## Core Infrastructure

The ATH environment is built around several infrastructure layers:

### Network

The network layer provides routing, switching, segmentation, firewalling, and controlled access between devices and services.

### Compute

A dedicated server provides the compute resources used for virtualization, Linux services, containers, and experimentation.

### Storage

Network-attached storage provides centralized storage for files, backups, and services that require persistent data.

### Services

Self-hosted applications run within the ATH environment and are separated from the underlying infrastructure wherever practical.

### Security

Security is incorporated throughout the architecture through network segmentation, access controls, secure remote connectivity, credential management, updates, backups, and least-privilege principles.

## Design Philosophy

Around-The-Horn is intended to be more than a collection of hardware and applications. Each component is selected and configured as part of a larger system, with emphasis placed on understanding how networking, compute, storage, virtualization, and security interact.

The architecture will continue to evolve as new services are deployed, lessons are learned, and the lab expands.
