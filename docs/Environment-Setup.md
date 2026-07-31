# Environment Setup

## Azure Resources

- Azure Subscription
- Resource Group
- Log Analytics Workspace
- Microsoft Sentinel Workspace
- Windows Server Virtual Machine

## Log Sources

### Azure Activity Logs

Collected:

- Administrative events
- Resource creation
- Resource deletion
- RBAC changes
- Subscription activity

### Windows VM Logs

Collected via the Azure Monitor Agent:

- Security Events
- Process Creation
- Authentication Logs
- PowerShell Activity
- Windows Event Logs

## Setup Steps

1. Provisioned an Azure subscription and created a dedicated resource group for the lab.
2. Deployed a Log Analytics Workspace and enabled Microsoft Sentinel on top of it.
3. Connected the Azure Activity Logs data connector to capture subscription-level administrative activity.
4. Deployed a Windows Server virtual machine to act as the target endpoint.
5. Installed the Azure Monitor Agent on the VM and configured a Data Collection Rule to forward Security Events, process creation, authentication, PowerShell, and Windows Event Logs to the workspace.
6. Verified log ingestion in Sentinel before starting attack simulations.

## Cost Management

- Ran the lab on a free/education Azure allowance to keep costs minimal.
- Stopped/deallocated the VM whenever it wasn't actively in use.
- Set a billing budget alert to avoid unexpected charges.
