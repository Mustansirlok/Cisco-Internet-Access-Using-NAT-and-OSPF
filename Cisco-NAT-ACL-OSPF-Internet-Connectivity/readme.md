# Cisco NAT, ACL, and OSPF Internet Connectivity Lab

## Overview

This project demonstrates the implementation of Network Address Translation (NAT), Access Control Lists (ACLs), and OSPF dynamic routing in a Cisco Packet Tracer environment.

The lab simulates a real-world enterprise network where private hosts communicate with external networks through a NAT-enabled edge router. OSPF is used to exchange routing information between routers, while ACLs define which internal networks are eligible for translation.

A loopback interface configured with IP address 8.8.8.8 is used to simulate an Internet destination and verify end-to-end connectivity.

---

## Objectives

- Configure OSPF routing between routers
- Implement NAT Overload (PAT) for private networks
- Configure ACLs for NAT traffic selection
- Simulate Internet connectivity using a loopback interface
- Verify end-to-end communication from internal hosts to external networks
- Validate routing, translation, and reachability

---

## Technologies Used

- Cisco Packet Tracer
- Cisco IOS CLI
- OSPF Routing Protocol
- NAT Overload (PAT)
- Access Control Lists (ACLs)
- Loopback Interfaces
- Routing Verification
- Network Troubleshooting

---

## Network Topology

### Internal Networks

| Network | Description |
|----------|-------------|
| 192.168.1.0/24 | Branch LAN |
| 192.168.2.0/24 | Headquarters LAN |

### WAN Links

| Network |
|----------|
| 1.1.1.0/24 |
| 200.1.1.0/24 |

### Simulated Internet

| Interface | Address |
|------------|---------|
| Loopback0 | 8.8.8.8 |

---

## Features Implemented

### OSPF Dynamic Routing

Configured OSPF to advertise internal and WAN networks between routers and establish routing adjacency.

### NAT Overload (PAT)

Implemented Port Address Translation to allow multiple private hosts to share a single public IP address when accessing external networks.

### Access Control Lists

Configured ACLs to identify and permit internal traffic for NAT translation.

### Simulated Internet Connectivity

Created a loopback interface on the ISP router to emulate an external Internet resource and verify outbound connectivity.

### End-to-End Reachability Testing

Validated communication from internal hosts to the simulated Internet destination through routing and NAT translation.

---

## Verification Commands

### OSPF Verification

```bash
show ip ospf neighbor
show ip route
show ip protocols
```

### NAT Verification

```bash
show ip nat translations
show ip nat statistics
```

### ACL Verification

```bash
show access-lists
```

### Interface Verification

```bash
show ip interface brief
```

### Connectivity Testing

```bash
ping 8.8.8.8
tracert 8.8.8.8
```

---

## Project Structure

```text
Cisco-NAT-ACL-OSPF-Internet-Connectivity/

├── README.md
├── nat-acl-ospf-lab.pkt
├── topology.png

└── screenshots/
    ├── topology.png
    ├── ospf-neighbor.png
    ├── ospf-routing-table.png
    ├── nat-config.png
    ├── nat-translations.png
    ├── nat-statistics.png
    ├── acl-verification.png
    ├── interface-status.png
    ├── loopback-interface.png
    ├── ping-google-loopback.png
    └── traceroute.png
```

---

## Skills Demonstrated

- Cisco Router Configuration
- OSPF Dynamic Routing
- NAT Overload (PAT)
- Access Control Lists
- Enterprise Network Design
- Routing Troubleshooting
- IP Address Translation
- Network Verification
- Connectivity Testing
- Cisco IOS Administration

---

## Testing Results

The following validations were successfully completed:

- OSPF neighbors established
- Routes learned dynamically through OSPF
- NAT translations generated successfully
- ACLs applied and functioning correctly
- Internal hosts reached external destinations
- Loopback network reachable from private subnets
- End-to-end connectivity verified

---

## Learning Outcomes

This project provided practical experience with:

- Enterprise edge router configuration
- Dynamic routing implementation
- NAT deployment and verification
- ACL-based traffic control
- Simulated Internet access
- End-to-end network troubleshooting

---

## Author

Mustansir Lokhandwala
