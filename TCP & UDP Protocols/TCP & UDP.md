# 🧪 Research & Development: Network Protocols

This document presents a comprehensive overview of key network protocols used in the transport and application layers of the OSI and TCP/IP models. It includes detailed explanations of TCP, UDP, HTTP, HTTPS, and ICMP with practical insights into their workings, features, and applications.

---

## 1. 🔁 TCP (Transmission Control Protocol)

### Overview:
TCP is a **connection-oriented** protocol. It ensures reliable data transmission between devices on a network. It provides mechanisms for establishing a connection, ensuring ordered data delivery, and retransmitting lost packets.

### Key Features:
- Establishes a virtual circuit using a three-way handshake
- Provides error checking and correction
- Maintains data integrity using checksums
- Supports congestion and flow control
- Packets are sequenced and acknowledged

### How It Works:
1. **Three-way handshake**:
   - SYN: Client initiates a connection
   - SYN-ACK: Server acknowledges and responds
   - ACK: Client confirms the connection

2. **Data Transfer**:
   - Segments are numbered and tracked
   - ACKs sent to confirm receipt
   - Timeout and retransmission for reliability

3. **Connection Termination**:
   - FIN/ACK used to gracefully terminate sessions

### Use Cases:
- Web browsing (HTTP/HTTPS)
- Email (SMTP, IMAP, POP3)
- Secure communications (SSH)
- File transfers (FTP, SCP)

---

## 2. 🚀 UDP (User Datagram Protocol)

### Overview:
UDP is a **connectionless**, lightweight protocol that prioritizes speed over reliability. It sends packets without confirming receipt.

### Key Features:
- Minimal overhead
- Suitable for real-time applications
- No ordering or retransmission
- Allows packet loss

### How It Works:
- Sends independent datagrams
- No session setup or teardown
- Suitable for multicasting and broadcasting

### Use Cases:
- Video and audio streaming (YouTube, Zoom)
- Online gaming
- DNS lookups
- VoIP applications

---

## 3. 🌐 HTTP (HyperText Transfer Protocol)

### Overview:
HTTP is the foundation of data communication for the World Wide Web. It defines how messages are formatted and transmitted, and how web servers and browsers should respond.

### Protocol Layer:
- Application Layer (Layer 7 of OSI Model)
- Operates over TCP, typically on port 80

### Key Characteristics:
- Stateless protocol
- Uses request-response model
- Text-based communication

### How It Works:
1. **Client Request**:
   - Methods like GET, POST, PUT, DELETE sent to server
   - Includes headers, optional body

2. **Server Response**:
   - Returns a status code (e.g., 200 OK, 404 Not Found)
   - Provides headers and response body (HTML, JSON, etc.)

3. **Connection Persistence**:
   - HTTP/1.1 supports persistent connections
   - HTTP/2 introduces multiplexing

### Common Headers:
- Content-Type, Content-Length
- User-Agent
- Host

### Example:
```
GET /index.html HTTP/1.1
Host: example.com
```

---

## 4. 🔒 HTTPS (HyperText Transfer Protocol Secure)

### Overview:
HTTPS is a secure version of HTTP that encrypts the communication between client and server using SSL/TLS.

### Protocol Layer:
- Application Layer (uses TCP port 443)

### How It Works:
1. **TLS Handshake**:
   - Client and server agree on encryption protocols
   - Server sends SSL certificate
   - Session keys are generated

2. **Secure Data Transfer**:
   - HTTP messages are encrypted using TLS
   - Ensures end-to-end confidentiality and integrity

### Security Features:
- Encryption via symmetric/asymmetric cryptography
- Authentication through digital certificates
- Data integrity via MAC (Message Authentication Code)

### Use Cases:
- Banking, payment gateways
- Login forms and sensitive data
- Any service requiring encrypted communication

### Benefits:
- Protects against eavesdropping
- Prevents man-in-the-middle attacks
- Enhances user trust (padlock icon in browsers)

---

## 5. 📡 ICMP (Internet Control Message Protocol)

### Overview:
ICMP is a support protocol used for diagnostics and error reporting in network operations. It is used by network devices to send control messages.

### Protocol Layer:
- Network Layer (Layer 3 of OSI Model)

### Key Characteristics:
- Used to send error messages (e.g., destination unreachable)
- Supports utilities like `ping` and `traceroute`
- Not used for data transmission

### How It Works:
- Devices generate ICMP messages in response to network events
- Encapsulated within IP packets
- Types include:
  - Echo Request/Reply (Type 8/0)
  - Destination Unreachable (Type 3)
  - Time Exceeded (Type 11)

### Use Cases:
- `ping`: Sends ICMP Echo Request to check host availability
- `traceroute`: Determines path to destination host
- Network troubleshooting and monitoring

---

## 🔁 Summary Table

| Protocol | OSI Layer | Connection | Reliable | Encrypted | Port | Common Use Cases |
|----------|------------|------------|----------|-----------|------|------------------|
| TCP      | Transport  | Yes        | Yes      | No        | 80,443,25 | Email, HTTP, FTP |
| UDP      | Transport  | No         | No       | No        | 53,67,161 | DNS, Streaming |
| HTTP     | Application| Yes (via TCP) | Yes   | No        | 80   | Web browsing     |
| HTTPS    | Application| Yes (via TCP) | Yes   | ✅ Yes    | 443  | Secure websites  |
| ICMP     | Network    | N/A        | N/A      | No        | N/A  | Ping, Traceroute |

---

> 📘 **Note**:  
> - TCP/UDP are part of the Transport Layer in the OSI model.  
> - HTTP/HTTPS operate at the Application Layer.  
> - ICMP works at the Network Layer, essential for diagnostics, not data transport.

---

**Prepared by:** Parepalli Likhith Sai  
**Internship Domain:** Cloud Infra & Security  
**Submission:** Week 1 Protocol Analysis Task  
**Date:** June 2025
