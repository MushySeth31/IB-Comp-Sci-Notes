# Computer Networks
#### A system of interconnected computing devices (i.e. computers, phones, routers, etc.) that communicate and share data and resources with each other.

#### Computer networks can share data, regardless of how far the devices are.

### Parts of a network:
- Nodes -> Devices connected to a network
- Links -> Physical or wireless media that carries data between nodes
- Protocols -> Rules that govern how data is formatted, transmitted, and interpreted across the network

### Types of networks
#### LAN (Local Area Network)
Network inside a small location.

Areas such as:
- Home
- School
- Office

Usually high bandwidth and low latency
Uses Ethernet or Wi-Fi

#### Example Layout:
Computers - Switches - Router - Internet

#### WAN (Wide Area Network)
Large scale networks connecting multiple LANS. Covers cities or countries.

Biggest WAN is the Internet.

#### Example Layout:
Home LAN - ISP - Global Internet - Servers

#### PAN (Personal Area Network)
Very short range connection, around a person. Usually Bluetooth

#### Example Layout:
Phone - Smartwatch - Earphones

---

## Core Networking Devices
### Network Interface Card (NIC)
- Hardware that connects devices to a network
- Contains MAC address which uniquely identifies devices as LAN

### Switches
- Connect multiple devices in a LAN and forward frames to the correct destination using MAC address
- Reduces unnecessary broadcasting and improves network efficiency

### Routers
- Connects different networks (LAN to WAN) and route packets based on IP address

### WAPs (Wireless Access Points)
- Allows wireless devices to be connected to a wired LAN

---

## Network Communication
Data on a network is sent in packets.

Instead of one big message: HELLO WORLD

It is broken into packets:
1: HEL
2: LO
3: WOR
4:LD

Each packet contains a header, payload, and sometimes a trail for error checking

---


