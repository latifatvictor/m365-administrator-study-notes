
# Plan for Directory Synchronization Using Microsoft Entra Connect Sync

## Overview

Microsoft Entra Connect Sync enables organisations to synchronize:

- Users
- Groups
- Contacts
- Devices

between:

```text
On-premises Active Directory ↔ Microsoft Entra ID
```

Although Microsoft Entra Cloud Sync is lighter and easier to deploy, Microsoft Entra Connect Sync is still the preferred option for:

- Complex enterprise environments
- Advanced hybrid identity scenarios
- Exchange hybrid deployments
- Advanced synchronization requirements

---

# Why Proper Planning Matters

Before deploying Microsoft Entra Connect Sync, organisations must carefully plan:

- Infrastructure
- Authentication method
- Synchronization scope
- Attribute filtering
- Security
- Connectivity
- Failover
- SQL requirements

Poor planning can lead to:

- Synchronization failures
- Authentication problems
- Security risks
- User sign-in issues
- Complex troubleshooting

---

# Key Planning Questions

Before deployment, organisations should answer the following questions.

---

# 1. Where Will Microsoft Entra Connect Sync Be Installed?

Decide:

- Which server will host Entra Connect Sync
- Whether it will be dedicated
- Whether it meets security requirements

---

# 2. Is High Availability Required?

Determine whether you need:

```text
Failover or staging mode servers
```

for redundancy.

---

# 3. How Many Active Directories Will Be Synchronized?

Decide whether synchronization includes:

- One forest
- Multiple forests
- Complex hybrid environments

---

# 4. What Will Be Synchronized?

Choose whether to synchronize:

- Entire Active Directory
- Specific OUs
- Specific objects
- Specific attributes

---

# 5. Will Filtering Be Used?

Decide whether to use:

- OU filtering
- Domain filtering
- Attribute filtering

---

# Real Work Example

A company may choose to synchronize:

```text
Only corporate users
```

while excluding:

- Service accounts
- Test accounts
- Admin accounts

---

# 6. Which Advanced Features Will Be Enabled?

Decide whether to enable:

- Password Hash Synchronization
- Password Writeback
- Device Writeback
- Pass-Through Authentication
- Federation

---

# Authentication Planning

Authentication choice is one of the most important design decisions.

---

# Option 1 - Password Hash Synchronization (PHS)

## Overview

Microsoft Entra Connect Sync synchronizes:

```text
A cryptographic hash of the password hash
```

to Microsoft Entra ID.

---

# Benefits of PHS

Users can:

- Use the same username and password
- Authenticate to cloud services easily
- Enjoy simplified sign-in

---

# Important Security Point

The actual password is NEVER stored in Microsoft Entra ID.

Only:

```text
A non-reversible cryptographic hash
```

is synchronized.

---

# Real Work Example

A user signs into:

- Microsoft Teams
- Outlook Online
- SharePoint Online

using the same password as on-premises Active Directory.

---

# Option 2 - No Password Hash Synchronization

If organisations do NOT want password hashes stored in Microsoft Entra ID, they must use:

- Active Directory Federation Services (AD FS)
OR
- Pass-Through Authentication (PTA)

---

# Alternative Option

Organisations may also:

```text
Use separate cloud passwords
```

although this is generally less preferred.

---

# Preparation Tasks Before Installation

Before installing Microsoft Entra Connect Sync, several preparation tasks are required.

---

# Microsoft Entra ID Requirements

## Microsoft Entra Tenant Required

You must have:

```text
A Microsoft Entra tenant
```

before deploying synchronization.

---

# Domain Verification

Add and verify your production domain.

Example:

```text
contoso.com
```

instead of only using:

```text
contoso.onmicrosoft.com
```

---

# Object Limits

| Scenario | Object Limit |
|---|---|
| Default tenant | 50,000 |
| Verified domain | 300,000 |
| Larger environments | Support request required |
| More than 500,000 objects | Requires licensing |

---

# Preparing On-Premises Data

Before synchronization:

- Clean up Active Directory
- Validate identities
- Fix formatting issues

---

# Use Microsoft IdFix

