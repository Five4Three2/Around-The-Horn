# Build Log 02 — Network Deployment & Troubleshooting

## Objective

Deploy the core Around-The-Horn network infrastructure and establish reliable communication between the UniFi gateway, managed switch, lab server, and connected client devices.

This phase also provided an opportunity to troubleshoot device adoption and connectivity issues encountered during the initial deployment.

## Core Network Deployment

The initial ATH network deployment centered around two primary UniFi devices:

- UniFi Dream Machine Pro gateway
- UniFi Pro Max managed switch

The gateway provides centralized routing, firewall, and network-management capabilities, while the managed switch provides connectivity for the growing collection of wired infrastructure and client devices.

A 10 Gb SFP+ direct-attach copper (DAC) connection was selected for communication between the gateway and switch.

## Initial Deployment

The network infrastructure was introduced incrementally rather than replacing the existing network environment all at once.

During the initial configuration process, the UniFi devices were connected, powered on, updated, and prepared for centralized management.

The managed switch did not immediately complete the adoption process as expected. This required additional troubleshooting before the core network could be considered operational.

## Troubleshooting the Adoption Process

### Observation

The managed switch was visible to the network-management platform but initially failed to complete adoption successfully.

Device addressing also changed during the configuration process, requiring the current network state to be verified rather than relying on previously observed addressing information.

### Troubleshooting Approach

The issue was approached by verifying the environment one layer at a time:

1. Confirmed that the gateway was online and accessible.
2. Verified the physical connection between network devices.
3. Checked the current status of the managed switch.
4. Reattempted device adoption through the UniFi management interface.
5. Allowed the devices to complete required configuration and update processes.
6. Verified that both core devices reported an online and managed state.

This process reinforced the importance of validating the current state of a network rather than assuming that previously observed device information remains unchanged during deployment.

## SFP+ Connectivity

After the core devices were successfully adopted and operational, the SFP+ DAC connection between the gateway and managed switch was established and verified.

The connection provides a high-bandwidth link between the two primary network devices and creates additional capacity for future server, storage, and network traffic.

## Validation

Following troubleshooting and deployment, the core network was validated by confirming:

- The UniFi gateway was online and manageable.
- The UniFi managed switch was successfully adopted.
- Both devices reported an operational state.
- The SFP+ connection between the gateway and switch was active.
- Connected client devices maintained network connectivity.
- The lab server remained reachable through the network.
- Network-management information was available through the centralized UniFi interface.

## Lessons Learned

The initial network deployment demonstrated several practical lessons:

- Device adoption may require troubleshooting even when physical connectivity appears correct.
- IP addressing and device state can change during deployment and configuration.
- Physical connectivity should be verified before focusing on software configuration.
- Infrastructure changes are easier to troubleshoot when introduced incrementally.
- Successful adoption does not replace the need to validate actual network connectivity afterward.
- Maintaining documentation during deployment makes later troubleshooting easier.

## Security Considerations

Specific IP addresses, device identifiers, credentials, authentication information, and detailed firewall configuration are intentionally excluded from this public build log.

Future network segmentation and firewall policies will be documented at an architectural level while sensitive production configuration remains private.

## Next Steps

With the core network infrastructure operational, future network development will focus on:

- Expanding structured Ethernet cabling
- Implementing planned network segmentation
- Developing inter-VLAN firewall policies
- Integrating centralized network-attached storage
- Expanding monitoring and configuration backups
- Implementing secure remote-access capabilities
