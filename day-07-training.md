# Day 07 — Linux Networking Commands

**Environment:** Kali Linux

## Topics
- **Main Topic:** Linux Networking Commands
- **Focus:** `ip`, `ping`, and `ss`

## Learning Notes

Linux networking commands help users inspect network interfaces, check connectivity, and understand active network connections.

The following commands are useful for basic network inspection:

1. **`ip`** – Displays and manages network interface and routing information.
   - `ip addr` displays network interfaces and their IP addresses.
   - `ip route` displays the system's routing table.

2. **`ping`** – Checks whether another device or host can be reached over a network.
   - Example: `ping -c 4 127.0.0.1` sends four test packets to the local loopback address.
   - It can help identify basic connectivity problems, although some hosts block ping requests.

3. **`ss`** – Displays information about network sockets and connections.
   - `ss -t` displays TCP sockets.
   - `ss -u` displays UDP sockets.
   - `ss -tuln` displays listening TCP and UDP sockets with numerical addresses and ports.

These commands help users understand how their Linux computer communicates with other devices and which network services may be listening for connections.

## Practical Work and Tools

- **What I actually did:** Studied the purpose of Linux networking commands and how they are used for basic network inspection. Specific hands-on network tests have not been confirmed.
- **Tools actually used:** Kali Linux terminal, if used during the session. No additional networking tools are confirmed.
- **Evidence:** Notes explaining IP addresses, network connectivity, socket information, and the purpose of `ip`, `ping`, and `ss`.

## Key Takeaways

- `ip addr` displays network interfaces and IP addresses.
- `ip route` shows how network traffic is routed.
- `ping` helps check basic network connectivity.
- `ss` displays network sockets and connection information.
- Network inspection is an important part of troubleshooting.
- A failed ping does not always mean a device is offline because network filtering may block it.

**Commands to remember:**

```bash
ip addr
ip route
ping -c 4 127.0.0.1
ss -t
ss -u
ss -tuln
```

## Challenges and Questions

I am still learning how to interpret IP addresses, routing information, and listening ports. I want to understand the difference between an IP address and a port number and how to identify normal network connections.

## Reflection

Today, I learned about three important Linux networking commands: `ip`, `ping`, and `ss`. I understood that `ip` provides information about network interfaces and routes, `ping` checks basic connectivity, and `ss` displays network sockets and connections. I want to review IP addresses, ports, and routing tables and practise these commands in my own Kali Linux environment.

## Safety

Only inspect networks and systems I own or have explicit permission to assess. I will use safe connectivity tests, respect network access restrictions, and never include passwords, keys, personal data, or private system details.

