# Youngest Brother of Nmap

This script is a simple port scanner written in Python, designed to identify open ports on a given target.

## How It Works

- **Target Definition:** 
  - The script takes a target IP address or hostname as a command-line argument, converting it to its IPv4 format.

- **Execution Overview:** 
  - If the target is valid, it prints a banner with the target information and the time the scan started.
  - It then attempts to connect to ports 78 through 81 on the target.
  - For each port, it checks if the connection is successful:
    - If yes, the port is reported as open.
    - If no response is received within a 1-second timeout, the port is considered closed or unreachable.

## Error Handling

- **Graceful Exit:**
  - The program exits cleanly if interrupted (e.g., with `Ctrl+C`).
  
- **Hostname Resolution:**
  - If the hostname cannot be resolved, the script notifies the user and exits.

- **Socket Errors:**
  - If there’s a socket error, the script handles it and exits.

## Usage

```bash
python3 scanner.py <ip>
