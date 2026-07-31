# Lab Architecture

## Overview Diagram

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


## Detection Workflow

Attack Simulation
│
Logs Generated
│
Azure Monitor Agent
│
Log Analytics Workspace
│
Microsoft Sentinel
│
Analytics Rule
│
Incident Created
│
Threat Hunting
│
Investigation
│
MITRE Mapping


## Components

- **Windows Server VM** — the simulated target/victim endpoint where attacker behaviour is generated.
- **Azure Monitor Agent (AMA)** — installed on the VM to forward Security Events, process creation events, authentication logs, PowerShell logs, and Windows Event Logs.
- **Log Analytics Workspace** — central repository that ingests and stores telemetry from both the VM and Azure Activity Logs.
- **Microsoft Sentinel** — layered on top of the workspace, providing Analytics Rules, incident management, and hunting capabilities.
- **Analytics Rules** — custom KQL-based rules that generate incidents when telemetry matches known attack patterns.
- **Incidents** — generated whenever an Analytics Rule fires, triggering the investigation workflow.
- **Threat Hunting** — proactive KQL queries run against the workspace to validate detections and search for related activity.
