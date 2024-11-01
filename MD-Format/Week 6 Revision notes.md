# Week 6 - Routing Concepts and Protocols

## 1. Introduction to Routing
- **Definition of Routing**:
  - Routing is the process of moving data packets from one network to another, ensuring they reach their correct destination.
  - This is a critical function of the Internet, allowing devices across different networks to communicate.

- **Role of Routers**:
  - **Routers** are devices designed specifically to perform routing. They operate at the **Network Layer (Layer 3)** of the OSI model.
  - Routers connect separate networks and make decisions about the best path for data packets based on their **routing tables**.

---

## 2. Basic Routing Process
- **Three Main Steps in Routing**:
  1. **De-encapsulation**:
     - The router removes the data link layer headers and trailers from the incoming packet, revealing the network layer (Layer 3) information.
  2. **Routing Decision**:
     - The router examines the **destination IP address** in the packet and uses its **routing table** to find the best path.
  3. **Re-encapsulation and Forwarding**:
     - The router places the network layer packet in a new data link frame for the next network segment and forwards it through the correct interface.

- **Routing Tables**:
  - Routing tables are essential tools for routers, listing possible paths and helping them decide where to forward packets.
  - **Core Elements in Routing Tables**:
    - **Destination Network**: The network address for packet destinations.
    - **Next Hop**: The address of the next router in the path to the destination.
    - **Metric**: A value that indicates the "cost" of the route (e.g., hop count or delay).
    - **Timestamp**: Shows when the routing information was last updated.

---

## 3. Types of Routing
- **Static Routing**:
  - Routes are manually configured by the network administrator.
  - **Advantages**:
    - Simple setup, predictable, and requires less overhead.
    - Effective for small networks with few routers or where paths rarely change.
  - **Disadvantages**:
    - Difficult to manage on large networks.
    - Cannot automatically adapt to network failures.
  - **Best For**:
    - Small networks or networks with a single path to the destination (e.g., hub-and-spoke topologies).

- **Dynamic Routing**:
  - Routers automatically discover and update routes through communication with other routers.
  - **Advantages**:
    - Automatically adapts to changes in network topology, such as new devices or link failures.
    - Ideal for larger, more complex networks.
  - **Disadvantages**:
    - Requires more processing power, memory, and bandwidth.
    - Can be initially more complex to set up.
  - **Process**:
    - **Initialization**: Routers identify directly connected networks.
    - **Information Sharing**: Routers exchange updates about their known routes.
    - **Continuous Updates**: Routers periodically check and adjust routes to ensure the most efficient paths.

---

## 4. Key Routing Protocols
- **Static Routing Protocols**:
  - Requires manual input and adjustments by the network administrator. It is typically used when routes are fixed and rarely change.

- **Dynamic Routing Protocols**:
  - Enable routers to discover paths and adjust routes automatically, using specific algorithms to determine the best path.

- **Types of Dynamic Routing Protocols**:
  - **Interior Gateway Protocols (IGP)**: Used within a single organization (autonomous system).
    - **Examples**: **RIP (Routing Information Protocol)**, **EIGRP (Enhanced Interior Gateway Routing Protocol)**, **OSPF (Open Shortest Path First)**.
  - **Exterior Gateway Protocols (EGP)**: Used between organizations (across autonomous systems).
    - **Example**: **BGP (Border Gateway Protocol)**.

---

## 5. Routing Algorithms
- **Distance Vector Algorithm**:
  - Based on the **Bellman-Ford Algorithm**, this method helps routers determine the best path by sharing their distance to each network.
  - **Routing Information Protocol (RIP)**:
    - A simple distance-vector protocol using hop count as a metric, RIP updates routing tables every 30 seconds.
    - **Limitations**: Suitable for smaller networks due to a maximum hop count of 15.

- **Link State Algorithm**:
  - Based on **Dijkstra’s Least-Cost Algorithm**, routers determine the shortest path by sharing information only about their directly connected links.
  - **Open Shortest Path First (OSPF)**:
    - OSPF calculates the best path by considering link states and only updates when there are changes.
    - **Process**:
      - Routers announce their presence with **Hello messages**.
      - They then send **Link State Advertisements (LSAs)** containing information about their connected networks.
      - Routers use the LSAs to build a network map and calculate the shortest paths to each destination.

- **Path Vector Algorithm**:
  - Used by **Border Gateway Protocol (BGP)**, which is designed for large-scale inter-network routing.
  - **BGP Characteristics**:
    - Uses AS (Autonomous System) paths rather than just hop counts.
    - Ensures reliable routing between organizations by preventing loops and making route selection decisions based on policies.

---

## 6. Routing Table Management
- **Types of Routing Table Entries**:
  - **Directly Connected Networks**: Networks physically connected to the router.
  - **Remote Networks**: Networks reachable through other routers.
  - **Default Routes**: Used as a last resort when there is no specific route for a destination.

- **Routing Table Optimization Techniques**:
  - **Route Summarization**: Combines multiple entries into a single summary route, reducing table size.
  - **Default Routes**: Acts as a catch-all for unspecified destinations, preventing routing tables from growing too large.

---

## 7. Comparison of Static and Dynamic Routing
| **Static Routing**                               | **Dynamic Routing**                           |
|--------------------------------------------------|-----------------------------------------------|
| Simple to set up and maintain                    | Automatically adapts to network changes       |
| Limited to small or stable networks              | Suitable for large, complex networks          |
| No automatic rerouting in case of link failure   | Can detect and reroute around failed paths    |
| Best for predictable and small environments      | Ideal for dynamic, evolving networks          |

---

## 8. Summary of Routing Protocols
- **RIP (Routing Information Protocol)**:
  - Distance-vector protocol, good for small networks, limited by a maximum of 15 hops.
  - **Metric**: Hop count, with periodic updates.

- **EIGRP (Enhanced Interior Gateway Routing Protocol)**:
  - Advanced protocol that balances elements of both distance-vector and link-state protocols.
  - Uses bandwidth and delay metrics, providing quick recovery from network changes.

- **OSPF (Open Shortest Path First)**:
  - Link-state protocol using Dijkstra’s algorithm for efficient routing.
  - Updates only occur with network changes, saving bandwidth and ensuring fast convergence.

- **BGP (Border Gateway Protocol)**:
  - Path vector protocol, essential for internet routing between organizations.
  - Tracks AS paths to prevent loops, enables policy-based routing, and manages routes across multiple organizations.

---
