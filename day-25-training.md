# Day 25 — Python Environment Setup

**Environment:** Kali Linux  
**Main Topic:** Python Environment Setup  
**Focus:** Python, pip, and Virtual Environments

## 1. Learning Notes

Today I learned about setting up a Python development environment and managing Python packages. Python is useful in cybersecurity for automation, data processing, file handling, and building security-related educational projects.

**1. Python**

Python is a programming language known for its readable syntax and wide range of libraries.

It can be used for:
- Automating repetitive tasks.
- Processing files and text.
- Working with network-related data.
- Building simple security tools.
- Developing encryption and hashing projects.

A basic Python command is:

```bash
python3 --version
```

This displays the installed Python version.

**2. pip**

`pip` is Python's package installer. It helps install and manage external Python libraries.

For example:

```bash
python3 -m pip --version
```

This checks the pip version associated with Python 3.

A package can be installed using:

```bash
python3 -m pip install package-name
```

The package name above is a placeholder, not a package I confirmed installing.

**3. Virtual Environments**

A virtual environment is an isolated Python environment for a particular project.

It helps:
- Keep project dependencies separate.
- Avoid conflicts between package versions.
- Make projects easier to reproduce.
- Prevent unnecessary changes to the system Python installation.

Common commands for creating and using a virtual environment are:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

After activation, Python packages can be installed inside that environment.

To leave the virtual environment:

```bash
deactivate
```

**4. requirements.txt**

A `requirements.txt` file records the Python packages a project needs.

For example, a project can list its dependencies and install them in a virtual environment using:

```bash
python3 -m pip install -r requirements.txt
```

This makes it easier for another developer to prepare the same project environment.

## 2. Practical Work and Tools

**What I actually did:**  
I studied Python, pip, and virtual environments and learned the basic commands used to check Python installations, create isolated environments, and manage dependencies. I have not confirmed creating or activating a virtual environment during this session.

**Tools actually used:**
- Kali Linux — learning environment.
- Python 3, pip, and `venv` — topics studied; actual execution is not confirmed.

**Evidence:**  
These learning notes serve as documentation. No terminal screenshots, package installation output, or environment configuration results are confirmed.

## 3. Key Takeaways

- Python is useful for automation and cybersecurity projects.
- pip manages external Python packages.
- Virtual environments isolate project dependencies.
- `requirements.txt` helps document project dependencies.
- Isolated environments help prevent package conflicts.

**Important commands to remember:**

```bash
python3 --version
python3 -m pip --version
python3 -m venv .venv
source .venv/bin/activate
deactivate
```

**Important principle:** Use a separate virtual environment for each Python project instead of installing project dependencies globally.

## 4. Challenges and Questions

One concept I want to understand better is how Python packages are installed and managed separately for different projects.

Questions for further study:
- What is the difference between Python and pip?
- Why should I use `python3 -m pip`?
- How does a virtual environment isolate dependencies?
- What information belongs in `requirements.txt`?
- How can I troubleshoot package installation errors on Kali Linux?

## 5. Reflection

Today I learned that preparing a proper Python environment is an important first step before developing cybersecurity projects. Python provides the programming language, pip manages packages, and virtual environments help keep project dependencies organized.

I want to practice creating and activating a virtual environment and learn how to install project dependencies safely. These skills will help me maintain organized Python projects in my GitHub repository.

## 6. Safety

I will install Python packages only from trusted sources and review unfamiliar dependencies before using them. I will use isolated environments for project work and avoid running unknown scripts. I will never include passwords, API keys, personal data, or private system details in my GitHub repository.
