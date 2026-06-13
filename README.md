> It's like bowling with bumpers. – @ippsec

# AutoRecon

**Author:** Abdullah Saad (Computer Engineering undergrad, UET Taxila)  
**GitHub:** [AbdullahSaad/AutoRecon](https://github.com/AbdullahSaad/AutoRecon)

AutoRecon is a multi‑threaded network reconnaissance tool which performs automated enumeration of services. It is intended as a time‑saving tool for use in CTFs, penetration testing labs (e.g., OSCP), and real‑world engagements.

The tool begins with port scans / service detection. From those results it launches further enumeration scans using a variety of tools (e.g., if HTTP is found, feroxbuster is launched).

Everything is highly configurable. The default configuration performs **no automated exploitation** – keeping the tool safe for exams like OSCP.

## Features

- Multiple targets (IPs, CIDR, hostnames) – IPv6 ready.
- Concurrent scanning across targets and processors.
- Advanced plugin system (custom scans).
- Global & per‑target pattern matching (highlights important info).
- Intuitive directory structure: `exploit/`, `loot/`, `report/`, `scans/`.
- Full logging of commands & errors.
- Config file support, tagging system, timeouts, four verbosity levels.
- Colorised output (can be disabled).

## Installation (on Kali Linux)

```bash
sudo apt update && sudo apt install python3 python3-pip seclists
sudo apt install curl dnsrecon enum4linux feroxbuster gobuster impacket-scripts nbtscan nikto nmap onesixtyone oscanner redis-tools smbclient smbmap snmp sslscan sipvicious tnscmd10g whatweb

# Recommended: pipx
sudo apt install python3-venv
python3 -m pip install --user pipx
python3 -m pipx ensurepath
pipx install git+https://github.com/AbdullahSaad/AutoRecon.git

---

### 2. `autorecon.py` (unchanged in code, but authorship comment added)

```python
#!/usr/bin/python3
# AutoRecon – network reconnaissance tool
# Original work by Abdullah Saad (UET Taxila)
### 2. `autorecon.py` (unchanged in code, but authorship comment added)

```python
#!/usr/bin/python3
# AutoRecon – network reconnaissance tool
# Original work by Abdullah Saad (UET Taxila)

from autorecon.main import main

if __name__ == '__main__':
    main()
from autorecon.main import main

if __name__ == '__main__':
    main()