Microsoft recommends using:

```text
Microsoft 365 IdFix Tool
```

to identify:

- Duplicate attributes
- Invalid UPNs
- Formatting errors
- Invalid characters

---

# Real Work Example

IdFix may detect:

```text
Duplicate proxyAddresses
```

which would otherwise break synchronization.

---

# Review Optional Synchronization Features

Evaluate whether to enable:

- Password writeback
- Device writeback
- Group writeback
- Exchange hybrid features

---

# Active Directory Requirements

---

# Forest Functional Level

Minimum requirement:

```text
Windows Server 2003
```

or later.

---

# Writable Domain Controllers Required

Microsoft Entra Connect Sync:

```text
DOES NOT support Read-Only Domain Controllers (RODCs)
```

---

# NetBIOS Name Requirement

Microsoft Entra Connect Sync does NOT support:

```text
Dotted NetBIOS names
```

Example of unsupported format:

```text
corp.local.domain
```

---

# Active Directory Recycle Bin

Microsoft strongly recommends enabling:

```text
Active Directory Recycle Bin
```

for easier recovery.

---

# PowerShell Execution Policy

Entra Connect Sync uses PowerShell scripts during installation.

Recommended execution policy:

```powershell
RemoteSigned
```

---

# Microsoft Entra Connect Sync Server Security

The synchronization server contains:

```text
Critical identity data
```

and should be treated as:

```text
Tier 0 infrastructure
```

---

# Security Best Practices

- Restrict admin access
- Harden the server
- Monitor privileged access
- Follow Microsoft's Secure Privileged Access guidance

---

# SQL Server Requirements

Microsoft Entra Connect Sync requires SQL Server.

---

# Default SQL Installation

By default, it installs:

```text
SQL Server 2019 Express LocalDB
```

---

# SQL Express Limitations

SQL Express supports approximately:

```text
100,000 objects
```

due to the:

```text
10 GB database limit
```

---

# When Full SQL Server Is Required

If managing more than:

```text
100,000 objects
```

a full SQL Server installation is recommended.

---

# Supported SQL Versions

Supported up to:

```text
SQL Server 2019
```

---

# Unsupported SQL Platforms

Microsoft Entra Connect Sync does NOT support:

- Azure SQL Database
- Azure SQL Managed Instance

---

# SQL Collation Requirement

SQL Server must use:

```text
Case-insensitive collation (_CI_)
```

Case-sensitive collations (_CS_) are unsupported.

---

# SQL Instance Rule

Only:

```text
One synchronization engine
```

per SQL instance is supported.

---

# Required Accounts

---

# Microsoft Entra Permissions

You need:

- Global Administrator
OR
- Hybrid Identity Administrator

---

# Important Requirement

The account must be:

```text
Work or school account
```

NOT:

```text
Personal Microsoft account
```

---

# Active Directory Permissions

For Express Settings:

```text
Enterprise Administrator
```

permissions are required.

---

# Custom Installations

Custom settings allow:

- Greater flexibility
- More deployment options
- Complex topologies

---

# Connectivity Requirements

---

# DNS Resolution

The Entra Connect server must resolve:

- Internal DNS names
- External Microsoft Entra endpoints

---

# Active Directory Connectivity

The synchronization server requires connectivity to:

- All configured domains
- Forest root domains

---

# Firewall and Proxy Requirements

Required Microsoft 365 URLs and IP ranges must be allowed through:

- Firewalls
- Proxy servers

---

# TLS Requirements

## Important Security Requirement

Microsoft Entra Connect Sync version 2.x requires:

```text
TLS 1.2
```

TLS 1.0 and TLS 1.1 are NOT supported.

---

# Failure Scenario

If TLS 1.2 is not enabled:

```text
Installation fails
```

---

# Outbound Proxy Server Requirements

If using an outbound proxy:

- machine.config must be updated
- Authentication settings may need configuration

---

# Proxy Authentication Consideration

If the proxy requires authentication:

- Service accounts may need permission
- Custom installation settings may be required

---

# Important Timeout Warning

Microsoft Entra ID responses can take:

```text
Up to 5 minutes
```

