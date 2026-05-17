# Configure Microsoft Entra Cloud Sync Prerequisites

## Overview
Before installing Microsoft Entra Cloud Sync, organizations must complete several prerequisites to ensure secure, reliable, and highly available synchronization between on-premises Active Directory and Microsoft Entra ID.

Key prerequisites include:
- Creating a Group Managed Service Account (gMSA)
- Creating a Hybrid Identity Administrator account
- Preparing a supported provisioning agent server
- Configuring firewall and proxy settings
- Establishing high availability
- Reviewing synchronization limitations and security requirements

---

# Main Prerequisites

Organizations must complete the following tasks before deployment:

- Create the Microsoft Entra Connect Cloud Sync gMSA account
- Create a Hybrid Identity Administrator account
- Identify an on-premises Windows Server 2016 or later server
- Configure high availability with multiple active agents
- Configure firewall and proxy access
- Review NTLM and synchronization limitations

---

# Group Managed Service Account (gMSA)

Microsoft Entra Cloud Sync uses a Group Managed Service Account (gMSA) to securely run the lightweight provisioning agent.

## Benefits of gMSA
A gMSA provides:
- Automatic password management
- Simplified Service Principal Name (SPN) management
- Delegated administration
- Support across multiple servers

The provisioning agent account appears as:
domain\provAgentgMSA$

## Requirements for gMSA

### Active Directory Requirements
- Forest schema must be Windows Server 2012 or later
- At least one domain controller must run Windows Server 2012 or later

### RSAT Requirements
Install PowerShell Remote Server Administration Tools (RSAT) on a domain controller.

RSAT includes:
- Server Manager
- MMC snap-ins
- PowerShell cmdlets
- Administrative consoles
- Command-line management tools

### Server Requirements
The provisioning agent server must:
- Be domain joined
- Run Windows Server 2016 or later

---

# Hybrid Identity Administrator Account

Organizations must create a cloud-only Hybrid Identity Administrator account.

## Requirements
- Must not be a guest account
- Must have Hybrid Identity Administrator permissions

## Purpose
This account:
- Manages Cloud Sync configurations
- Prevents tenant lockout during on-premises outages

## Additional Recommendation
Add and verify custom domain names in Microsoft Entra ID so users can sign in using organizational domains.

---

# Provisioning Agent Server Requirements

The provisioning agent must be installed on a supported server.

## Minimum Requirements
- Windows Server 2016 or later
- Minimum 4 GB RAM
- .NET Framework 4.7.1 or later
- Domain joined

## PowerShell Execution Policy
Configure PowerShell execution policy as:
- RemoteSigned
or
- Undefined

## Additional Requirement
If firewalls exist between servers and Microsoft Entra ID, configure outbound access appropriately.

---

# Firewall and Proxy Requirements

If firewalls or proxies exist between the server and Microsoft Entra ID, configure outbound connectivity.

## Required Ports

| Port | Purpose |
|---|---|
| 80 | Downloads Certificate Revocation Lists (CRLs) |
| 443 | Main outbound communication with Microsoft Entra ID |
| 8080 (Optional) | Agent status reporting if port 443 is unavailable |

## Important Notes
- Allow outbound traffic from Windows services running as Network Service
- Configure proxy settings if internet access requires a proxy

---

# High Availability Recommendations

Microsoft recommends deploying:
- Three active Cloud Sync agents

## Benefits
This provides:
- Automatic failover
- Increased resiliency
- Reduced downtime
- Continuous synchronization availability

## Important Limitation
Although multiple agents can exist:
- Only one agent is active at a time
- Cloud Sync does not support load balancing

---

# NTLM Requirement

Microsoft recommends:
- Disabling NTLM on servers running the provisioning agent

If NTLM is enabled:
- It should be disabled before deployment

---

# Delta Synchronization Limitations

## Group Scope Filtering
- Delta sync does not support groups with more than 50,000 members

## Group Deletion
If a scoped group is deleted:
- Member users may not automatically delete

## OU and Group Renaming
If an OU or group is renamed:
- Cloud Sync may not recognize the rename
- Synchronization may remain healthy without updating properly

---

# Provisioning Log Considerations

Provisioning logs may:
- Display update operations as create operations
- Display create operations as update operations

This can make troubleshooting more difficult.

---

# OU Scoping Filter Limitations

## Supported
- Nested OUs are supported
- Example: One OU containing 130 nested OUs

## Unsupported
- More than 59 separate OUs in a single configuration

---

# Best Practices

Microsoft recommends organizations:
- Use Tier 0 secured servers
- Deploy multiple agents for resiliency
- Use cloud-only Hybrid Identity Administrator accounts
- Disable NTLM wherever possible
- Configure firewall rules correctly
- Monitor synchronization regularly
- Carefully validate OU scoping before production deployment

---

# Summary

Microsoft Entra Cloud Sync is a lightweight, cloud-managed synchronization solution for hybrid identity environments. Proper preparation ensures secure, reliable, and highly available synchronization between on-premises Active Directory and Microsoft Entra ID. Organizations should carefully configure gMSA accounts, provisioning servers, firewall rules, and synchronization scopes to avoid deployment and synchronization issues.
