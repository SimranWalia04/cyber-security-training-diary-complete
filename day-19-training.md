# Day 19 — System Hardening

**Environment:** Kali Linux  
**Main Topic:** System Hardening  
**Focus:** Updates, Secure Defaults, and Firewall Concepts

## 1. Learning Notes

Today I learned about **system hardening**, which means improving a computer's security by reducing unnecessary features, limiting access, and applying protective settings.

Three important areas of system hardening are:

**1. System Updates**

Operating system and software updates help fix security vulnerabilities, correct bugs, and improve stability.

Examples:
- Installing security updates regularly.
- Keeping applications up to date.
- Removing outdated software that is no longer needed.
- Checking update information before installing packages.

On Debian-based systems such as Kali Linux, package management commonly uses APT.

Some related commands I learned about are:

```bash
sudo apt update
sudo apt upgrade
```

The first command refreshes package information, while the second upgrades installed packages.

**2. Secure Defaults**

Secure defaults mean configuring a system so that unnecessary access and features are disabled unless they are required.

Examples:
- Using strong authentication.
- Avoiding unnecessary administrator privileges.
- Disabling unused services.
- Setting appropriate file permissions.
- Installing software only from trusted sources.

The principle of least privilege from my earlier training is also important here.

**3. Firewall Concepts**

A firewall monitors and controls network traffic according to configured rules.

It can help:
- Allow trusted network connections.
- Block unwanted connections.
- Restrict access to certain services.
- Reduce exposure to network-based threats.

A firewall can filter incoming traffic, outgoing traffic, or both.

On Linux, firewall management may involve tools such as `ufw` or `nftables`. These are examples of tools to learn about, not tools confirmed as used during this session.

## 2. Practical Work and Tools

**What I actually did:**  
I studied the purpose of system hardening, the importance of software updates, secure configuration, and basic firewall concepts. I have not confirmed that I changed system settings, installed updates, or configured firewall rules.

**Tools actually used:**  
No specific system-hardening or firewall tools are confirmed for this session. Kali Linux was the learning environment.

**Evidence:**  
These learning notes serve as documentation. No configuration screenshots, command output, or practical test results are confirmed.

## 3. Key Takeaways

- Regular updates help protect systems against known vulnerabilities.
- Unnecessary services and applications can increase security risks.
- Secure defaults reduce unnecessary access.
- Firewalls help control network traffic.
- Least privilege limits the permissions available to users and applications.

**Important commands to remember:**

```bash
sudo apt update
sudo apt upgrade
```

These commands are used for refreshing package information and upgrading installed packages. Review package changes before confirming an upgrade.

**Important principle:** Keep systems updated, remove unnecessary services, and allow only the access required for normal operation.

## 4. Challenges and Questions

One area I want to understand better is how firewall rules affect network connections without blocking legitimate services.

Questions for further study:
- What is the difference between incoming and outgoing firewall rules?
- How does UFW work on Linux?
- Why should unused services be disabled?
- How can I check whether a system is receiving security updates?
- What is the difference between a firewall and antivirus software?

## 5. Reflection

Today I learned that system hardening is an important part of maintaining a secure computer. Keeping software updated, using secure default settings, limiting unnecessary permissions, and understanding firewall rules can reduce security risks.

I want to review Linux firewall tools and learn how to inspect system services safely in my own practice environment. I also want to understand how to balance security settings with normal system functionality.

## 6. Safety

All system-hardening activities must be performed on systems I own or have explicit permission to manage. I will review firewall rules before changing them and avoid disabling services without understanding their purpose. I will never include passwords, keys, personal data, or private system details in my GitHub repository.
