# Build Log 04 — Jellyfin Deployment & Validation

## Objective

Deploy and validate Jellyfin as one of the first user-facing services within the Around-The-Horn (ATH) environment.

This phase provided an opportunity to move beyond infrastructure deployment and verify that the network, virtualization platform, Linux environment, and service layer could work together to deliver an application to multiple client devices.

## Service Selection

Jellyfin was selected as an initial self-hosted service because it provides a practical workload for testing several components of the ATH environment simultaneously.

Deploying the service required coordination between:

- Server infrastructure
- Linux
- Application services
- Network connectivity
- Persistent storage
- Client access
- User authentication

This made Jellyfin useful not only as a service but also as an early validation workload for the overall ATH architecture.

## Deployment Environment

Jellyfin operates within the ATH server environment rather than directly on an everyday desktop computer.

The service relies on the existing infrastructure layers:

1. Dell OptiPlex 7070 SFF physical server
2. Proxmox virtualization platform
3. Linux environment
4. Application and service layer
5. ATH network
6. Client devices

Separating the service from everyday desktop computing allows it to remain available independently and provides a more appropriate foundation for future self-hosted applications.

## Initial Configuration

Following deployment, Jellyfin was configured for local network access and an initial media library was established.

The initial objective was not simply to confirm that the application started successfully. The service also needed to be reachable from other devices on the network and capable of providing consistent access across different client platforms.

## Client Connectivity Testing

Jellyfin was tested from multiple client types to verify that the service was accessible beyond the server itself.

Successful testing included:

- Desktop client access
- Mobile device access
- Streaming-device access through a television
- Authentication from supported client applications
- Library visibility from authorized clients
- Media playback across the local network

Testing from multiple devices helped verify communication between the service and different areas of the ATH client environment.

## Validation

The Jellyfin deployment was considered operational after confirming that:

- The service remained available within the ATH environment.
- Authorized users could authenticate successfully.
- The configured library was visible to permitted clients.
- Desktop access functioned correctly.
- Mobile access functioned correctly.
- Streaming-device access functioned correctly.
- Media could be delivered across the local network.
- The service remained accessible independently from the primary desktop computer.

This validation demonstrated that the underlying network, server, operating-system, and application layers could successfully support a user-facing self-hosted service.

## Troubleshooting Approach

Initial client connectivity required verification that devices were connected to the appropriate network and could communicate with the Jellyfin service.

Rather than assuming that an application problem was responsible for unsuccessful access, troubleshooting included checking both the client network connection and service availability.

This reinforced the importance of troubleshooting across infrastructure layers when working with self-hosted applications.

## Lessons Learned

The Jellyfin deployment reinforced several concepts:

- A running service is not necessarily a validated service.
- Applications should be tested from the same types of clients that will actually use them.
- Client network placement can affect service accessibility.
- Application troubleshooting may require investigation beyond the application itself.
- Virtualization, Linux, networking, storage, and client configuration all contribute to service availability.
- Successful deployment should include functional testing rather than relying only on server-side status indicators.

## Security and Privacy

The public ATH repository documents the technical architecture and deployment process without exposing private content or sensitive configuration.

The following information is intentionally excluded:

- Media contents
- Private library names
- User credentials
- Authentication tokens
- Internal addressing
- Personally identifying user information
- Private service endpoints

Future remote access will be implemented using controlled and secure methods rather than unnecessarily exposing internal management interfaces or services directly to the public internet.

## Next Steps

With the initial Jellyfin deployment validated, future service development will focus on:

- Expanding persistent storage
- Integrating centralized network-attached storage
- Improving backup and recovery
- Deploying additional self-hosted services
- Implementing planned network segmentation
- Developing secure remote-access capabilities
- Continuing service monitoring and documentation
