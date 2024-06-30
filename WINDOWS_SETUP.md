# Windows 10 - Environment Setup

### Purpose: 
- This document provides a comprehensive guide for setting up a development environment on Windows 10. 
- It covers essential PowerShell modules, software installations, and Python package installs to ensure a robust and efficient workspace for developers.

## Table of Contents
1. [PowerShell Module Installs](#powershell-module-installs)
1. [Software Installs](#software-installs)
1. [Pip Installs](#pip-installs)
1. [Create Daily Restart Task](#create-daily-restart-task)
1. [References](#references)

# PowerShell Module Installs
1. [posh-git](#posh-git)

## Posh-Git
### What is Posh-Git?
- Posh-git is a PowerShell module that provides Git enhancements, including informative prompts and tab completion for Git commands, making it easier to work with Git in the PowerShell environment.

### Example using posh-git:
```powershell
C:\Users\Desktop\github\references [main ≡ +0 ~1 -0 !]>
```

**PS commands to install/import posh-git:**
```
Install-Module posh-git
Import-Module posh-git
```

**NOTE:** Add `Import-Module posh-git` to $PROFILE script to have it loaded with every powershell instance. Otherwise, you would have to import the module anytime you want to use it.


# Software Installs
1. [Visual Studio IDE](#visual-studio-ide)
1. [VS Code](#vs-code)
1. [PowerShell Latest Version](powershell-latest-vesion)
1. [Git Setup](#git-setup)
1. [Python](#python)
1. [Sysinternals Suite](#sysinternals-suites)
1. [Java Development Kit](#java-development-kit)
1. [Ghidra](#ghidra)
1. [Ncat](#ncat)
1. [WSL 2](#wsl-2)
1. [Wireshark](#wireshark)

## Visual Studio IDE
- [VS IDE Install Link](https://visualstudio.microsoft.com/vs/)

## VS Code
- [VS Code Install Link](https://code.visualstudio.com/docs/?dv=win)

## PowerShell Latest Version
- [PowerShell Latest Link](https://learn.microsoft.com/en-us/powershell/scripting/install/installing-powershell-on-windows?view=powershell-7.4#winget)

## Git Setup
**Open an Administator PowerShell session.**

1. Install Chocolatey
- Chocolatey is a package manager for Windows that simplifies software installation, configuration, and management on Windows machines. It provides a command-line interface (CLI) similar to Linux package managers like apt-get and Homebrew for macOS.
- [Chocolatey Install Link](https://chocolatey.org/install#individual)  

Powershell command to install Chocolatey:
```
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```

2. Install Git
```
choco install git
```

3. Update Path to include Git
```
Add to $PATH environment variable: C:\Program Files\Git\
```

## Python
- I chose `Python 3.10.8 - Windows Installer (64 bit)`
- [Link to Python download page](https://www.python.org/downloads/windows/)

## Sysinterals Suite
[Link to Sysinternals Suite download](https://learn.microsoft.com/en-us/sysinternals/downloads/sysinternals-suite)
- The Sysinternals Troubleshooting Utilities have been rolled up into a single Suite of tools. This file contains the individual troubleshooting tools and help files

## Java Development Kit
[Link to JDK download](https://www.oracle.com/java/technologies/downloads/?er=221886#jdk21-windows)

### What is JDK?
- The JDK (Java Development Kit) is a software development kit used to develop Java applications. It includes the Java Runtime Environment (JRE), an interpreter/loader (Java), a compiler (javac), an archiver (jar), a documentation generator (Javadoc), and other tools needed for Java development.

## Ghidra
1. [Link to Ghidra GitHub](https://ghidra-sre.org/)
1. [Link to Ghidra Install Instructions](https://ghidra-sre.org/InstallationGuide.html#Install)
1. [YouTube Walk Through](https://www.youtube.com/watch?v=nh5Z_Woi7v0&t=154s)

### What is Ghidra?
- Ghidra is a free and open-source software reverse engineering (SRE) framework developed by the National Security Agency (NSA). It helps analyze compiled code on a variety of platforms including Windows, macOS, and Linux. 

## Ncat
[Link to Ncat Install](https://serverspace.io/support/help/how-to-install-ncat-tool-on_windows-and-linux/)

### What is Ncat?
- Ncat is a versatile networking utility, part of the Nmap suite, designed for various network-related tasks. It can be used for debugging, scanning, transferring files, creating network servers, and much more.

## WSL 2
[Link to WSL 2 Install Guide](https://www.omgubuntu.co.uk/how-to-install-wsl2-on-windows-10)

### What is WSL 2 (Windows Subsytem for Linux 2)?
WSL2, or Windows Subsystem for Linux 2, is a compatibility layer for running Linux binary executables natively on Windows 10 and Windows 11. It is an improvement over the original WSL (Windows Subsystem for Linux) in several ways:

- Full Linux Kernel: WSL2 uses a real Linux kernel with Windows, which means it's capable of running all Linux software.

- Performance: WSL2 is significantly faster than WSL1, especially for file system-heavy operations.

- Compatibility: Since WSL2 runs a full Linux kernel, it offers much better compatibility for Linux applications, including support for Docker and other development tools that require full Linux kernel functionality.

- Resource Usage: WSL2 uses a lightweight VM, but it still allows you to control how much memory and CPU it can use, providing a balance between resource usage and performance.

WSL2 provides a way for developers to use a Linux environment directly on Windows without the need for dual-booting or running a full virtual machine.

## Wireshark
[Link to Wireshark Download](https://www.wireshark.org/download.html)

### What is Wireshark?
- Wireshark is an open-source network protocol analyzer and packet sniffer. It can be used to inspect and analyze network traffic.  

- It provides a wealth of information, including the source and destination IP address, protocol type, and even payload contents.

- Wireshark supports many network protocols, including Ethernet, TCP/IP, DNS, HTTP, and many more.

- Wireshark's ability to decode the conversations happening in your network can be a powerful tool for troubleshooting network problems, analyzing performance, or learning more about what's happening in a network. 

# Pip Installs
1. [Pip Version](#pip-version)
1. [Pre-Commit](#pre-commit)
1. [Poetry](#poetry)

### Ensure pip is in your $PATH
- After installing Python, I was still required to add the path to `pip` in addition to the `Python` path.
- Pip was located here (change to meet your specific case):
```
C:\Users\YourUsername\AppData\Local\Programs\Python\Python3X\Scripts
```

### What is PIP?
- `pip` is the package installer for Python. It's a command-line tool that allows you to find, install, and manage Python packages (libraries and frameworks) from the Python Package Index (PyPI) and other package repositories.

## Pip Version
```
python -m pip --version
```

## Pre-Commit
What is pre-commit?
- Is a tool used primarily for managing and maintaining pre-commit hooks in software projects. Pre-commit hooks are scripts or commands that run automatically before a commit is made in a version control system (like Git).

```
pip install pre-commit
```

## Poetry

```
pip install poetry
```

### What is Python Poetry?

Python Poetry is a dependency management and packaging tool for Python projects. It simplifies the process of creating, managing, and publishing Python packages. Here's a brief overview of its key features and functionality:

Dependency Management:
- Poetry uses a pyproject.toml file to specify project dependencies and their versions. This file is similar to a requirements.txt but more structured and versatile.

- It resolves and installs dependencies, ensuring that all required packages and their dependencies are compatible and correctly installed.

Environment Management:
- Poetry can create and manage virtual environments automatically, isolating project dependencies from your system Python or other projects.


Package Building and Publishing:
- Poetry simplifies the process of building and publishing Python packages. It handles the packaging format and can publish packages to PyPI or other repositories with a single command.

Version Management:
- Poetry helps manage project versioning and adheres to semantic versioning principles, making it easier to handle releases and updates.

User-Friendly CLI:
- Poetry provides a command-line interface (CLI) that is intuitive and easy to use, with commands for adding, removing, and updating dependencies, running scripts, and managing environments.

## Create Daily Restart Task

### Purpose:
This Task will restart your system using a custom task.

Some benefits of restarting your computer daily include: 
- Improved Performance: Restarting clears the RAM, stops memory leaks, and closes unnecessary background processes, ensuring your computer runs smoothly.
- Stability: Restarting resets the system state, clearing minor glitches and bugs that can accumulate over time, leading to a more stable and reliable computer.
- Enhanced Security: Regularly applying security updates and closing open sessions reduces vulnerabilities and ensures a secure computing environment.
- Extended Hardware Lifespan: By not running components continuously, restarts can help reduce wear and tear, potentially extending the lifespan of your computer's hardware.
- Improved Network Performance: Restarting reinitializes network connections, which can resolve issues with connectivity and improve overall network performance.

### Steps to Creating Daily Restart Task:

1. Open task manager -> `Win + R`
1. Create Basic Task
1. Name Task: `Daily Restart` > Click `Next`
1. Set Trigger: Choose `Daily`, `Set desired time`, `Recur every set to 1` > Click Next
1. Set Action:  
    - Choose `Start a program` > Click Next
    - Program/script: `shutdown`
    - Add arguments (optional): `/r /f /t 0`
    - Click Next
1. Click `Finish` to set task.

### Argument Explanation:
- `/r`: This argument tells the shutdown command to restart the computer instead of shutting it down.

- `/f`: This forces running applications to close. It will forcefully terminate any running programs without warning the user, which ensures that the restart process isn't blocked by any open applications.

- `/t 0`: This sets the time delay before the restart to 0 seconds. The restart will occur immediately without any countdown or delay.

# References
1. Useful PS links --> [Click Here](https://github.com/janikvonrotz/awesome-powershell)
1. 50 PS Modules to checkout --> [Click Here](https://blog.ironmansoftware.com/50-of-the-top-powershell-modules-to-check-out/)