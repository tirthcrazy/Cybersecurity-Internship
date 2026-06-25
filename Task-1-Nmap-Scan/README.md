# Task 1: Basic Network Scanning with Nmap

## Objective

The objective of this task was to perform a basic network scan using Nmap to identify open ports and services running on a target machine.

## Tool Used

- Nmap 7.98
- Kali Linux

## Command Executed

```bash
nmap -sV localhost
# Task 1: Basic Network Scanning with Nmap

## Objective

The objective of this task was to perform a basic network scan using Nmap to identify open ports and services running on a target machine.

## Tool Used

- Nmap 7.98
- Kali Linux

## Command Executed

nmap -sV localhost

## Scan Results

The scan was performed on the localhost address (127.0.0.1).

### Findings

- Host Status: Up
- Open Ports Found: 0
- Closed Ports: 1000
- Services Detected: None

### Analysis

Nmap scanned the top 1000 TCP ports on the target machine. No open ports were detected, indicating that no network services were actively listening on the scanned ports.

### Significance

- Open ports allow network services to communicate.
- Closed ports do not accept incoming connections.
- Systems with fewer exposed ports generally have a smaller attack surface.

## Conclusion

The Nmap scan successfully analyzed the localhost system and found no open ports among the 1000 commonly scanned TCP ports.

## Screenshot Evidence

Screenshots of the scan output are included in the screenshots folder.
