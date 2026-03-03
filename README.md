# horizon-freight-network-operations
Network+ aligned NOC infrastructure simulation with VLAN design, device monitoring, and incident management.
# Horizon Freight Logistics – Network Operations (NetOps) Infrastructure

This project simulates a Network Operations Center (NOC) environment for Horizon Freight Logistics.It models real-time infrastructure monitoring, VLAN segmentation, incident tracking, and root cause analysis in a small enterprise network.

---

## 🏢 Environment Overview

The Horizon Freight NetOps environment simulates a small enterprise logistics network supporting headquarters operations, warehouse connectivity, and remote workforce access.
Infrastructure Components:

• Headquarters Office Network  
• Warehouse Branch Network  
• Remote Users via VPN  
• Fortinet Edge Firewall (FortiGate Series)  
• Core & Access Layer Switching (Cisco Catalyst)  
• Domain Controller (Active Directory / DNS / DHCP)  
• Segmented VLAN Architecture  
• Centralized IP Address & VLAN Management  
• Network Operations Center (NOC) Incident Management Platform  

---

## 🌐 Network Architecture
## IP & VLAN Management

The NOC platform includes centralized IP addressing and VLAN management to maintain clear network segmentation across the Horizon Freight infrastructure.

![IP & VLAN Management](screenshots/ip-vlan-management.png)

### VLAN Structure

| VLAN | Purpose | Subnet |
|-----|--------|--------|
| 10 | Corporate Users | 192.168.10.0/24 |
| 20 | Servers | 192.168.20.0/24 |
| 30 | VoIP | 192.168.30.0/24 |
| 40 | Guest WiFi | 192.168.40.0/24 |
| 99 | Network Management | 192.168.99.0/24 |

Each subnet is associated with a dedicated gateway and DHCP configuration where appropriate.  
This segmentation improves security, traffic management, and operational monitoring across the environment.
## Network Topology

The following diagram represents the simulated enterprise network architecture used in this Network Operations Center (NOC) environment. The design demonstrates VLAN segmentation, centralized switching, and perimeter firewall protection.

![Network Topology](screenshots/network-topology.png)

## Network Traffic Flow

The Horizon Freight infrastructure follows a layered enterprise network design to provide segmentation, security, and efficient traffic management across the environment.

### Traffic Flow Overview

1. User devices connect to access switches within **VLAN 10 (Corporate Users)**.

2. Inter-VLAN routing occurs at the **core switch**, allowing communication between segmented networks when required.

3. Internal services such as **Active Directory, DNS, DHCP, and file services** reside in **VLAN 20 (Servers)**.

4. Voice communications operate within **VLAN 30 (VoIP)** to ensure traffic isolation and maintain quality of service.

5. Guest wireless users connect to **VLAN 40 (Guest WiFi)**, which is isolated from internal resources for security.

6. Network infrastructure devices such as switches, firewalls, and monitoring systems operate within **VLAN 99 (Management)** to allow secure administrative access.

### External Connectivity

All outbound and inbound traffic passes through the **Fortinet Edge Firewall**, where security policies, NAT rules, and VPN access controls are enforced.
Remote users securely access internal services through a **VPN connection terminating at the firewall**, allowing authorized connectivity to corporate resources while maintaining network security.

---

## 📊 NOC Dashboard Capabilities
- Real-time device monitoring
- Incident tracking by OSI layer
- Root cause categorization
- Device uptime tracking
- VLAN distribution analytics
- Top devices by incident frequency

---

## 🚨 Incident Simulation Model
## Sample Incident Investigation

Example: Slow Network Performance – VLAN 10 (Corporate Users)

Incident ID: NET-0009  
Severity: Medium  
Status: Open  

Symptoms:
Users connected to VLAN 10 reported slow access to internal applications and shared resources. Increased latency observed when pinging internal servers.

Investigation Steps:
1. Verified user subnet (192.168.10.0/24) connectivity
2. Checked switch interface utilization on Core Switch SW-01
3. Reviewed VLAN routing configuration
4. Tested connectivity to Domain Controller (192.168.20.11)
5. Identified intermittent packet loss on corporate VLAN interface

Root Cause:
Network misconfiguration affecting VLAN 10 routing path.

Resolution:
Corrected VLAN routing configuration on core switch and verified stable connectivity between corporate subnet and server subnet.

Time to Resolve:
18 minutes
## Incident Management Example

The NOC platform allows incidents to be reported, categorized by OSI layer, and tracked through investigation and resolution.

![Incident Queue](screenshots/incident-queue.png)
The environment supports simulated incidents including:
- VPN instability
- DHCP scope exhaustion
- Firewall misconfiguration
- Switch port failure
- Server service disruption
Each incident follows structured investigation and resolution documentation.

---

## 📈 Operational Metrics
Dashboard tracks:
- Device uptime percentage
- Open vs. resolved incidents
- Escalation rate
- Incident distribution by OSI layer
- Root cause analytics

---

## 🎯 Objective
This project demonstrates applied Network+ concepts including:
- Subnetting
- VLAN design
- Firewall rule logic
- Incident response
- Network troubleshooting methodology
- Infrastructure monitoring awareness
