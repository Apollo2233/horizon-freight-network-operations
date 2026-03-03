# horizon-freight-network-operations
Network+ aligned NOC infrastructure simulation with VLAN design, device monitoring, and incident management.
# Horizon Freight Logistics – Network Operations (NetOps) Infrastructure

This project simulates a Network Operations Center (NOC) environment for Horizon Freight Logistics.It models real-time infrastructure monitoring, VLAN segmentation, incident tracking, and root cause analysis in a small enterprise network.

---

## 🏢 Environment Overview
- 1 Headquarters Office
- 1 Warehouse Network
- Remote Users via VPN
- Fortinet Edge Firewall
- Core & Access Layer Switching
- Domain Controller (AD/DNS/DHCP)
- Segmented VLAN Architecture

---

## 🌐 Network Architecture
## Network Topology

The following diagram represents the simulated enterprise network architecture used in this Network Operations Center (NOC) environment. The design demonstrates VLAN segmentation, centralized switching, and perimeter firewall protection.

![Network Topology](screenshots/network-topology.png)

### VLAN Segmentation
| VLAN | Purpose        | Subnet            |
|------|---------------|------------------|
| 10   | Corporate     | 192.168.10.0/24  |
| 20   | Servers       | 192.168.20.0/24  |
| 30   | VoIP          | 192.168.30.0/24  |
| 40   | Guest WiFi    | 192.168.40.0/24  |
| 99   | Management    | 192.168.99.0/24  |

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
