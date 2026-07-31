 # Microsoft Sentinel SIEM & Threat Hunting Project

## Overview

This project demonstrates the end-to-end workflow of a Security Operations Center (SOC) using Microsoft Sentinel. The objective was to collect security telemetry from Azure and Windows endpoints, create custom detections using Kusto Query Language (KQL), simulate attacker behaviour with Atomic Red Team, investigate alerts, and map findings to the MITRE ATT&CK framework.

The lab replicates how a SOC analyst detects, investigates, and documents security incidents in a cloud environment.

## Objectives

- Deploy Microsoft Sentinel in Azure
- Collect logs from Azure and Windows endpoints
- Simulate attacker behaviour
- Develop custom KQL detection rules
- Perform threat hunting
- Investigate incidents
- Map detections to MITRE ATT&CK
- Document findings and recommendations

## Technologies Used

- Microsoft Azure
- Microsoft Sentinel
- Azure Monitor Agent (AMA)
- Log Analytics Workspace
- Windows Server Virtual Machine
- Kusto Query Language (KQL)
- Atomic Red Team
- PowerShell
- MITRE ATT&CK Framework

## Lab Architecture

Windows Server VM
│
Azure Monitor Agent
│
Log Analytics Workspace
│
Microsoft Sentinel
│
Analytics Rules
│
Incidents
│
Threat Hunting


See [docs/Architecture.md](docs/Architecture.md) for the full breakdown.

## Repository Structure

Microsoft-Sentinel-SOC-Lab/
│
├── README.md
├── docs/
│ ├── Architecture.md
│ ├── Environment-Setup.md
│ ├── Threat-Hunting.md
│ ├── Detection-Rules.md
│ ├── MITRE-Mapping.md
│ └── Lessons-Learned.md
│
├── kql/
│ ├── PowerShell.kql
│ ├── ScheduledTask.kql
│ ├── UACBypass.kql
│ ├── ClearEventLogs.kql
│ └── LSASS.kql
│
├── attack-simulations/
│ ├── T1059.001.md
│ ├── T1053.005.md
│ ├── T1548.002.md
│ ├── T1070.001.md
│ └── T1003.001.md
│
└── LICENSE


## MITRE ATT&CK Coverage

| ATT&CK ID | Technique | Tactic | Detection |
|---|---|---|---|
| T1059.001 | PowerShell | Execution | ✔ |
| T1053.005 | Scheduled Task | Persistence | ✔ |
| T1548.002 | UAC Bypass | Privilege Escalation | ✔ |
| T1070.001 | Clear Windows Event Logs | Defense Evasion | ✔ |
| T1003.001 | LSASS Memory Access | Credential Access | ✔ |

Full mapping details in [docs/MITRE-Mapping.md](docs/MITRE-Mapping.md).

## Skills Demonstrated

- Microsoft Sentinel
- Detection Engineering
- Threat Hunting
- Security Monitoring
- KQL Query Development
- Incident Investigation
- Log Analysis
- Azure Security Monitoring
- MITRE ATT&CK Mapping
- SOC Operations

## Documentation

- [Environment Setup](docs/Environment-Setup.md)
- [Threat Hunting Process](docs/Threat-Hunting.md)
- [Detection Rules](docs/Detection-Rules.md)
- [MITRE ATT&CK Mapping](docs/MITRE-Mapping.md)
- [Lessons Learned](docs/Lessons-Learned.md)

## License

This project is licensed under the terms of the [MIT License](LICENSE).
