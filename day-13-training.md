# Day 13 — Nmap Fundamentals

**Environment:** Kali Linux

## Topics
- **Main Topic:** Nmap Fundamentals
- **Focus:** Network Discovery Concepts in an Authorized Lab

## Learning Notes

Nmap stands for **Network Mapper**. It is a network discovery and security auditing tool used to identify hosts, discover open ports, and gather information about network services.

It is commonly used by cybersecurity professionals to understand devices and services within networks they are authorized to assess.

### 1. Host Discovery

Host discovery is the process of identifying which devices are active on a network.

For example, in an authorized training lab, a security learner may identify which lab machines are available for testing.

### 2. Port Scanning Concepts

A port is a communication endpoint associated with a service on a device.

Nmap can help identify port states, including:

- **Open:** An application is accepting connections on that port.
- **Closed:** The device is reachable, but no application is listening on that port.
- **Filtered:** Network filtering prevents Nmap from determining whether the port is open or closed.

### 3. Service Detection

Service detection helps identify which applications or services are associated with open ports.

For example, a discovered service might indicate that a machine is running an SSH service or a web server.

### 4. Basic Nmap Commands

The following examples are intended only for a personal training machine or an explicitly authorized lab target.

- `nmap --version` – Displays the installed Nmap version.
- `nmap -h` – Displays the help information.
- `nmap 127.0.0.1` – Scans the local computer's loopback address.

Understanding the output is as important as knowing how to run the tool.

## Practical Work and Tools

- **What I actually did:** Studied Nmap's purpose, host discovery, port states, and service identification concepts. A completed network scan has not been confirmed.
- **Tools actually used:** Kali Linux environment. Nmap is the tool studied in this lesson; actual use has not been confirmed.
- **Evidence:** Learning notes explaining Nmap, open/closed/filtered ports, and authorized network discovery.

## Key Takeaways

- Nmap is used for network discovery and security auditing.
- Host discovery helps identify active devices.
- Port scanning provides information about network services.
- Open, closed, and filtered are different port states.
- Service detection helps identify applications running on ports.
- Network scanning must always be authorized.

**Commands to remember:**

```bash
nmap --version
nmap -h
nmap 127.0.0.1
```

## Challenges and Questions

I am still learning how to interpret Nmap scan results and understand the difference between open, closed, and filtered ports. I also want to understand how service detection works and how network firewalls affect scan results.

## Reflection

Today, I learned about Nmap and its role in network discovery and security auditing. I understood that it can help identify active hosts, discover port states, and provide information about network services. I also learned that scan results must be interpreted carefully and that permission is essential before scanning any system. I want to review basic Nmap output and practise using it safely on my own training machine.

## Safety

Only scan systems and networks I own or have explicit permission to assess. I will use a local machine or authorized training lab, avoid scanning public or third-party networks without permission, and never include passwords, keys, personal data, or private system details in my training diary.
