# 🧪 Research & Development: Network Protocols

## 1. 🔁 TCP (Transmission Control Protocol)

### Overview:
TCP is a **connection-oriented** protocol. It ensures reliable data transmission between devices on a network.

### Key Features:
- Connection-based
- Data is delivered in **sequence**
- Ensures **reliable** delivery (acknowledgements, retransmissions)
- Slower but **more reliable** than UDP

### How It Works:
1. **Three-way handshake**:
   - Client sends SYN
   - Server responds with SYN-ACK
   - Client replies with ACK

2. **Data Transfer**:
   - Segments are numbered
   - Receiver acknowledges each segment
   - Lost packets are **retransmitted**

3. **Connection Termination**:
   - Uses FIN and ACK flags to close the session

### Use Cases:
- Web browsing (HTTP/HTTPS)
- Email (SMTP, IMAP)
- File transfers (FTP)

---

## 2. 🚀 UDP (User Datagram Protocol)

### Overview:
UDP is a **connectionless** protocol. It focuses on low-latency transmission, without guarantee of delivery.

### Key Features:
- No connection required
- No acknowledgment or retransmission
- Fast but **unreliable**
- Packets may arrive out of order or be lost

### How It Works:
- Sends datagrams without establishing a connection
- No guarantee of delivery or order
- Minimal overhead

### Use Cases:
- Live video/audio streaming
- Online multiplayer gaming
- DNS queries

---

## 3. 🌐 HTTP (HyperText Transfer Protocol)

### Overview:
HTTP is a **stateless** application layer protocol used for transferring web content.

### How It Works:
- Client sends a **request** (e.g., GET, POST) to a web server
- Server sends back a **response** (HTML, JSON, etc.)
- Operates over TCP (usually port 80)

### Characteristics:
- Stateless (each request is independent)
- Text-based protocol
- No encryption

---

## 4. 🔒 HTTPS (HTTP Secure)

### Overview:
HTTPS is HTTP **secured by SSL/TLS encryption**.

### How It Works:
- Establishes a secure connection using **SSL/TLS handshake**
- Encrypts data between client and server
- Operates over TCP (usually port 443)

### Benefits:
- Ensures data **confidentiality**, **integrity**, and **authenticity**
- Widely used for banking, login forms, e-commerce, etc.

---

## 5. 📡 ICMP (Internet Control Message Protocol)

### Overview:
ICMP is used for **diagnostic** and **error-reporting** in networks.

### How It Works:
- Sends control messages (not data)
- Common messages: **echo request/reply** (used in `ping`), **destination unreachable**, **TTL exceeded**

### Use Cases:
- Troubleshooting tools like `ping`, `traceroute`
- Network health monitoring
- Error reporting

---

## 🔁 Summary Table

| Protocol | Layer | Connection | Reliable | Encrypted | Use Case |
|----------|-------|------------|----------|-----------|----------|
| TCP      | Transport | Yes        | Yes      | No        | File transfers, web traffic |
| UDP      | Transport | No         | No       | No        | Streaming, gaming          |
| HTTP     | Application | Yes (via TCP) | Yes | No        | Websites, APIs             |
| HTTPS    | Application | Yes (via TCP) | Yes | **Yes**   | Secure websites, e-commerce|
| ICMP     | Network | N/A        | N/A      | No        | Network diagnostics        |

---

> 📘 **Note**: TCP/UDP operate at the Transport Layer, while HTTP/HTTPS are Application Layer protocols. ICMP is a Network Layer protocol.