Proxy idle timeout should be configured for:

```text
At least 6 minutes
```

---

# Common Symptoms of Proxy Timeout Issues

- Failed synchronization
- Delayed sync cycles
- Connectivity errors
- Authentication failures

---

# Hardware Requirements

---

# Minimum Requirements Table

| Number of Objects | CPU | Memory | Disk |
|---|---|---|---|
| <10,000 | 1.6 GHz | 4 GB | 70 GB |
| 10,000–50,000 | 1.6 GHz | 4 GB | 70 GB |
| 50,000–100,000 | 1.6 GHz | 16 GB | 100 GB |
| 100,000–300,000 | 1.6 GHz | 32 GB | 300 GB |
| 300,000–600,000 | 1.6 GHz | 32 GB | 450 GB |
| >600,000 | 1.6 GHz | 32 GB | 500 GB |

---

# Important SQL Requirement

For environments with:

```text
100,000+ objects
```

a full SQL Server installation is recommended.

---

# AD FS and Web Application Proxy Requirements

Minimum requirements:

| Requirement | Value |
|---|---|
| CPU | Dual-core 1.6 GHz+ |
| Memory | 2 GB+ |
| Azure VM | A2 or higher |

---

# Real Enterprise Deployment Example

## Scenario

A global organisation has:

- 250,000 users
- Multiple forests
- Exchange hybrid
- Conditional Access
- Hybrid devices

---

# Recommended Design

- Microsoft Entra Connect Sync
- Full SQL Server
- Password Hash Sync enabled
- Staging mode failover server
- TLS 1.2 enabled
- AD Recycle Bin enabled

---

# Common Mistakes to Avoid

- Using unsupported TLS versions
- Ignoring IdFix cleanup
- Using RODCs
- Forgetting firewall rules
- Not verifying domains
- Using insufficient hardware
- Using SQL Express for massive environments
- Poor server hardening

---

# Important Exam Points

- Microsoft Entra Connect Sync requires careful planning
- Password Hash Sync is Microsoft's recommended authentication method
- SQL Express supports approximately 100,000 objects
- TLS 1.2 is required for Entra Connect Sync v2.x
- The synchronization server is considered Tier 0 infrastructure
- RODCs are unsupported
- IdFix should be used before synchronization
- Proxy timeout should be at least 6 minutes
- Active Directory Recycle Bin is recommended
- Full SQL Server is recommended for larger environments

---

# Common Interview Questions

## Q1: What is the recommended authentication method for Entra Connect Sync?

Password Hash Synchronization (PHS).

---

## Q2: What SQL version is installed by default?

SQL Server 2019 Express LocalDB.

---

## Q3: What is the SQL Express database limit?

10 GB.

---

## Q4: What protocol version is required in Entra Connect Sync v2.x?

TLS 1.2.

---

## Q5: Can Entra Connect Sync use Read-Only Domain Controllers?

No.

---

## Q6: Why should IdFix be used before synchronization?

To identify and correct directory synchronization errors.

---

## Q7: What Active Directory functional level is required?

Windows Server 2003 or later.

---

## Q8: Why is the Entra Connect server considered Tier 0?

Because it contains critical identity infrastructure and synchronization data.

---

# Best Practices

- Use Password Hash Synchronization whenever possible
- Harden the synchronization server
- Enable TLS 1.2
- Use IdFix before deployment
- Verify custom domains before synchronization
- Enable Active Directory Recycle Bin
- Monitor synchronization health
- Use full SQL Server for large environments
- Secure privileged access carefully
- Plan failover and staging mode

---

# Summary

Microsoft Entra Connect Sync is Microsoft's enterprise hybrid identity synchronization solution.

It provides:

- User synchronization
- Group synchronization
- Password synchronization
- Hybrid identity
- Advanced hybrid capabilities

Successful deployment requires careful planning around:

- Authentication
- SQL requirements
- Connectivity
- Security
- Hardware
- Active Directory readiness
- Synchronization scope

A properly planned deployment provides secure, scalable, and reliable hybrid identity management between on-premises Active Directory and Microsoft Entra ID.
