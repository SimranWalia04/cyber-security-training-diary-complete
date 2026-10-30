# Day 08 — Networking Fundamentals
 
**Environment:** Kali Linux

## Topics
- **Main Topic:** Networking Fundamentals
- **Focus:** IP Addresses, Gateways, and Routing

## Learning Notes

Networking allows computers and other devices to communicate and exchange information. Understanding IP addresses, gateways, and routing is important for learning how data travels between devices and networks.

### 1. IP Addresses

An IP address is a numerical address assigned to a device on a network. It helps identify the device and allows data to reach the correct destination.

There are two common IP versions:

- **IPv4:** Uses four groups of numbers separated by dots. Example: `192.168.1.10`.
- **IPv6:** Uses hexadecimal characters separated by colons. Example: `2001:db8::1`.

### 2. Default Gateway

A default gateway is usually a router that connects a local network to other networks, such as the internet.

For example, a computer might have an IP address of `192.168.1.10`, while its default gateway is `192.168.1.1`.

When the computer needs to communicate with a destination outside its local network, it generally sends the traffic through the default gateway.

### 3. Routing

Routing is the process of deciding where network traffic should go. Routers and operating systems use routing tables to determine the next destination for network packets.

Linux provides commands for viewing network information:

- `ip addr` – Displays network interfaces and IP addresses.
- `ip route` – Displays routing table information.
- `ip route show default` – Displays the default route, if configured.

For example, a default route might look like:

```text
default via 192.168.1.1 dev eth0
```

This indicates that traffic without a more specific route is sent through gateway `192.168.1.1` using interface `eth0`. Actual interface names and addresses vary between systems.

## Practical Work and Tools

- **What I actually did:** Studied the concepts of IP addresses, default gateways, and routing. Specific hands-on network configuration or inspection has not been confirmed.
- **Tools actually used:** Kali Linux terminal, if used during the session. No additional networking tools are confirmed.
- **Evidence:** Learning notes about IPv4, IPv6, default gateways, and routing tables. A sanitized screenshot of network information can be added if available.

## Key Takeaways

- IP addresses identify devices on networks.
- IPv4 and IPv6 are two versions of the Internet Protocol.
- A default gateway helps devices communicate with other networks.
- Routing determines where network packets should be sent.
- Routing tables contain information used to select network paths.

**Commands to remember:**

```bash
ip addr
ip route
ip route show default
```

## Challenges and Questions

I am still learning the difference between a device's IP address, its subnet, and its default gateway. I want to understand how Linux decides whether traffic should stay within a local network or travel through a router.

## Reflection

Today, I learned about IP addresses, default gateways, and routing. I understood that an IP address identifies a device on a network, a gateway connects different networks, and routing determines where data should travel. I also learned that Linux provides commands such as `ip addr` and `ip route` to inspect network information. I want to review IPv4 and IPv6 and practise reading routing tables in my Kali Linux environment.

## Safety

Only inspect networks and systems I own or have explicit permission to assess. I will avoid changing network settings without understanding their effects and will never include passwords, keys, personal data, or private network details in my training diary.

