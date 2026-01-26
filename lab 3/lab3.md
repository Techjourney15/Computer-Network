# LAB 3: Simulation of Network Devices Using Cisco Packet Tracer

## Objectives

1. To become familiar with Cisco Packet Tracer by simulating different networking devices such as hubs, switches, bridges, routers, and repeaters.
2. To observe the movement of Protocol Data Units (PDUs) and analyze how data transmission differs between broadcast-based and unicast-based devices.

---

## Theory

### Cisco Packet Tracer
Cisco Packet Tracer is a powerful network simulation software used for designing and testing computer networks in a virtual environment. It enables learners to create network topologies and configure Cisco networking devices through a simulated command-line interface.

---

### Hub
A hub is a networking device that operates at the Physical Layer (Layer 1) of the OSI model. It connects multiple devices within a network and functions as a multiport repeater. Since it does not maintain a MAC address table, it is considered an unintelligent device.

Hubs are typically used in very small networks where traffic control and security are no major concerns.

---


### Switch
A switch functions at the Data Link Layer (Layer 2) and connects devices within a network by intelligently forwarding data packets. Unlike a hub, a switch is capable of learning and storing MAC addresses.

Switches are widely used in organizational and enterprise networks to improve performance and minimize collisions.

---


### Bridge
A bridge is also a Layer 2 networking device used to connect separate LAN segments and control traffic flow between them.

Bridges are used to divide large networks into smaller segments for better traffic management.

---

### Router
A router operates at the Network Layer (Layer 3) and is responsible for connecting multiple networks, such as linking a local network to the internet or interconnecting different subnets.

Routers are essential for internet connectivity and communication between separate network segments.

---


### Repeater
A repeater is a Layer 1 device designed to regenerate or replicate a signal.

Repeaters are deployed in network infrastructures to overcome attenuation and signal loss, ensuring data transmission remains stable over extended distances.

---

### Gateway
A gateway is a network point that provides access from one network to another. It is usually implemented using a router configured to forward traffic outside the local network.

A gateway routes traffic from a private network to external networks by acting as an entry and exit point.

---

## Observation

### Hub Implementation
---

| Device Name | Interface        | IP Address    | Subnet Mask       |
|------------|------------------|---------------|-------------------|
| PC0        | FastEthernet0    | 192.168.1.1   | 255.255.255.0     |
| PC1        | FastEthernet0    | 192.168.1.2   | 255.255.255.0     |
| PC2        | FastEthernet0    | 192.168.1.3   | 255.255.255.0     |
| PC3        | FastEthernet0    | 192.168.1.4   | 255.255.255.0     |
| PC4        | FastEthernet0    | 192.168.1.5   | 255.255.255.0     |
| PC5        | FastEthernet0    | 192.168.1.6   | 255.255.255.0     |

In this simulation, a star topology was created using a Hub. PC0, PC1, PC2, PC3, PC4, and PC5 were connected to the Hub using copper straight-through cables. When a PDU was sent from PC5 to PC0, the Hub broadcasted the packet to all connected devices. The intended recipient accepted the packet, while other devices rejected it.


### Switch Implementation

| Device Name | Interface        | IP Address     | Subnet Mask       |
|------------|------------------|----------------|-------------------|
| PC0        | FastEthernet0    | 192.168.1.10   | 255.255.255.0     |
| PC1        | FastEthernet0    | 192.168.1.11   | 255.255.255.0     |
| PC2        | FastEthernet0    | 192.168.1.12   | 255.255.255.0     |
| PC3        | FastEthernet0    | 192.168.1.13   | 255.255.255.0     |
| PC4        | FastEthernet0    | 192.168.1.14   | 255.255.255.0     |
| PC5        | FastEthernet0    | 192.168.1.15   | 255.255.255.0     |

A switch was used to connect multiple devices. After learning MAC addresses, the switch forwarded packets using unicast transmission. Data was sent directly from source to destination without disturbing other ports.

### Bridge Implementation

| Device Name | IP Address     | Subnet Mask       |
|------------|----------------|-------------------|
| Switch0    | 192.168.1.2    | 255.255.255.0     |
| Switch1    | 10.10.10.2     | 255.255.255.0     |
| Bridge0    | 192.168.1.1    | 255.255.255.0     |

Two network segments were connected using a bridge. The bridge filtered traffic and allowed packets to cross only if the destination belonged to the corresponding network segment.

### Repeater Implementation

| Device Name | Connection Type              | Status |
|------------|------------------------------|--------|
| Repeater   | Port 0 to Left Segment       | Active |
| Repeater   | Port 1 to Right Segment      | Active |

A repeater was placed between two long-distance segments to regenerate signals. This ensured successful packet transmission without signal degradation.

### Router Implementation

| Device Name | Interface              | IP Address     | Subnet Mask       | Gateway        |
|------------|------------------------|----------------|-------------------|----------------|
| Router0    | Gig0/0 (LAN 1)         | 192.168.1.1    | 255.255.255.0     | N/A            |
| Router0    | Gig0/1 (LAN 2)         | 10.10.10.1     | 255.255.255.0     | N/A            |
| PC-LAN1    | FastEthernet0          | 192.168.1.2    | 255.255.255.0     | 192.168.1.1   |
| PC-LAN2    | FastEthernet0          | 10.10.10.2     | 255.255.255.0     | 10.10.10.1    |

A router was configured to connect two different LANs. The router acted as a gateway, enabling communication between different network IDs.



## Discussion and Conclusion

The network topology was created by placing end devices such as PCs and laptops along with networking devices like hubs, switches, bridges, repeaters, and routers. Proper cable selection played a crucial role in the setup. Straight-through cables were used for connections between different device types, while crossover cables were used for similar devices.

During the initial router configuration, communication failed because the default gateway was not properly assigned on the PCs in the second network. Once the correct gateway IP was configured, the networks communicated successfully.

This experiment provided hands-on experience with how different networking devices manage data traffic. The hub demonstrated broadcast-based communication, which can lead to congestion and security concerns, while switches and routers showed more efficient and controlled data transmission.

---
