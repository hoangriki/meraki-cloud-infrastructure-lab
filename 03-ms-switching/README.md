# 03 - Meraki MS Switching

This module covers the deployment and configuration of Cisco Meraki MS switches within the Meraki cloud-managed networking platform.

The focus is on Layer 2 switching fundamentals, VLAN segmentation, port configuration, and operational visibility through the Meraki Dashboard.

Meraki MS switches provide centralized cloud-based management for campus and branch switching environments while maintaining traditional switching concepts such as trunking, access ports, and VLAN tagging.

---

## 🔧 Technical Objectives

- Deploy and manage MS switches through the Meraki Dashboard
- Configure access and trunk switch ports
- Implement VLAN segmentation
- Monitor switch performance and port status
- Apply centralized switching policies

---

## 🏗 Meraki Switching Architecture

Meraki MS switches operate as Layer 2 switches managed through the Meraki cloud control plane.

Key architecture components include:

- **Cloud Management Plane** – configuration and monitoring via Meraki Dashboard
- **Switching Data Plane** – local packet forwarding between connected devices
- **Secure Device Management Tunnel** – outbound encrypted communication between switch and Meraki cloud

Configuration is performed in the cloud and pushed to the switch automatically.

---

## 🔌 Switch Deployment Workflow

Switch deployment in the Meraki environment follows a standardized workflow:

1. Claim switch into Organization inventory
2. Assign switch to a network
3. Connect switch to internet for cloud registration
4. Configure switching policies via the Dashboard

Once online, the device automatically downloads its configuration from the Meraki cloud.

---

## 🌐 VLAN Segmentation

Virtual LANs (VLANs) are used to logically segment networks within a switching environment.

Example VLAN architecture:

| VLAN ID | Network Purpose |
|-------|----------------|
| 10 | User Devices |
| 20 | Voice / VoIP |
| 30 | Guest Network |
| 99 | Management |

Benefits of VLAN segmentation:

- Network isolation
- Improved security boundaries
- Reduced broadcast domains
- Easier traffic policy enforcement

---

## 🔄 Switch Port Configuration

Meraki switch ports can operate in two primary modes:

### Access Ports

Access ports connect endpoint devices and carry traffic for a single VLAN.

Common devices:

- Workstations
- Printers
- VoIP phones
- IoT devices

Configuration elements:

- Access VLAN assignment
- Port description
- Port isolation (optional)

---

### Trunk Ports

Trunk ports allow multiple VLANs to traverse a single link between network devices.

Typical trunk connections:

- Switch-to-switch uplinks
- Switch-to-router links
- Switch-to-firewall connections
- Switch-to-access-point connections

Configuration elements:

- Native VLAN
- Allowed VLAN list
- Trunk encapsulation (802.1Q)

---

## 📊 Switch Monitoring & Visibility

The Meraki Dashboard provides real-time visibility into switch operations.

Available monitoring capabilities include:

- Port utilization statistics
- Connected device identification
- Power over Ethernet (PoE) status
- Link speed and duplex information
- Event logs and port activity history

Operational Benefit:

Cloud-based visibility simplifies troubleshooting and network diagnostics without requiring direct CLI access.

---

## ⚡ Power over Ethernet (PoE)

Many Meraki MS switches support PoE for powering connected devices.

Common PoE devices include:

- Wireless access points
- VoIP phones
- Security cameras
- IoT sensors

Benefits:

- Reduces power infrastructure requirements
- Simplifies device deployment
- Centralized power management

---

## 🔐 Security Considerations

Switching infrastructure plays a key role in enforcing network security.

Security measures include:

- VLAN segmentation
- Port isolation
- Controlled trunk access
- Monitoring unauthorized device connections

Switch-level segmentation provides an important layer in a defense-in-depth security model.

---

## 🧠 Engineering Takeaways

- Meraki MS switches retain traditional Layer 2 switching concepts while leveraging cloud management
- VLAN segmentation is essential for scalable network design
- Access vs trunk port configuration is foundational for network traffic flow
- Centralized monitoring improves operational visibility
- Cloud-managed switching reduces configuration overhead in distributed environments

---

## 🧪 Lab Validation

- Deployed MS switch into Meraki network
- Configured access ports for endpoint devices
- Configured trunk ports for network uplinks
- Implemented VLAN segmentation
- Verified port status and device connectivity through the Dashboard

---

## 🎯 Infrastructure & DevOps Relevance

Understanding switching architecture supports:

- Cloud and hybrid network design
- Infrastructure segmentation strategies
- Data center and campus networking
- Observability and network monitoring practices

In modern infrastructure environments, these principles align with:

- Infrastructure automation
- Network-as-Code models
- Scalable enterprise deployments

---

## Status

Completed ✔
