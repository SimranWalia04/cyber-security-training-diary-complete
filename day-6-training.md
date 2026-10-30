# Day 06 — Processes and System Information

**Environment:** Kali Linux

## Topics
- **Main Topic:** Processes and System Information
- **Focus:** Process Listings and System Inspection

## Learning Notes

A process is a program or task that is currently running on a computer. Linux manages processes so that multiple applications and background services can operate at the same time.

Each process has a unique Process ID (PID), which helps the operating system identify and manage it.

Some useful Linux commands for process listings and system inspection include:

1. **`ps`** – Displays information about running processes.
   - Example: `ps` displays processes associated with the current terminal.
   - `ps aux` displays a broader list of running processes.

2. **`top`** – Shows a live view of running processes and system resource usage, such as CPU and memory.

3. **`free -h`** – Displays memory usage in a human-readable format.

4. **`uname -a`** – Displays information about the Linux kernel and system.

5. **`uptime`** – Shows how long the system has been running and provides system load information.

6. **`df -h`** – Displays available and used disk space in a human-readable format.

These commands help users understand what is running on a Linux system and how system resources are being used.

## Practical Work and Tools

- **What I actually did:** Studied the concept of Linux processes, Process IDs, and basic system information. Specific hands-on process inspection has not been confirmed.
- **Tools actually used:** Kali Linux terminal, if used during the session. No additional tools are confirmed.
- **Evidence:** Notes describing process listings, CPU and memory usage, disk space, and system information commands.

## Key Takeaways

- A process is a running program or task.
- Every process has a Process ID (PID).
- `ps aux` provides a list of running processes.
- `top` provides a continuously updating view of system activity.
- `free -h` checks memory usage.
- `df -h` checks disk space.
- System inspection helps identify resource usage and understand system performance.

**Commands to remember:**

```bash
ps
ps aux
top
free -h
uname -a
uptime
df -h
```

## Challenges and Questions

I am still learning how to interpret process information and understand the meaning of CPU and memory usage. I want to learn how to identify unfamiliar processes and understand which ones are important for normal system operation.

## Reflection

Today, I learned about Linux processes and basic system inspection. I understood that running applications are managed as processes and that each process has its own PID. I also learned that commands such as `ps`, `top`, and `free -h` help monitor system activity and resource usage. I want to review process listings and practise reading system information so I can understand how Kali Linux operates in the background.

## Safety

Only inspect systems I own or have explicit permission to assess. I will avoid stopping unfamiliar system processes and will never include passwords, keys, personal data, or private system details in my training diary.

