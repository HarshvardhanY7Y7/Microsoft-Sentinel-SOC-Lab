# MITRE ATT&CK Mapping

## Simulated Techniques

| Technique | ATT&CK ID | Tactic |
|---|---|---|
| PowerShell | T1059.001 | Execution |
| Scheduled Task | T1053.005 | Persistence |
| UAC Bypass | T1548.002 | Privilege Escalation |
| Clear Event Logs | T1070.001 | Defense Evasion |
| LSASS Memory Access | T1003.001 | Credential Access |

## Detection Coverage

| ATT&CK ID | Technique | Detection |
|---|---|---|
| T1059.001 | PowerShell | ✔ |
| T1053.005 | Scheduled Task | ✔ |
| T1548.002 | UAC Bypass | ✔ |
| T1070.001 | Clear Windows Event Logs | ✔ |
| T1003.001 | LSASS Memory Access | ✔ |

Each technique was simulated with Atomic Red Team, detected with a custom Sentinel Analytics Rule, and investigated end-to-end (see [attack-simulations/](../attack-simulations) for the per-technique write-ups).
