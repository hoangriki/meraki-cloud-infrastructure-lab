# 01 - Meraki Dashboard Initialization

This module documents the initial configuration and architectural setup of the Cisco Meraki cloud management platform.

The focus of this section is establishing the organizational structure, device inventory workflow, network segmentation model, and licensing architecture within the Meraki Dashboard.

---

## 🔧 Technical Objectives

- Provision a Meraki Organization
- Establish network hierarchy
- Claim and assign hardware to inventory
- Deploy logical networks
- Apply and validate licensing
- Understand the cloud management control plane

---

## 🏗 Meraki Cloud Architecture Overview

The Meraki Dashboard operates as a centralized cloud control plane.

All managed devices (MX, MS, MR, SM) establish secure outbound management tunnels to the Meraki cloud. Configuration changes are performed in the dashboard and pushed to devices in real time.

Architecture Layers:

1. **Organization** (Top-level administrative boundary)
2. **Inventory** (Hardware asset pool)
3. **Network** (Logical deployment container)
4. **Devices** (MX, MS, MR, SM endpoints)

Understanding this hierarchy is critical for scalable enterprise deployments.

---

## 🏢 Organization Provisioning

Actions Performed:

- Created a new Organization
- Configured administrative access controls
- Reviewed role-based access capabilities

Key Concept:
The Organization acts as the global administrative boundary.  
All networks, licenses, administrators, and devices are managed within this scope.

Best Practice:
Separate organizations for MSP clients or distinct business entities.

---

## 📦 Device Claiming & Inventory Management

Devices were added using:

- Serial number claim
- Order number bulk claim

Workflow:

1. Claim device into Organization inventory
2. Assign device to a specific Network
3. Device checks in via cloud management plane

Key Distinction:

- **Inventory** = Asset ownership
- **Network** = Operational deployment

This separation enables hardware staging prior to production assignment.

---

## 🌐 Network Creation & Logical Segmentation

Networks were created to simulate deployment scenarios.

Supported network types:

- Security Appliance (MX)
- Switching (MS)
- Wireless (MR)
- Systems Manager (SM)
- Combined Network

Design Considerations:

- Use structured naming conventions (Location-Function)
- Align networks with physical or logical sites
- Plan for VLAN segmentation and security policy boundaries

Example Naming Standard:

- HQ-Combined
- Branch01-MX
- Lab-Wireless

Proper network segmentation improves scalability and policy enforcement.

---

## 🔐 Licensing Model & Co-Termination

Meraki operates on a subscription-based licensing model.

Actions Performed:

- Claimed license key
- Applied license to Organization
- Reviewed co-termination status

Key Concept: **Co-Termination Model**

All device licenses within an organization share a single expiration date.

When additional licenses are added, the dashboard recalculates a weighted average expiration date across all devices.

Operational Risk:

If licenses expire, devices enter a grace period and eventually cease operation.

License management is critical for production environments.

---

## 📊 Administrative & Governance Review

Explored:

- Organization-wide settings
- Admin role assignment
- API access enablement (for future automation)
- Change logging and audit tracking

This reinforces governance and infrastructure management best practices.

---

## 🧠 Engineering Takeaways

- Cloud-managed networking relies on centralized control plane architecture
- Organizational design impacts scalability and multi-site deployments
- Inventory separation enables controlled device lifecycle management
- Licensing architecture must be planned to avoid service disruption
- Naming conventions directly affect operational clarity

---

## 🧪 Lab Validation

- Successfully provisioned Organization
- Claimed and assigned device to inventory
- Created Combined Network
- Verified device registration status
- Reviewed licensing dashboard
- Audited administrative configuration options

---

## 🎯 Infrastructure Relevance

This module establishes foundational knowledge for:

- Cloud-based network operations
- Hybrid infrastructure deployments
- SD-WAN configuration (MX)
- Policy-based segmentation
- Infrastructure governance

These concepts directly support modern cloud engineering and DevOps practices where centralized control planes and infrastructure abstraction are standard.

---

## Status

Completed ✔
