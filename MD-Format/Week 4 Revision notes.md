# Week 4 - Subnetting, Supernetting, and Classless Interdomain Routing (CIDR)

## 1. Introduction to Subnetting
- **What is Subnetting?**
  - Subnetting is the process of dividing a large network into smaller, manageable sub-networks (subnets).
  
- **Why Subnetting is Needed?**
  - **Broadcast Domain Reduction**: Helps reduce network congestion by limiting broadcasts to specific subnets.
  - **Network Organization**: Allows division by department, visitor networks, etc.
  - **Support for WANs**: Enables geographically separated networks to share a network ID.

---

## 2. Understanding Subnetting
- **Subnet Structure**:
  - Subnetting divides the **Host ID** part of an IP address, adding a **Subnet ID** to create a more flexible structure.

- **Subnet Masks**:
  - A **subnet mask** helps define how many bits are used for the network vs. the host.
  - **Example**: A `255.255.255.0` mask on a Class B address splits the 16-bit host ID into an 8-bit subnet ID and an 8-bit host ID.
  
- **Three-Level Address Structure**:
  - By subnetting, we shift from a two-level (network and host) to a three-level structure (network, subnet, and host).
  - **External networks** see only the main network ID, keeping internal subnet structures hidden.

---

## 3. Steps to Calculate Subnet Masks
- **Determining the Subnet Mask**:
  1. **Decide how many subnets are needed**.
  2. **Calculate the number of bits needed**: Use `2^n` (where `n` is the number of bits) to get at least the required number of subnets.
  3. **Borrow bits from the Host ID** to create the Subnet ID.

- **Example**: Creating 4 subnets in a Class C address (`192.168.1.0`):
  - Step 1: A Class C address has a 24-bit network ID and an 8-bit host ID.
  - Step 2: 4 subnets require borrowing 2 bits (since `2^2 = 4`).
  - Step 3: The subnet mask becomes `255.255.255.192` (or `11111111.11111111.11111111.11000000` in binary).

---

## 4. Subnetting Rules
- **IP Address Rules in Subnets**:
  - **Host Bits All Zeros**: Represents the subnet itself.
  - **Host Bits All Ones**: Used as the broadcast address for the subnet.
  
---

## 5. Valid Subnet Addresses Example
- **Example with 4 Subnets**:
  - **Subnet #1**: 193.2.1.0/26 → Range: `193.2.1.1 - 193.2.1.62`
  - **Subnet #2**: 193.2.1.64/26 → Range: `193.2.1.65 - 193.2.1.126`
  - **Subnet #3**: 193.2.1.128/26 → Range: `193.2.1.129 - 193.2.1.190`
  - **Subnet #4**: 193.2.1.192/26 → Range: `193.2.1.193 - 193.2.1.254`

---

## 6. Variable Length Subnet Masking (VLSM)
- **What is VLSM?**
  - **Variable Length Subnet Masking** allows creating subnets of varying sizes within the same network.
  - **Benefits**: Maximizes IP address utilization by creating larger and smaller subnets based on need.

- **VLSM Example**:
  - A company needs 3 subnets for 60 hosts each and 2 subnets for 30 hosts each.
  - Using VLSM, we borrow additional bits from some subnets to adjust their sizes, allowing for a flexible network structure.

---

## 7. Introduction to Supernetting
- **What is Supernetting?**
  - Supernetting combines multiple smaller networks into a single larger network.
  - **Purpose**: Simplifies routing by reducing the number of entries in a routing table, which improves network performance.

- **Benefits of Supernetting**:
  - Reduces **routing table size**, lowering the load on routers.
  - Enhances **network stability** by minimizing routing updates.
  - Lowers **processor and memory requirements** on routers.

- **Supernetting Example**:
  - Aggregating addresses from 210.78.168.0 to 210.78.175.0 using a supernet mask (`255.255.248.0`) allows these networks to be managed as one.

---

## 8. Implementing Supernetting
- **Steps to Implement Supernetting**:
  1. Determine the number of networks to aggregate.
  2. Borrow bits from the network portion to adjust the subnet mask.
  3. Apply a modified mask to treat the group as a single supernetwork.

- **Example Calculation**:
  - A mid-sized organization needs 1000 IP addresses, typically requiring a Class B network.
  - By supernetting four Class C addresses, each with 254 addresses, we reach approximately 1000 addresses with a mask of `255.255.252.0`.

---

## 9. Classless Interdomain Routing (CIDR)
- **What is CIDR?**
  - **CIDR (Classless Interdomain Routing)** provides flexible address allocation without following traditional class boundaries.
  - CIDR uses variable-length subnet masking to divide or aggregate IP addresses based on need.

- **CIDR Notation**:
  - CIDR denotes addresses with a prefix that shows the number of bits used for the network, e.g., `192.168.1.0/24`.
  
- **CIDR Example**:
  - A company needing 500 addresses can use a CIDR block instead of multiple Class C addresses.
  - For instance, `193.2.0.0/23` would provide two Class C ranges (193.2.0.0 to 193.2.1.255), avoiding unnecessary IP address wastage.

---

## 10. Comparing Subnetting and Supernetting
| **Subnetting**                               | **Supernetting**                            |
|----------------------------------------------|---------------------------------------------|
| Divides a large network into smaller networks | Combines multiple smaller networks into a larger one |
| Reduces broadcast domains                    | Reduces routing table entries               |
| Uses host bits for subnet ID                 | Uses network bits to form a larger network  |

---

