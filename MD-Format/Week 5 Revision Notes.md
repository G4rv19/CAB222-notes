# Week 5 - Routing: Static and Dynamic Routing

## 1. Introduction to Routing
- **What is Routing?**
  - **Routing** is the process of selecting the best path to send data packets from a source to a destination across networks.
  - Routers are the primary devices used for routing, working at the **Network Layer (Layer 3)** of the OSI model.

- **How Routing Works**:
  - Each packet passes through multiple routers, which forward it closer to the destination based on routing tables.
  - Routing tables in routers store information about possible paths to reach various network destinations.

---

## 2. Routers and Routing Process
- **Router Functions**:
  - Routers connect separate networks and ensure data packets find the optimal path.
  - They do not forward broadcast frames, limiting unnecessary data transmission.

- **Router Interfaces**:
  - Routers must have at least two interfaces (ports) to connect and forward packets between networks.

- **Routing Steps**:
  1. **De-encapsulation**: Strips the Layer 2 frame header to expose the Layer 3 packet.
  2. **Path Selection**: Looks up the best path in the routing table based on the destination IP address.
  3. **Encapsulation and Forwarding**: Encapsulates the packet in a new Layer 2 frame and sends it out via the selected interface.

- **Routing Table Basics**:
  - Routing tables contain **destination networks**, **next-hop information**, **metrics** (costs), and **timestamps**.
  - **Hop Count**: The number of routers a packet passes through, helping to identify shorter paths.

---

## 3. Types of Routing
- **Static Routing**:
  - Manually configured by network administrators.
  - **Advantages**:
    - Simple and predictable for small, stable networks.
    - Low overhead; does not require extra resources for dynamic updates.
  - **Disadvantages**:
    - Not scalable for large or dynamic networks.
    - If a route fails, there’s no automatic rerouting.
  - **Common Use Cases**:
    - Small networks with few routers.
    - Hub-and-spoke topologies where each branch has a single path to the central hub.

- **Dynamic Routing**:
  - Routers automatically learn routes by exchanging information.
  - **Advantages**:
    - Automatically adapts to network changes and reroutes traffic if needed.
    - Suitable for larger, more complex networks.
  - **Disadvantages**:
    - Requires more processing power, memory, and bandwidth for updates.
  - **Components**:
    - **Initialization**: Routers identify directly connected networks.
    - **Sharing and Updating**: Routers exchange route information and update tables periodically or on-demand.

---

## 4. Routing Protocols
- **Static vs. Dynamic Protocols**:
  - Static routes are fixed manually, while dynamic protocols allow routers to discover and update routes automatically.

- **Dynamic Routing Protocol Categories**:
  - **Interior Gateway Protocols (IGP)**: Used within a single organization (e.g., **RIP**, **EIGRP**, **OSPF**).
  - **Exterior Gateway Protocols (EGP)**: Used between organizations (e.g., **BGP**).

- **Distance Vector Algorithm**:
  - **Based on Bellman-Ford Algorithm**:
    - Routers share their entire routing table with neighbors periodically.
    - Each router announces the cost (distance) to reach various networks.
  - **Routing Information Protocol (RIP)**:
    - One of the first Internet protocols, using hop count as a metric and updating every 30 seconds.

- **Link State Algorithm**:
  - **Based on Dijkstra’s Algorithm**:
    - Routers share information only about their directly connected links.
    - Calculates the shortest path to each destination.
  - **Open Shortest Path First (OSPF)**:
    - Uses **Hello messages** to establish neighbor relationships and update link states only when changes occur.

---

## 5. Key Dynamic Routing Protocols
- **Routing Information Protocol (RIP)**:
  - **Operation**: Periodically shares the entire routing table.
  - **Limitations**: Suitable for small networks, as it uses hop count up to 15, which limits scalability.

- **Open Shortest Path First (OSPF)**:
  - **Operation**: Shares only link-state updates (rather than entire tables), minimizing bandwidth use.
  - **Benefits**:
    - Lowers network overhead, quick convergence, and supports large networks.
  - **Process**:
    1. **Hello Messages**: Routers introduce themselves to neighbors.
    2. **Link-State Packets (LSPs)**: Routers share only link information with neighbors.
    3. **Shortest Path Calculation**: Each router calculates the best route to each destination.

- **Enhanced Interior Gateway Routing Protocol (EIGRP)**:
  - **Hybrid Protocol**: Combines features of both distance-vector and link-state protocols.
  - **Benefits**: Provides rapid convergence and maintains backups of primary paths.

- **Border Gateway Protocol (BGP)**:
  - **For External Routing**: Manages how packets are routed across the Internet, between different organizations.
  - **Path Vector Protocol**: Tracks the path of networks to prevent routing loops and ensures data takes the best route.

---

## 6. Routing Table Structure and Simplification
- **Routing Table Entries**:
  - **Directly Connected Networks**: Networks connected directly to the router’s interface.
  - **Remote Networks**: Reachable only through other routers.
  - **Default Routes**: Used when no other specific route is found in the table (e.g., `0.0.0.0/0`).

- **Maintaining Efficient Routing Tables**:
  - **Route Summarization**: Combines multiple routes into a single entry, reducing table size.
  - **Next Hop**: Specifies where packets should go next.
  - **Default Route**: Acts as a "catch-all" for unspecified destinations, guiding packets to a default path.

---

## 7. Summary
| **Static Routing**                               | **Dynamic Routing**                           |
|--------------------------------------------------|-----------------------------------------------|
| **Pros**: Simple setup, low resource use         | **Pros**: Automatically adjusts to changes    |
| **Cons**: No automatic rerouting, not scalable   | **Cons**: Requires more resources, complexity |
| **Best for**: Small networks, single exit points | **Best for**: Large or complex networks       |

---
