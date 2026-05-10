

# Configure Microsoft Entra Connect Sync Prerequisites

## Overview

Before installing Microsoft Entra Connect Sync, organisations must prepare their Microsoft Entra ID tenant, on-premises Active Directory, server environment, accounts, connectivity, and security controls.

Microsoft Entra Connect Sync is used to synchronise identities between:

```text
On-premises Active Directory → Microsoft Entra ID
```

---

# Important Note

Azure Active Directory is now called Microsoft Entra ID.

---

# Microsoft Entra ID Prerequisites

You need a Microsoft Entra tenant before installing Microsoft Entra Connect Sync.

You can manage Microsoft Entra Connect Sync using:

- Microsoft Entra admin center
- Office portal

---

# Verify Your Custom Domain

Before synchronisation, add and verify the domain you plan to use.

Example:

```text
contoso.com
```

Avoid relying only on the default tenant domain:

```text
contoso.onmicrosoft.com
```

---

# Object Limits

| Scenario | Object Limit |
|---|---|
| Default Microsoft Entra tenant | 50,000 objects |
| Verified domain | 300,000 objects |
| More than 300,000 objects | Support case required |
| More than 500,000 objects | Requires Microsoft 365, Entra P1/P2, or EMS licence |

---

# Prepare On-Premises Data

Before synchronising, use the Microsoft IdFix tool to identify:

- Duplicate attributes
- Formatting problems
- Invalid characters
- Incorrect UPNs
- Problematic proxyAddresses

---

# Why IdFix Matters

Directory errors can cause:

- Sync failures
- Duplicate cloud objects
- Incorrect usernames
- Mail flow issues
- Licensing problems

---

# Optional Sync Features to Review

Before installation, decide whether to enable:

- Password Hash Synchronisation
- Password Writeback
- Device Writeback
- Group Writeback
- Exchange hybrid writeback
- Federation
- Pass-through Authentication

---

# On-Premises Active Directory Requirements

---

# Schema and Forest Functional Level

The Active Directory schema version and forest functional level must be:

```text
Windows Server 2003 or later
```

---

# Domain Controller Requirement

The domain controller used by Microsoft Entra Connect Sync must be:

```text
Writable
```

Read-only domain controllers are not supported.

---

# RODC Limitation

Microsoft Entra Connect Sync does not support:

```text
Read-Only Domain Controllers
```

and does not follow write redirects.

---

# Dotted NetBIOS Names

On-premises forests or domains with dotted NetBIOS names are not supported.

Example of unsupported format:

```text
corp.contoso
```

---

# Active Directory Recycle Bin

Microsoft recommends enabling:

```text
Active Directory Recycle Bin
```

This helps recover deleted AD objects.

---

# PowerShell Execution Policy

Microsoft Entra Connect Sync runs signed PowerShell scripts during installation.

Recommended execution policy:

```powershell
RemoteSigned
```

---

# Microsoft Entra Connect Sync Server

The Entra Connect Sync server contains critical identity data.

It must be secured properly.

---

# Multiple Active Sync Servers

Microsoft does not support multiple active Microsoft Entra Connect Sync servers synchronising to a single tenant.

Allowed design:

```text
One active server + staging mode server
```

---

# Tier 0 Security Requirement

The Microsoft Entra Connect Sync server should be treated as:

```text
Tier 0 / Control Plane infrastructure
```

because it controls identity synchronisation.

---

# Server Installation Prerequisites

---

# Supported Server Types

Microsoft Entra Connect Sync can be installed on:

- Domain controller
- Domain-joined member server
- Non-domain joined server

---

# Recommended Operating System

Microsoft recommends:

```text
Windows Server 2022
```

---

# Minimum Supported Operating System

Microsoft Entra Connect Sync must be installed on:

```text
Windows Server 2016 or later
```

---

# .NET Framework Requirement

Minimum required version:

```text
.NET Framework 4.6.2
```

Recommended:

```text
.NET Framework 4.8 or later
```

---

# Unsupported Server Types

You cannot install Microsoft Entra Connect Sync on:

- Small Business Server
- Windows Server Essentials before 2019
- Windows Server Core

---

# GUI Requirement

The server must have:

```text
Full GUI installed
```

Windows Server Core is not supported.

---

# PowerShell Transcription Limitation

If using the Microsoft Entra Connect Sync wizard to manage AD FS configuration:

```text
PowerShell Transcription Group Policy must not be enabled
```

---

# AD FS Deployment Prerequisites

If deploying AD FS, ensure:

- AD FS servers run Windows Server 2012 R2 or later
- Web Application Proxy servers run Windows Server 2012 R2 or later
- Windows Remote Management is enabled
- TLS/SSL certificates are configured
- Name resolution works correctly

