# Day 10 — DNS Basics

**Environment:** Kali Linux

## Topics
- **Main Topic:** DNS Basics
- **Focus:** Name Resolution and DNS Records

## Learning Notes

DNS stands for **Domain Name System**. It is often described as the phonebook of the internet because it translates human-readable domain names into IP addresses that computers use to communicate.

For example, when someone visits `example.com`, the computer uses DNS to find the IP address associated with that domain name.

### 1. Name Resolution

Name resolution is the process of converting a domain name into an IP address.

A simplified DNS lookup works as follows:

1. A user enters a domain name into a browser.
2. The computer checks available cached DNS information.
3. If the answer is not cached, it asks a DNS resolver.
4. The resolver finds the appropriate DNS information.
5. The IP address is returned so the computer can connect to the destination.

### 2. Common DNS Records

DNS uses different record types to store information about domain names.

| Record | Purpose |
|---|---|
| A | Maps a domain name to an IPv4 address |
| AAAA | Maps a domain name to an IPv6 address |
| CNAME | Creates an alias for another domain name |
| MX | Identifies mail servers for a domain |
| NS | Identifies authoritative name servers |
| TXT | Stores text information, often used for domain verification and email security |

### 3. DNS Lookup Commands

Linux provides commands that can help inspect DNS information.

- `nslookup example.com` – Queries DNS information for a domain.
- `dig example.com` – Displays detailed DNS query information.
- `host example.com` – Performs a simple DNS lookup.

These commands are useful for understanding how domain names are resolved.

## Practical Work and Tools

- **What I actually did:** Studied the purpose of DNS, the name-resolution process, and common DNS record types. Specific DNS queries have not been confirmed.
- **Tools actually used:** Kali Linux terminal, if used during the session. No specific DNS lookup tool is confirmed as having been used.
- **Evidence:** Learning notes describing DNS resolution and A, AAAA, CNAME, MX, NS, and TXT records.

## Key Takeaways

- DNS translates domain names into IP addresses.
- DNS makes websites easier to access without remembering numerical addresses.
- A records contain IPv4 addresses, while AAAA records contain IPv6 addresses.
- MX records identify mail servers.
- NS records identify authoritative name servers.
- `nslookup`, `dig`, and `host` are useful DNS inspection commands.

**Commands to remember:**

```bash
nslookup example.com
dig example.com
host example.com
```

## Challenges and Questions

I am still learning how DNS resolvers communicate with authoritative name servers. I also want to understand the difference between A records, CNAME records, and MX records and how DNS caching affects lookup results.

## Reflection

Today, I learned about DNS and how it helps computers translate domain names into IP addresses. I understood that DNS makes internet communication easier and uses different records to store information about domains. I also learned about useful Linux commands such as `nslookup`, `dig`, and `host`. I want to review the DNS resolution process and practise reading different DNS records in my Kali Linux environment.

## Safety

Only inspect systems and domains I own or have permission to assess. I will use DNS queries for learning and troubleshooting, respect network policies, and never include passwords, keys, personal data, or private system details in my training diary.
