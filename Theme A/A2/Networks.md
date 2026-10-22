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
- 1: HEL
- 2: LO
- 3: WOR
- 4:LD

#### Each packet contains a header, payload (data), and sometimes a trail for error checking.

Protocol data units (PDUs) layers:
- Frame at data link
- Packet at network
- segment at transport

#### Protocols define how data is structured, routed, checked for errors, and reassembled at the destination.

---

## Network Models
Layerd models describe how data travels through different conceptual layers.

### Open System Interconnection model (OSI)
Reference frameork for how communication should proceed from one aplication to another through a network.

OSI Layers:
1. Application
- Network services directly to user applications
- Interface between user's application and the network
- Allows softwares (browsers) to access network communcation services

2. Presentation
- Ensures data is formatted in a way tha the receiving system can understand
- Responsible for data formatting, encryption and decryption, and compression

3. Session
- Manages and controls communication sessions between devices
- Establishes, maintains, and terminates the session
- Conversations between devices must stay organized and synchronized

4. Transport
- End-to-end communication between devices
- Ensures data is delivered reliably, set in correct order, and flow is controlled
- Manages delivery process between sender and receiver

5. Network
- Determines how data travels from one network to another
- Assigns logical addresses (IP addresses)
- Determines best route for data
- Routes packets across networks
- Responsible for getting data from source to destination across multiple networks

6. Data Link
- Manages communication between devices on the same network
- Uses physical (MAC) address
- Organizes data into frames
- Detects transimssion errors
- Ensures data is moved correctly in a local network

7. Physical
- Transmitting raw bits over a physical medium
- Sends electrical, optical, or radio signals
- Defines cables, voltages, and signal standards
- Physically moves data from one device to another

#### Each layer serves the one above it and is served by the one below it, making network design modular and interoperable.

### TCP/IP Model
Similar to OSI model, just modernized

TCP/IP Layers:
1. Application
- Provides network communication services directly to user applications
- Allows applications to send and receive data over the network

2. Transport
- Deliver data from one device to another
- Must arrive at the correct destination device, delivered reliably, and organized correctly
- Manages end-to-end communication between devices
- Breaks data into packets

3. Internet
- Addressing and routing data across networks
- Assigns IP addresses
- Determines best route for data
- Routes packets between networks

4. Network Access
- Handles communication between a device and the physical network
- Controls how data is physically transmitted
- Uses hardware (network cards)
- Send data through cables or wireless signals
- Ensures data actually leaves the device and enters the network medium

#### OSI Application, Presentation, and Session --> TCP/IP Application
#### OSI Transport --> TCP/IP Transport
#### OSI Network --> TCP/IP Internet
#### OSI Data Link and Physical --> TCP/IP Network Access

---

## Network Performance
### Bandwidth
Maximum capacity of the link.

Measured in bits per second (bps)

### Throughput
Actual rate achieved.

### Latency (Ping)
Delay between sending and receiving data.

Measured in miliseconds (ms).

### Jitter
Variation in delay.

Like uncertainties for ping.

---

## Network Topology
Physical or logical arrangement of devices in a netork and how data flows between them.

Directly affects:
- Reliability
- Transmission speed
- Scalability
- Data collisions
- Cost

### Star Topology
#### Strucutre
All devices are connected to a central device (A switch called "the hub").

#### Functions
- Centralizes traffic control
- Reduces data collisions
- Simplifies troubleshooting

#### Reliability
High reliablity for individual device failure. However, if hub fails, entire network collapses.

#### Transmission Speed
Fast, as modern switches allow full-duplex communication (two devices can transmit and receive data simultaneously).

#### Scalability
Moderately scalable, can add devices by connecting to the hub.

#### Cost
Moderate, requires more cabling than some topologies.

#### Used in homes, small offices, and classrooms because of reliability and simplicity being prioritized.

### Mesh Topology
#### Structure
Devices are interconnected with multiple redundant paths

#### Functions
- Multiple routing for data
- Ensures fault tolerance
- Prevents single points of failure

#### Reliability
Very high reliability. If one line fails, data reroutes.

#### Transmission Speed
Fast in well-designed systems.

#### Scalability
Complex scalability, connections grow rapidly.

#### Cost
High cost, requires many cables and parts

#### Used in data centers, governments, mission-critical systems, and internet backbone due to highly important reliability.

### Hybrid Topology
#### Structure
Combination of two or more topologies.

#### Functions
- Balance cost and reliability
- Enables scalable enterprise networks

#### Reliability
Depending on design, usually high.

#### Transmission Speed
Optimized through hierarchical structure.

#### Scalability
Highly scalable, suitable for large organizations

#### Cost
Moderate to high

#### Used in corporations, universities, government departments, and large enterprises.
#### Most real-world networks today are hybrid.

## Network Architecure
How communication is structured and organized.

Two main architecture models:
- Client-Server
- Peer-to-Peer (P2P)

### Client-Server Architecture
Centralized model where clients request services from dedicated server.

#### Structure
Clients --> request services

Server --> provides services

#### Benefits
- Centralized control
- Better security management
- Easier backups
- Scalable

#### Drawbacks
- Server failure affects many users
- Higher setup cost
-  Requires maintainance

#### Used for web browsing, email, online banking, corporate databases, VoIP systems.

### Peer-to-Peer (P2P) Architecture
Decentralized model where each device can act as both client and server.

#### Structure
PC <--> PC <--> PC

#### Benefits
- Low cost
- No central dependency
- Resilient in distributed systems

#### Drawbacks
- Harder to manage
- Security challenges
- Limited centralized control

#### Used for file sharing, VoIP between users, blockchain, and distributed computing.

---

## Network Segmentation
Process of dividing a network into smaller isolated segments.

Improves:
- Performance --> Reduces broadcast traffic and congestion
- Security --> Limits attack spread
- Resource management --> Allows better control over traffic flow

### Methods of Network segmentation:
#### Subnetting
Divides an IP network into smaller logical networks.

Purpose:
- Efficient IP address use
- Reduced broadcast domain size
- Improved routing control

#### Virtual Local Area Network (VLAN)
Logically separates devices within the same physical switch.

Functions:
- Creates separate broadcast domains
- Improves security
- Reduces congestion

#### Even if physically connected to the same switch, devices remain logically separated.

#### Network Segments (Physical Segmentation)
Using separate switches or routers to isolate network areas.
