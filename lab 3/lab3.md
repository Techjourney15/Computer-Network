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
A hub was used to connect multiple devices. The packet transmission was observed to be broadcast in nature, meaning data was sent to all connected devices regardless of the destination.

---

### Switch Implementation
A switch was used to connect multiple devices. Unlike the hub, once the switch learned the MAC addresses, the message flow became unicast. The packet was sent directly from the source to the destination without disturbing other ports.

---

### Bridge Implementation
Two network segments were connected using a bridge. The simulation demonstrated how the bridge filters traffic and only allows data to pass to the other segment if the destination device belongs to that segment.

---

### Repeater Implementation
A repeater was placed between two long-distance segments. The signal propagation was observed to remain stable, ensuring that packets could travel longer distances without degradation.

---

### Router Implementation
Routers were used to connect multiple networks. Communication between different network segments was successfully achieved after proper IP and gateway configuration.

---

## Discussion and Conclusion

The network topology was created by placing end devices such as PCs and laptops along with networking devices like hubs, switches, bridges, repeaters, and routers. Proper cable selection played a crucial role in the setup. Straight-through cables were used for connections between different device types, while crossover cables were used for similar devices.

During the initial router configuration, communication failed because the default gateway was not properly assigned on the PCs in the second network. Once the correct gateway IP was configured, the networks communicated successfully.

This experiment provided hands-on experience with how different networking devices manage data traffic. The hub demonstrated broadcast-based communication, which can lead to congestion and security concerns, while switches and routers showed more efficient and controlled data transmission.

---
