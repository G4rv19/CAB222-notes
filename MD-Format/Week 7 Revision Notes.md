# Week 7 - Application Layer Protocols

## 1. Introduction to the Application Layer
- **Application Layer Role**:
  - The **Application Layer** is the top layer in the OSI model, providing services directly to user applications.
  - It handles protocols that allow different applications to communicate over the network, including web browsing, email, and file transfers.

---

## 2. Domain Name System (DNS)
- **Purpose of DNS**:
  - Converts human-readable domain names (like `example.com`) into IP addresses (like `192.168.1.1`).
  - DNS acts like the internet's "phone book," mapping names to numbers.

- **DNS Structure**:
  - **Root Domain**: Top of the DNS hierarchy, containing all top-level domains (TLDs).
  - **TLDs**: Top-Level Domains, divided into:
    - **Country-Code TLDs (ccTLDs)**: Specific to countries (e.g., `.au` for Australia).
    - **Generic TLDs (gTLDs)**: Represent types of organizations (e.g., `.com`, `.gov`).
  - **Fully Qualified Domain Name (FQDN)**: A complete domain name that specifies an exact location in the DNS hierarchy (e.g., `www.example.com`).

- **DNS Server Roles**:
  - **Authoritative Servers**: Provide information about specific domain names they control.
  - **Non-Authoritative Servers**: Respond with information not originally in their database but found by querying other servers.
  - **Recursive vs. Iterative Queries**:
    - **Recursive**: Local DNS server is responsible for providing a complete answer.
    - **Iterative**: Server provides what information it has, and the client may need to query further.

- **Basic DNS Resolution Process**:
  1. User types a website (e.g., `example.com`) into the browser.
  2. DNS client requests IP from a local DNS server.
  3. Local DNS server queries root servers, TLD servers, and finally, authoritative servers to resolve the IP address.

---

## 3. Hypertext Transfer Protocol (HTTP)
- **Role of HTTP**:
  - The foundation of data communication on the **World Wide Web (WWW)**.
  - **HTTP** is a protocol for transferring hypertext, including images, text, and multimedia.
  - Works on **port 80** and follows a **request-response model** between clients (browsers) and servers.

- **HTTP Basics**:
  - **Request**: The client sends an HTTP request to a server (e.g., `GET /index.html`).
  - **Response**: The server processes the request and sends back a response, including status (e.g., `200 OK`) and content.
  - **URL Structure**: Each web resource is identified by a **Uniform Resource Locator (URL)**, which includes:
    - **Service Type**: (e.g., `http`).
    - **Host Name**: Domain name (e.g., `example.com`).
    - **Path**: Location of the file on the server (e.g., `/page.html`).

- **HTTP Encapsulation**:
  - Data moves through multiple layers: HTTP formats the data, **TCP** handles reliable transmission, **IP** routes the packet, and finally, it’s sent over a network medium.

---

## 4. Simple Mail Transfer Protocol (SMTP) and Email Protocols
- **Email Protocols**:
  - Three main protocols handle email:
    - **SMTP (Simple Mail Transfer Protocol)**: Used to send emails over the Internet (uses port **25**).
    - **POP3 (Post Office Protocol 3)**: Downloads emails from the server to the client and deletes them from the server (uses port **110**).
    - **IMAP4 (Internet Message Access Protocol 4)**: Manages emails directly on the server without downloading (uses port **143**).

- **Email Flow**:
  1. **SMTP**: Sends emails from the client to the email server.
  2. **POP3/IMAP4**: Retrieves emails from the server to the client.

- **Comparison of POP3 and IMAP4**:
  - **POP3**: Good for offline access; emails are stored locally.
  - **IMAP4**: Ideal for online access; emails remain on the server, accessible from multiple devices.

---

## 5. File Transfer Protocol (FTP)
- **Purpose of FTP**:
  - **FTP** allows the transfer of files between a client and a server.
  - It is **not secure** by default, as data (including passwords) is transmitted in plaintext.

- **FTP Operation**:
  - Uses two ports:
    - **Port 21**: For control commands.
    - **Port 20**: For data transfer.
  - **Access Methods**:
    - **Web Browser**: By entering an FTP URL (e.g., `ftp://example.com`).
    - **FTP Client Software**: Specialized tools for managing files over FTP.
    - **Command Line**: Direct command inputs (e.g., `ftp example.com`).

- **Is FTP Still Relevant?**
  - While FTP was revolutionary, it is now largely replaced by secure alternatives like **SFTP** (Secure FTP).

---

## 6. Telnet and Secure Shell (SSH)
- **Telnet**:
  - Enables users to connect to remote devices and execute commands.
  - Operates on **port 23** and is **insecure** as it sends data, including passwords, in plaintext.

- **SSH (Secure Shell)**:
  - **SSH** is a secure alternative to Telnet, encrypting data for safe transmission.
  - Operates on **port 22** and allows secure remote access, commonly used for server management.

- **Common SSH Tools**:
  - **PuTTY**: A popular client program supporting SSH, Telnet, and other remote protocols.

---

## 7. Dynamic Host Configuration Protocol (DHCP)
- **Role of DHCP**:
  - Automatically assigns **IP addresses** to devices on a network, making network configuration easy and efficient.
  - Uses **UDP port 67** for server-side communication and **UDP port 68** for client-side communication.

- **DHCP Lease Process**:
  1. **DHCPDISCOVER**: The client broadcasts a request for an IP.
  2. **DHCPOFFER**: The DHCP server responds with an IP offer.
  3. **DHCPREQUEST**: The client accepts the IP offer.
  4. **DHCPACK**: The server acknowledges and finalizes the lease.

- **Lease Renewal**:
  - The client renews its IP lease when 50% of the lease time has passed. If it fails, it tries again at 87.5% of the lease time.

- **Benefits of DHCP**:
  - Centralized management of IP addresses.
  - Reduced risk of IP conflicts.
  - Simplifies device configuration and network management.

---

## Summary of Key Protocols
| **Protocol**         | **Port** | **Purpose**                                         |
|----------------------|----------|-----------------------------------------------------|
| **DNS**              | 53       | Resolves domain names to IP addresses               |
| **HTTP**             | 80       | Transfers web pages and multimedia files            |
| **SMTP**             | 25       | Sends email messages                                |
| **POP3**             | 110      | Retrieves emails from the server (download/delete)  |
| **IMAP4**            | 143      | Retrieves emails from the server (sync online)      |
| **FTP**              | 20/21    | Transfers files between client and server           |
| **Telnet**           | 23       | Remote command execution (insecure)                 |
| **SSH**              | 22       | Secure remote command execution                     |
| **DHCP**             | 67/68    | Dynamically assigns IP addresses                    |

---


