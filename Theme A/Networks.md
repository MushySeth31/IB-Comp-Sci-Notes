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


