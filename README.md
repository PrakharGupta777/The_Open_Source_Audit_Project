# OSS Audit Capstone Project

**Name:** Prakhar Gupta  
**Registration Number:** 24BCE11168  
**Chosen Software:** Apache HTTP Server  

---

## Project Overview
This repository contains the five shell scripts for my Open Source Software capstone project. [cite_start]The main goal is to demonstrate how open-source tools—specifically **Apache HTTP Server**—interact with a Linux system[cite: 12]. 

[cite_start]Instead of using complex tools, I wrote these in standard Bash using native utilities like `awk`, `grep`, and `du` to keep it simple and effective[cite: 15, 99].

## What the Scripts Do

* **Script 1 (`script1_identity.sh`)**: A system identity fetcher. [cite_start]It uses command substitution to display the kernel version, the logged-in user, OS distribution info, and system uptime [cite: 93-97].
* [cite_start]**Script 2 (`script2_inspector.sh`)**: Checks if Apache (`apache2` or `httpd`) is installed using `dpkg` or `rpm`[cite: 125, 128]. [cite_start]It uses a case statement to provide a quick note on the software's purpose[cite: 141].
* [cite_start]**Script 3 (`script3_auditor.sh`)**: Uses a `for` loop to audit permissions and disk space for standard directories like `/etc` and `/var/log` [cite: 145-147]. [cite_start]It also checks the Apache config folder permissions[cite: 162].
* [cite_start]**Script 4 (`script4_log_analyzer.sh`)**: Reads a log file line-by-line using a `while-read` loop [cite: 163-165]. [cite_start]It counts a specific keyword (like "error") and shows the last 5 matching lines[cite: 184].
* [cite_start]**Script 5 (`script5_manifesto.sh`)**: An interactive script that asks the user three questions about open source and saves the answers into a `.txt` file using output redirection[cite: 185, 186].

## Requirements
* A Linux environment (Ubuntu, Debian, Fedora, etc.).
* Bash shell.
* Apache HTTP Server should be installed for scripts 2 and 3 to show full results.

## How to Run the Code

1.  Open the terminal in the folder where the scripts are saved.
2.  Grant execution permissions:
    ```bash
    chmod +x script1_identity.sh script2_inspector.sh script3_auditor.sh script4_log_analyzer.sh script5_manifesto.sh
    ```
3.  Run scripts 1, 2, 3, and 5:
    ```bash
    ./script1_identity.sh
    ./script2_inspector.sh
    ./script3_auditor.sh
    ./script5_manifesto.sh
    ```
4.  Run script 4 with a log file path as an argument:
    ```bash
    # For Ubuntu:
    ./script4_log_analyzer.sh /var/log/syslog "error"

    # For RedHat/Fedora:
    ./script4_log_analyzer.sh /var/log/messages "error"
    ```
5.  Read the file created by script 5:
    ```bash
    cat manifesto_$(whoami).txt
    ```
