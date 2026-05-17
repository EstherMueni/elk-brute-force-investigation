# ELK Stack SSH Brute Force Investigation

A real SOC investigation report documenting an SSH brute 
force attack detected and investigated using a home 
ELK Stack SIEM environment.

## What Makes This Lab Real

This is not a simulated or copy-pasted report. Every finding 
came from actual tools running on my own Ubuntu server:

- Filebeat shipped real /var/log/auth.log data to ELK
- Hydra generated real brute force attack traffic
- Kibana captured 1713 failed authentication attempts
- Screenshots taken directly from my Kibana dashboard

## Investigation Summary

| Field | Details |
|---|---|
| **Attack Type** | SSH Brute Force |
| **Tool Used** | Hydra with custom wordlists |
| **Total Attempts** | 1713 |
| **Source IP** | 127.0.0.1 |
| **Successful Logins** | ZERO |
| **Detection Method** | ELK Stack SIEM |
| **Outcome** | No breach — attack failed completely |

## Skills Demonstrated

- ELK Stack SIEM configuration and usage
- Filebeat log shipping from /var/log/auth.log
- Real time attack detection in Kibana
- Brute force attack simulation using Hydra
- True positive vs false positive triage
- MITRE ATT&CK framework mapping
- Professional incident report writing
- SSH security hardening recommendations
- NIST incident response methodology

## Tools Used

- Elasticsearch 9.3.2
- Kibana 9.3.2
- Filebeat 9.3.2
- Hydra
- Ubuntu Server
- Linux auth.log

## Lab Environment

All activity performed on owned Ubuntu Server 
virtual machine. Attack tool pointed at 127.0.0.1 
only — never left local environment.

## Repository Structure

```
elk-brute-force-investigation/
│
├── investigation-report.md    — Full investigation report
├── README.md                  — This file
└── evidence/                  — Screenshots from Kibana
    ├── screenshot1.png        — Kibana histogram spike
    ├── screenshot2.png        — Search results 1713 entries
    └── screenshot3.png        — Sample log entry
```
