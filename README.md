# Wazuh-SIEM-Lab
SIEM lab (Wazuh + Palo Alto)
# Lab — SIEM with Wazuh & Palo Alto Syslog

This repository documents **Priyadharshini Rengaramanujam**'s Lab, configuring centralized logging from a **Palo Alto** firewall to **Wazuh SIEM** via **Syslog**, generating test THREAT events, and onboarding an endpoint agent. Lab requirements and steps are captured in the assignment brief and the validation screenshots.

## Repository Contents
- `evidence/Priyadharshini Rengaramanujam_LAB_7.pdf` — Screens showing syslog server profile, log forwarding object, firewall rules, Wazuh THREAT log, and endpoint in manager.
- `BLOG.md` — Lessons learned from implementing SIEM log forwarding and alerting.

## Key Outcomes
- **Syslog Server Profile** configured on Palo Alto targeting `wazuh.iamlab.depaulseclabs.com` over UDP.  
- **Log Forwarding Profile**: Match lists created across log types forwarding to Wazuh.  
- **Security Policies** updated to send logs to Syslog.  
- **Malware test event** blocked; Wazuh shows `data.type: THREAT` in logs.  
- **Wazuh Agent** installed on IAMLAB-VDC; endpoint visible in Endpoint Manager.  

## Tech Stack & Tools
- **Wazuh** (SIEM/Manager)
- **Palo Alto** (Syslog forwarding)
- **Windows** endpoint agent

## Author
**Priyadharshini Rengaramanujam** — Graduate Student (Cybersecurity), DePaul University
