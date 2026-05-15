# Configure Microsoft Entra Cloud Sync Prerequisites

## Overview
Before installing Microsoft Entra Cloud Sync, organizations must complete several prerequisites to ensure secure, reliable, and highly available synchronization between on-premises Active Directory and Microsoft Entra ID. These prerequisites include configuring a Group Managed Service Account (gMSA), preparing a Hybrid Identity Administrator account, identifying a supported server for the provisioning agent, planning for high availability, and configuring firewall and proxy settings.

## Key Prerequisites for Microsoft Entra Cloud Sync
Organizations must complete the following tasks before deployment:
- Create the Microsoft Entra Cloud Sync gMSA account
- Create a Hybrid Identity Administrator account
- Prepare an on-premises Windows Server 2016 or later server
- Configure high availability with multiple active agents
- Configure firewall and proxy access
- Review NTLM and synchronization limitations

## Group Managed Service Account (gMSA)
Microsoft Entra Cloud Sync uses a Group Managed Service Account (gMSA) to run the lightweight provisioning agent securely.

### Benefits of gMSA
A gMSA provides:
- Automatic password management
- Simplified Service Principal Name (SPN) management
- Delegated management capabilities
- Support across multiple servers

The provisioning agent uses the account in the following format:
domain\provAgentgMSA$

### Requirements for gMSA

#### Active Directory Requirements
- Forest schema must be Windows Server 2012 or later
- At least one domain controller must run Windows Server 2012 or later

#### RSAT Requirements
Install Remote Server Administration Tools (RSAT) PowerShell modules on a domain controller.

RSAT includes:
- Server Manager
- MMC snap-ins
- PowerShell cmdlets
- Administrative command-line tools

#### Server Requirements
The server hosting the provisioning agent must:
- Be domain joined
- Run Windows Server 2016 or later

## Hybrid Identity Administrator Account
Organizations must create a cloud-only Hybrid Identity Administrator account in Microsoft Entra ID.

### Requirements
- Must not be a guest account
- Must have Hybrid Identity Administrator permissions

### Purpose
This account:
- Manages Cloud Sync configurations
- Prevents tenant lockout if on-premises services fail

### Additional Recommendation
Add and verify one or more custom domains in Microsoft Entra ID so users can sign in using organizational domain names.

## Provisioning Agent Server Requirements
The provisioning agent must be installed on a supported server.

### Minimum Requirements
- Windows Server 2016 or later
- Minimum 4 GB RAM
- .NET Framework 4.7.1 or later
- Domain joined

### PowerShell Execution Policy
Configure PowerShell execution policy as:
RemoteSigned
or
Undefined

## Firewall and Proxy Requirements
If firewalls or proxies exist between the server and Microsoft Entra ID, configure outbound access.

### Required Ports

| Port | Purpose |
|---|---|
| 80 | Certificate Revocation List (CRL) validation |
| 443 | Main outbound communication with Microsoft Entra ID |
| 8080 (Optional) | Agent status reporting if 443 is unavailable |

### Important Notes
- Allow outbound traffic from Windows services running as Network Service
- Configure proxy settings if internet access requires a proxy server

## High Availability Recommendations
Microsoft recommends deploying:
- Three active Cloud Sync agents

### Benefits
This configuration provides:
- Automatic failover
- Reduced downtime
- Greater resiliency
- Continuous synchronization availability

### Important Limitation
Although multiple agents can exist:
- Only one agent is active at a time
- The service does not perform load balancing

## NTLM Considerations
Microsoft recommends:
- Disabling NTLM on servers running the provisioning agent

If NTLM is enabled:
- It should be disabled before deployment

## Delta Synchronization Limitations

### Group Scope Filtering
- Delta sync supports groups with fewer than 50,000 members

### Group Deletion
If a scoped group is deleted:
- Member users may not automatically delete

### OU and Group Renaming
If an OU or group is renamed:
- Cloud Sync may not detect the change
- The sync job may remain healthy without updating correctly

## OU Scoping Filter Limitations

### Supported
- Nested OUs are supported
- Example: One OU containing 130 nested OUs

### Unsupported
- More than 59 separate OUs in one configuration

## Provisioning Log Considerations
Provisioning logs may:
- Show update operations as create operations
- Show create operations as update operations

This behavior can make troubleshooting slightly confusing.

## Best Practices
Microsoft recommends organizations:
- Use Tier 0 secured servers
- Deploy multiple agents for resiliency
- Use cloud-only Hybrid Identity Administrator accounts
- Disable NTLM where possible
- Configure firewall rules properly
- Validate OU scoping carefully before production deployment
- Monitor synchronization regularly

## Summary
Microsoft Entra Cloud Sync provides a lightweight, cloud-managed synchronization solution for hybrid identity environments. Proper preparation is essential to ensure reliable provisioning, security, and high availability. Organizations should carefully configure gMSA accounts, provisioning servers, firewall rules, and synchronization scopes before deployment to avoid future synchronization and authentication issues.