---

# Traffic Inspection Warning

You cannot break and analyse traffic between:

```text
Microsoft Entra Connect Sync ↔ Microsoft Entra ID
```

This is unsupported and may disrupt the service.

---

# MFA Trusted Site Requirement

If Hybrid Identity Administrators use MFA, add this URL to trusted sites:

```text
https://secure.aadcdn.microsoftonline-p.com
```

This supports secure Office login content rendering.

---

# Microsoft Entra Connect Health

If using Microsoft Entra Connect Health, ensure its prerequisites are met before deployment.

Connect Health helps monitor:

- Sync servers
- AD FS servers
- Domain controllers

---

# Hardening the Microsoft Entra Connect Sync Server

Microsoft recommends hardening the server to reduce security risks.

---

# Hardening Best Practices

- Treat the server as Tier 0 infrastructure
- Restrict admin access
- Use dedicated privileged accounts
- Use privileged access workstations
- Deny NTLM authentication where possible
- Enable MFA for privileged users
- Use Windows LAPS
- Monitor federation configuration changes
- Disable unnecessary services

---

# Dedicated Privileged Accounts

Administrators should not use highly privileged accounts for:

- Email
- Web browsing
- Daily productivity tasks

Use dedicated admin accounts only for privileged tasks.

---

# Windows LAPS

Windows LAPS helps manage local administrator passwords.

It provides:

- Unique local admin passwords
- Automatic password rotation
- Secure backup of local admin credentials

---

# Privileged Access Workstations

Privileged administrators should use dedicated secure workstations for admin tasks.

This reduces the risk of credential theft.

---

# MFA for Privileged Accounts

Enable MFA for all privileged accounts in:

- Microsoft Entra ID
- On-premises Active Directory

---

# Why MFA Matters

If an attacker gets a privileged password, MFA helps prevent account takeover.

---

# Disable Soft Matching

Soft Matching allows cloud objects to be matched with on-premises objects.

If not required, disable it to reduce security risk.

---

# Disable Hard Match Takeover

Hard Match Takeover allows Microsoft Entra Connect Sync to take over cloud-managed objects.

If not needed, disable it to prevent identity takeover risks.

---

# Staging Mode

Staging mode allows an extra Microsoft Entra Connect Sync server to be installed without actively synchronising changes to Microsoft Entra ID.

---

# Purpose of Staging Mode

Staging mode is used for:

- High availability
- Disaster recovery
- Testing configuration changes
- Migration to a new server
- Safe updates

---

# Staging Mode Rule

Only one Microsoft Entra Connect Sync server can be active.

Other servers can be in:

```text
Staging mode
```

---

# What Staging Mode Does Not Do

A staging server does not actively:

- Export changes to Microsoft Entra ID
- Run password hash sync
- Run password writeback

until promoted.

---

# Real Work Scenario

A company wants to upgrade Microsoft Entra Connect Sync.

They:

1. Install a new server in staging mode.
2. Import the existing configuration.
3. Test synchronisation rules.
4. Validate expected changes.
5. Promote the staging server.
6. Decommission the old active server.

---

# SQL Server Requirements

Microsoft Entra Connect Sync requires SQL Server to store identity data.

---

# Default SQL Option

By default, it installs:

```text
SQL Server 2019 Express LocalDB
```

---

# SQL Express Limit

SQL Express has a:

```text
10 GB size limit
```

This supports approximately:

```text
100,000 objects
```

---

# When to Use Full SQL Server

Use a full SQL Server installation if managing more than:

```text
100,000 objects
```

---

# SQL Server Support

Microsoft Entra Connect Sync supports mainstream supported SQL Server versions up to:

```text
SQL Server 2022
```

---

# Unsupported SQL Platforms

Microsoft Entra Connect Sync does not support:

- Azure SQL Database
- Azure SQL Managed Instance
- SQL Server 2012

---

# SQL Collation Requirement

SQL Server must use:

```text
Case-insensitive collation
```

Supported example:

```text
_CI_
```

Unsupported:

```text
_CS_
```

---

# SQL Instance Requirement

Only one synchronisation engine is supported per SQL instance.

You cannot share a SQL instance with:

- FIM/MIM Sync
- DirSync
- Another Entra Connect Sync engine

---

# Required Accounts

---

# Microsoft Entra Account

You need one of the following:

- Global Administrator
- Hybrid Identity Administrator

---

# Important Account Rule

The account must be:

```text
Work or school account
```

It cannot be a personal Microsoft account.

---

# Active Directory Account

For Express Settings or DirSync upgrade, you need:

```text
Enterprise Administrator
```

permissions.

---

# Connectivity Requirements

---

# DNS Resolution

