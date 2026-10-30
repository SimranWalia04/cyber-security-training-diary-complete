# Day 09 — TCP, UDP, and Ports

**Environment:** Kali Linux

## Topics
- **Main Topic:** TCP, UDP, and Ports
- **Focus:** Transport Protocols and Service Ports

## Learning Notes

TCP and UDP are two important transport-layer protocols used for communication between devices on a network. They help applications send and receive data.

### 1. TCP (Transmission Control Protocol)

TCP is a connection-oriented protocol. It establishes a connection before transferring data and provides reliable delivery.

Its main features include:
- Ensures data arrives in the correct order.
- Detects missing or corrupted data.
- Retransmits data when necessary.
- Provides reliable communication.

**Example:** Web browsing over HTTPS commonly uses TCP.

### 2. UDP (User Datagram Protocol)

UDP is a connectionless protocol. It sends data without establishing a connection first.

Its main features include:
- Lower communication overhead than TCP.
- Does not guarantee delivery.
- Does not guarantee that packets arrive in order.
- Useful when speed and low delay are important.

**Example:** Some online games and real-time communication applications use UDP.

### 3. Network Ports

A port is a number used to identify a particular application or service communicating over a network.

Common service ports include:

| Port | Protocol | Common service |
|---|---|---|
| 20/21 | TCP | FTP |
| 22 | TCP | SSH |
| 25 | TCP | SMTP |
| 53 | TCP/UDP | DNS |
| 80 | TCP | HTTP |
| 443 | TCP | HTTPS |

A port number helps the operating system direct incoming network traffic to the appropriate application.

### 4. Inspecting Network Connections

Linux provides commands to inspect network sockets and listening services.

- `ss -t` – Displays TCP sockets.
- `ss -u` – Displays UDP sockets.
- `ss -tuln` – Displays listening TCP and UDP sockets using numerical addresses and ports.

## Practical Work and Tools

- **What I actually did:** Studied the differences between TCP and UDP, the purpose of network ports, and common service-port numbers. Specific hands-on network inspection has not been confirmed.
- **Tools actually used:** Kali Linux terminal, if used during the session. No additional networking tools are confirmed.
- **Evidence:** Learning notes comparing TCP and UDP and listing common network service ports.

## Key Takeaways

- TCP provides reliable, ordered data delivery.
- UDP has lower overhead but does not guarantee delivery or ordering.
- Ports identify applications and services on a device.
- Common ports include 22 for SSH, 53 for DNS, 80 for HTTP, and 443 for HTTPS.
- `ss` can help inspect listening ports and network sockets.

**Commands to remember:**

```bash
ss -t
ss -u
ss -tuln
```

## Challenges and Questions

I am still learning why some applications use TCP while others use UDP. I also want to understand how ports help multiple applications communicate through the same network connection and how to identify listening services.

## Reflection

Today, I learned about TCP, UDP, and network ports. I understood that TCP focuses on reliable and ordered delivery, while UDP provides a simpler communication method with less overhead. I also learned that ports help identify network services, with examples such as SSH on port 22 and HTTPS on port 443. I want to review the differences between these protocols and practise reading socket information using the `ss` command.

## Safety

Only inspect networks and systems I own or have explicit permission to assess. I will not attempt unauthorized connections or access to services, and I will never include passwords, keys, personal data, or private system details in my training diary.
