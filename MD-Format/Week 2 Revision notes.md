# Week 2 - Network Media, NICs, Ethernet, and Wi-Fi

## 1. Network Media
- **Two Main Types of Media**:
  - **Wired Media**: Physical connections, such as cables.
  - **Wireless Media**: Uses airwaves to transmit data, like Wi-Fi.

- **Cable Types**:
  - **Copper Wire**:
    - Transmits data via electrical signals.
    - Used for short to medium distances.
  - **Fiber Optic**:
    - Transmits data as light pulses, immune to electromagnetic interference.
    - Used for high-speed, long-distance communication.

---

## 2. Criteria for Choosing Network Media
- **Bandwidth**:
  - The rate of data transfer, measured in **bits per second (bps)**.
  - Common units:
    - **Mbps** (Megabits per second) and **Gbps** (Gigabits per second).
    - Example conversions: 1 Gbps = 125 MB/s.

- **Distance**:
  - Each cable type has a **maximum segment length**.
  - **Attenuation**: Signal weakening over long distances; repeaters can boost signals.

- **Interference**:
  - Physical and **radio frequency interference (RFI)**, especially in densely populated areas.
  - **Electromagnetic interference (EMI)** from electrical devices like motors or fluorescent lights.

- **Security**:
  - Copper wires are more susceptible to **eavesdropping**.
  - Fiber optics are resistant to interference and harder to tap.

---

## 3. Types of Cables
- **Coaxial Cable**:
  - Once widely used, now mainly for cable TV and internet.
  
- **Twisted-Pair Cable**:
  - **Unshielded Twisted Pair (UTP)**: Commonly used in LANs.
  - **Shielded Twisted Pair (STP)**: Shielded to reduce interference.

- **Fiber Optic Cable**:
  - Composed of a core (glass or plastic) surrounded by cladding.
  - **Single-mode fiber (SMF)**: Longer distance, uses laser light.
  - **Multimode fiber (MMF)**: Shorter distance, uses LED light.

---

## 4. Cable Components and Installation
- **RJ-45 Connectors**:
  - Used in UTP and STP cables to connect devices.
  
- **Cable Termination**:
  - **568A and 568B Standards**: Define wiring schemes.
  - **Straight-through cables**: Same wiring standard on both ends, commonly used in connecting different devices (PC-to-switch).
  - **Crossover cables**: Different wiring standards on each end, used for connecting similar devices (PC-to-PC).

---

## 5. Network Interface Cards (NICs)
- **Purpose**:
  - A **NIC** connects a computer to a network, handling data transmission and reception.

- **Types**:
  - **Wired NICs**: Use Ethernet cables.
  - **Wireless NICs**: Connect via Wi-Fi, require SSID and sometimes security credentials.

- **MAC Address**:
  - Each NIC has a unique **MAC address**, a 48-bit identifier (e.g., `04-40-31-5B-1A-C4`).
  - Used to identify devices within a local network.

- **Functions**:
  - **Receiving Data**: Converts signals to frames, verifies destination, and sends to network protocol if addressed to the NIC.
  - **Sending Data**: Encapsulates data in frames with MAC address, converts to signals, and transmits over the network.

---

## 6. Ethernet Technology
- **Overview**:
  - Used for wired LANs, MANs, and some WANs.
  - Standards governed by **IEEE 802.3**.

- **Speeds**:
  - Ranges from **10 Mbps** to **10 Gbps**.

- **Media Access Control**:
  - **CSMA/CD (Carrier Sense Multiple Access with Collision Detection)**:
    - Devices "listen" to the network before sending data.
    - Collisions are detected and cause retransmission after a delay.

- **Error Handling**:
  - Ethernet uses **Cyclic Redundancy Check (CRC)** for error detection in frames.
  - Damaged frames are discarded without notification.

- **Addressing**:
  - Each device has a **MAC address**; incoming frames are processed if the address matches.

---

## 7. Ethernet Standards
- **10BaseT**: 
  - Operates at 10 Mbps, typically used with Category 3 or higher UTP cabling.

- **100BaseTX**: 
  - Runs at 100 Mbps, commonly used with Category 5 UTP.

- **1000BaseT (Gigabit Ethernet)**:
  - Operates at 1 Gbps, using Category 5 or higher cables.

- **10GBaseT**:
  - 10 Gbps over Category 6A or 7 cables, used in data centers for high-speed connections.

---

## 8. Wireless Networks
- **Benefits**:
  - **Mobility**: Users can move around while connected.
  - **Convenience**: Easy setup, especially in large buildings where cabling is expensive.

- **Wi-Fi Components**:
  - **Wireless Access Point (AP)**: Core of a Wi-Fi network, transmits and receives wireless signals.
  - **Wireless Router**: Combines the AP, switch, and router functions in one device.

- **Wi-Fi Modes**:
  - **Infrastructure Mode**: Uses a central AP.
  - **Ad Hoc Mode**: Direct device-to-device communication, often used for temporary connections.

---

## 9. Wi-Fi Frequencies and Standards
- **2.4 GHz**:
  - Larger coverage area, penetrates obstacles better, but more susceptible to interference.
  
- **5 GHz**:
  - Higher speeds, less interference, but has a smaller coverage area.

- **Wi-Fi Standards**:
  - **802.11b**: Up to 11 Mbps, 2.4 GHz.
  - **802.11g**: Up to 54 Mbps, 2.4 GHz.
  - **802.11n (Wi-Fi 4)**: Up to 600 Mbps, dual-band (2.4/5 GHz).
  - **802.11ac (Wi-Fi 5)**: Up to 3.46 Gbps, 5 GHz.
  - **802.11ax (Wi-Fi 6)**: Up to 9.6 Gbps, supports 2.4, 5, and 6 GHz bands.

---

## 10. Wi-Fi Security
- **Encryption Protocols**:
  - **WEP**: Weakest, easily compromised.
  - **WPA and WPA2**: Improved security over WEP.
  - **WPA3**: Latest, with enhanced protection for open networks.

- **CSMA/CA Protocol**:
  - **Carrier Sense Multiple Access with Collision Avoidance**:
    - Prevents collisions in wireless networks by "requesting" permission to transmit.
    - **RTS/CTS** (Request to Send/Clear to Send) packets help manage communication in busy networks.

---

