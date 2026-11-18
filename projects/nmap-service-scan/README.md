
# Network Scanning and Service Enumeration Using Nmap

## Project Overview

This project focuses on performing network scanning and service enumeration using Nmap in an isolated virtual cybersecurity lab.

The purpose of this project is to identify open ports, running services, and service versions on a Metasploitable 2 virtual machine.

## Objective

- Identify open TCP ports on the target machine.
- Discover running network services.
- Identify service versions using Nmap.
- Understand the importance of reconnaissance in penetration testing.

## Environment and Tools

- Kali Linux (Scanning Machine)
- Metasploitable 2 (Target Machine)
- Oracle VirtualBox
- Nmap
- Host-Only Network

## Lab Configuration

| Machine          | IP Address     | Role             |
|------------------|----------------|------------------|
| Kali Linux       | 192.168.56.101 | Scanning Machine |
| Metasploitable 2 | 192.168.56.102 | Target Machine   |

Both virtual machines were configured within a Host-Only network to provide a controlled testing environment.

## Methodology

### Step 1: Verify Network Connectivity

Before scanning, I verified that Kali Linux could communicate with the Metasploitable 2 target.

Command:

```bash
ping -c 4 192.168.56.102
```

### Step 2: Perform Nmap Service Scanning

I used Nmap to identify open TCP ports and detect running service versions.

Command:

```bash
nmap -sV 192.168.56.102
```

### Step 3: Analyse Scan Results

After completing the scan, I reviewed the output to identify open ports, service names, and detected versions.

## Results and Findings

The Nmap scan identified several open ports and running services on the Metasploitable 2 machine.

| Port | Service | Detected Version   |
|------|---------|--------------------|
| 21   | FTP     | vsftpd 2.3.4       |
| 22   | SSH     | OpenSSH 4.7p1      |
| 23   | Telnet  | Linux telnetd      |
| 25   | SMTP    | Postfix smtpd      |
| 53   | DNS     | ISC BIND 9.4.2     |
| 80   | HTTP    | Apache httpd 2.2.8 |

These findings show that the target exposes multiple network services.

However, identifying an open port or service version does not automatically confirm that a vulnerability exists.

Further authorised assessment would be required to verify potential security weaknesses.

## Challenges and Improvements

One challenge was understanding the different services and interpreting the information returned by Nmap.

This project helped me become more familiar with service enumeration and the role of reconnaissance in penetration testing.

In the future, I would improve this project by comparing different Nmap scanning techniques and documenting how scan configurations affect the results.

## Evidence

The Nmap scan output and supporting screenshots will be added to the evidence folder.

## Ethical Considerations

All scanning activities were performed against Metasploitable 2 within my own isolated virtual lab for educational purposes.
