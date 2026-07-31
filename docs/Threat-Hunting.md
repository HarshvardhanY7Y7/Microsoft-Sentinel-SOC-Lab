# Threat Hunting Process

Each simulation followed the same repeatable workflow:

1. Execute the Atomic Red Team test.
2. Verify the resulting logs reached Sentinel.
3. Hunt the telemetry using KQL.
4. Validate Indicators of Compromise (IOCs).
5. Generate an incident from the matching Analytics Rule.
6. Investigate the evidence.
7. Map the activity to MITRE ATT&CK.
8. Document the findings.

## Investigation Workflow

Each alert was investigated using the following evidence points:

- Event timeline
- User account involved
- Host involved
- Process hierarchy
- Command line execution
- Event IDs
- Parent-child process relationships

## Why This Workflow

Following the same steps for every technique kept the investigations consistent and made it straightforward to compare findings across the five simulated attacks, and to spot gaps in detection coverage or logging before writing up final documentation.
