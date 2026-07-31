# Detection Engineering

Custom Analytics Rules were created using KQL. Each rule generated an incident whenever telemetry matched the predefined logic for a simulated technique.

Rules were built for:

- PowerShell execution
- Scheduled Task creation
- Privilege escalation attempts (UAC Bypass)
- Event log clearing
- LSASS memory access

The underlying KQL queries for each rule are in the [kql/](../kql) folder.

## Example Detection Logic

### PowerShell Execution (T1059.001)

**Objective:** Detect suspicious PowerShell usage.

Investigation included:

- Executing user
- Host
- Command line
- Parent process
- Timestamp

### Scheduled Task Creation (T1053.005)

**Objective:** Identify persistence mechanisms.

Evidence collected:

- Task name
- Creator account
- Creation time
- Associated process

### UAC Bypass (T1548.002)

**Objective:** Detect privilege escalation attempts.

Evidence collected:

- Elevated process
- Parent process
- User
- Process tree

### Windows Event Log Clearing (T1070.001)

**Objective:** Detect defence evasion.

Evidence collected:

- Security Event ID
- User
- Time
- Machine

### LSASS Memory Access (T1003.001)

**Objective:** Identify credential dumping behaviour.

Evidence collected:

- Accessing process
- Target process
- User account
- Timestamp