The Microsoft Entra Connect Sync server needs DNS resolution for:

- Internal AD DS names
- Microsoft Entra endpoints

---

# Required Network Connectivity

The server must connect to:

- All configured domains
- Root domain of all configured forests
- Microsoft Entra endpoints
- Microsoft 365 URLs and IP ranges

---

# Firewall and Proxy

If firewalls or proxies restrict traffic, allow required:

- Microsoft 365 URLs
- Microsoft Entra admin center URLs
- Azure portal URLs where required

---

# TLS Requirement

Microsoft Entra Connect Sync version 2.0 and later requires:

```text
TLS 1.2
```

TLS 1.0 and TLS 1.1 are not supported.

---

# What Happens If TLS 1.2 Is Not Enabled?

Installation fails.

---

# Outbound Proxy Requirement

If using an outbound proxy, update:

```text
C:\Windows\Microsoft.NET\Framework64\v4.0.30319\Config\machine.config
```

with the correct proxy settings.

---

# Proxy Authentication

If the proxy requires authentication:

- Use custom installation settings
- Ensure the service account can authenticate through the proxy

---

# Proxy Timeout Warning

Microsoft Entra ID can take up to:

```text
5 minutes
```

to respond during sync operations.

Set proxy idle timeout to at least:

```text
6 minutes
```

---

# Common Proxy Timeout Symptoms

- Failed directory synchronization
- Delayed synchronization
- Sync errors
- Connectivity issues

---

# Real Work Scenario

A company installs Microsoft Entra Connect Sync behind a proxy.

Sync keeps failing.

The admin discovers the proxy idle timeout is set to 2 minutes.

Fix:

```text
Increase idle timeout to 6 minutes or more
```

---

# Prerequisites Checklist

Before installation, confirm:

- Microsoft Entra tenant exists
- Custom domain is verified
- Object limits are understood
- IdFix has been run
- AD forest functional level is supported
- Writable domain controller is available
- AD Recycle Bin is enabled
- PowerShell execution policy allows scripts
- Server runs Windows Server 2016 or later
- Server has full GUI
- .NET Framework 4.6.2 or later is installed
- TLS 1.2 is enabled
- Required admin accounts are available
- Firewall and proxy rules are configured
- Server is hardened as Tier 0
- SQL requirements are met

---

# Common Mistakes to Avoid

- Installing on unsupported server versions
- Not verifying the custom domain
- Ignoring IdFix errors
- Using a read-only domain controller
- Running multiple active sync servers
- Not enabling TLS 1.2
- Using weak admin access controls
- Leaving privileged accounts without MFA
- Using SQL Express for very large environments
- Forgetting proxy timeout settings

---

# Important Exam Points

- Microsoft Entra Connect Sync requires a Microsoft Entra tenant
- Custom domains should be verified before synchronisation
- Verified domain increases object limit to 300,000
- IdFix should be used before synchronisation
- AD forest functional level must be Windows Server 2003 or later
- RODCs are not supported
- Server must run Windows Server 2016 or later
- Windows Server Core is not supported
- TLS 1.2 is required for version 2.0 and later
- Only one active sync server is supported
- Staging mode supports high availability and disaster recovery
- SQL Express supports approximately 100,000 objects
- The sync server is Tier 0 infrastructure

---

# Common Interview Questions

## Q1: What is required before installing Microsoft Entra Connect Sync?

A Microsoft Entra tenant, verified domain, prepared AD DS, supported server, required accounts, and network connectivity.

---

## Q2: Can you run multiple active Microsoft Entra Connect Sync servers?

No. Only one active server is supported per tenant.

---

## Q3: What is staging mode used for?

High availability, testing, migration, updates, and disaster recovery.

---

## Q4: Does staging mode run password hash sync?

No, not until the server is promoted.

---

## Q5: What is the minimum supported Windows Server version?

Windows Server 2016 or later.

---

## Q6: Is Windows Server Core supported?

No.

---

## Q7: What TLS version is required for Microsoft Entra Connect Sync v2?

TLS 1.2.

---

## Q8: Why should the server be treated as Tier 0?

Because it contains critical identity data and controls synchronization between AD DS and Microsoft Entra ID.

---

# Summary

Microsoft Entra Connect Sync requires careful prerequisite planning.

Key areas include:

- Microsoft Entra tenant readiness
- Custom domain verification
- Active Directory cleanup
- Supported server OS
- PowerShell policy
- SQL planning
- Secure admin accounts
- TLS 1.2 connectivity
- Firewall and proxy configuration
- Server hardening
- Staging mode planning

A secure and well-prepared Microsoft Entra Connect Sync deployment improves hybrid identity reliability, security, and disaster recovery.
