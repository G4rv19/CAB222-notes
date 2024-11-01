# Week 1 - Introduction to Computer Networks

## 1. Introduction to Computer Networks
- **Purpose of Learning Network History**: 
  - Understanding how networks have evolved provides insight into why certain technologies and protocols exist.
  - Knowing the past helps in understanding the current state of network design, and it’s crucial for troubleshooting and planning for future developments.

---

## 2. Internet History
- **1957**:
  - The **USSR launched Sputnik**, the first artificial Earth satellite. This event prompted the United States to focus on advancing science and technology to remain competitive.
  
- **Establishment of ARPA (1958)**:
  - In response to Sputnik, the U.S. established the **Advanced Research Projects Agency (ARPA)**, intending to advance U.S. technological leadership, eventually leading to the creation of the internet.

- **ARPANET (1969)**:
  - ARPANET was a project by ARPA within the U.S. Department of Defense to create a network that could withstand disruptions, such as during a war.
  - ARPANET’s goal was to connect different computers to communicate and share resources efficiently.
  - **Interface Message Processor (IMP)**:
    - The IMP acted as the first packet-switching node, similar to what we now call a router. IMPs connected different networks, making communication possible between them.
    - This was significant because it marked the first use of packet-switching, which is the basis of internet data transfer today.

- **1974 - TCP Development**:
  - **TCP (Transmission Control Protocol)** was developed to ensure reliable data transmission across networks. TCP was a breakthrough because it allowed data to be broken into packets, transmitted across the network, and reassembled correctly on the receiving end.

- **1983 - TCP/IP Suite**:
  - The transition from **NCP (Network Control Protocol)** to the **TCP/IP suite** created a standard protocol for communication across networks. TCP/IP allowed for reliable data transfer and set the stage for the modern internet.

- **1991-1994 - World Wide Web (WWW)**:
  - **WWW** was created, making it easy for users to browse and access information through a graphical interface.
  - Significant events:
    - **1993**: The U.S. White House launched its official website, [www.whitehouse.gov](http://www.whitehouse.gov), making government information accessible online.
    - **1994**: **Pizza Hut** began online ordering, showcasing the potential of e-commerce.

---

## 3. Network Terminology
- **LAN (Local Area Network)**:
  - A network that connects devices within a limited geographic area, such as an office, school, or campus.
  - LANs are usually privately owned and use high-speed connections for fast data transfer within a short range.

- **WAN (Wide Area Network)**:
  - A network covering a large geographic area, often using external providers like telecommunication companies.
  - WANs are designed to connect LANs over long distances, such as connecting offices in different cities.

- **MAN (Metropolitan Area Network)**:
  - MANs connect LANs within a specific geographic region, such as a city or metropolitan area.
  - Often used to link multiple buildings within a city or region using high-speed connections.

- **Internetwork**:
  - A collection of interconnected networks (LANs and WANs), typically using **routers** to enable communication between them.

- **Internet, Intranet, and Extranet**:
  - **Internet**: A global network of interconnected networks, accessible to anyone with the right access protocols (e.g., TCP/IP, HTTP).
  - **Intranet**: A private network within an organization, accessible only to internal users for secure data and resource sharing.
  - **Extranet**: An extension of an intranet, allowing limited access to external users (e.g., vendors or partners).

---

## 4. Network Communication Units
- **Packets**:
  - A packet is a small unit of data sent across the network.
  - Each packet has **IP addresses** for the source (sender) and destination (receiver), enabling it to navigate through different networks.

- **Frames**:
  - A frame is a packet with additional information, including **MAC (Media Access Control) addresses** that define the hardware addresses of the source and destination within the same local network.

- **Bits**:
  - The smallest unit of data, represented as either `0` or `1`, which corresponds to the electrical signals (off and on) within the physical layer of a network.

---

## 5. Basics of Network Communication
- **Hardware Components**:
  - **NIC (Network Interface Card)**:
    - A hardware component that allows a computer to connect to a network, typically installed inside the computer or as an external adapter.
    - Types:
      - **Wired NIC**: Connects using Ethernet cables.
      - **Wireless NIC**: Connects using Wi-Fi, translating data into radio signals.

  - **Network Medium**:
    - The physical medium through which data travels.
    - Examples include **Ethernet cables** for wired networks and **radio waves** for wireless networks.

  - **Interconnecting Devices**:
    - **Router**: Connects multiple networks, enabling devices on different networks to communicate.
    - **Switch**: Connects devices within the same network, efficiently routing data between them.
    - **Access Point (AP)**: Connects wireless devices to a network, functioning as a bridge between wired and wireless networks.

- **Network Connectivity**:
  - **Peer-to-Peer**: A direct connection between two or more devices where each can communicate without needing a central server.
  - **Star Topology**: A network layout where all devices are connected to a central device, typically a switch or hub.

- **Software Components**:
  - **Network Clients and Servers**:
    - **Client Software**: Requests information or services from a network.
    - **Server Software**: Provides resources or services to client devices on the network.
  - **Protocols**: A set of rules for communication across a network. **TCP/IP** is a fundamental protocol suite used on the internet.
  - **NIC Driver**: Software that enables the NIC to communicate with the operating system and other network components.

---

## 6. Network Architecture
- **Network Architecture**: The layout or design of a network, detailing how devices are interconnected and how data flows between them.
- **Reference Models**:
  - **OSI Model** (7 Layers): A theoretical framework for understanding and designing networks.
  - **TCP/IP Model**: A practical model focused on the protocols for internet communication.

---

## 7. OSI Model Layers
1. **Application Layer (Layer 7)**:
   - Provides services to user applications, like web browsers and email clients.
   - Examples of protocols: **HTTP**, **FTP**, **SMTP**.

2. **Presentation Layer (Layer 6)**:
   - Handles data formatting and translation, ensuring the data can be read by the receiving application.
   - Includes **encryption** and **decryption** of data.

3. **Session Layer (Layer 5)**:
   - Manages sessions or ongoing conversations between devices, including session setup and teardown.
   - Used for functions like **name lookup** and **user logins**.

4. **Transport Layer (Layer 4)**:
   - Manages end-to-end data transfer, breaking data into segments and ensuring error-free delivery.
   - Ensures reliability through **flow control** and **acknowledgments**.

5. **Network Layer (Layer 3)**:
   - Handles logical addressing and routing, using **IP addresses** to navigate data across networks.
   - Devices like **routers** operate at this layer.

6. **Data Link Layer (Layer 2)**:
   - Manages frames and ensures reliable transfer within a local network.
   - MAC addresses and **error detection** codes (e.g., **CRC**) operate at this layer.

7. **Physical Layer (Layer 1)**:
   - Converts bits to physical signals for transmission across a medium (e.g., electrical pulses or light).
   - Components include **cables, connectors, and repeaters**.

---

## 8. Data Encapsulation
- **Encapsulation**:
  - The process of adding control information (headers and trailers) to data as it moves down through the OSI layers, preparing it for network transmission.
  - **Example**: Similar to placing a letter in an envelope, where the envelope has the addresses (control information) while the letter itself is the data.

---
