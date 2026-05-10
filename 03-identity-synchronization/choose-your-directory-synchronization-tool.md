

# Choose Your Directory Synchronization Tool

## Overview

Organisations with on-premises Active Directory Domain Services (AD DS) can synchronise their users, groups, and contacts with Microsoft Entra ID.

This creates a:

```text
Hybrid Identity
```

Hybrid identity allows users to access both:

- On-premises resources
- Microsoft 365 cloud services

using the same identity.

---

# Why Directory Synchronization Matters

Most organisations want to:

- Reuse existing Active Directory accounts
- Avoid creating duplicate cloud accounts
- Reduce password management complexity
- Improve user productivity
- Simplify identity governance

---

# Benefits of Hybrid Identity

## Users Benefit From

- Single identity for cloud and on-premises access
- Fewer passwords to remember
- Consistent sign-in experience

---

## Organisations Benefit From

- Easier administration
- Centralized identity management
- Improved security
- Better auditing and governance
- Simplified Microsoft 365 deployment

---

# Identity Governance

Directory synchronization is part of:

```text
Identity Governance
```

Identity governance ensures:

- The right people have the right access
- To the right resources
- At the right time

---

# Microsoft Entra ID Role

Microsoft Entra ID acts as the cloud identity platform that connects:

- HR systems
- On-premises directories
- SaaS applications
- Microsoft 365 services

---

# Two Directory Synchronization Tools

Microsoft provides two primary synchronization solutions:

| Tool | Description |
|---|---|
| Microsoft Entra Connect Sync | Traditional on-premises synchronization solution |
| Microsoft Entra Cloud Sync | Modern lightweight cloud-managed synchronization solution |

---

# Microsoft Entra Connect Sync

## Overview

Microsoft Entra Connect Sync is the traditional hybrid identity synchronization tool.

It is installed:

- On-premises
- Usually on a domain-joined server
- Sometimes on a domain controller

---

# Key Requirement

Microsoft Entra Connect Sync requires:

```text
Outbound HTTPS connection to Microsoft 365
```

---

# Main Purpose

It synchronizes:

- Users
- Groups
- Contacts
- Devices

between:

```text
On-premises AD DS ↔ Microsoft Entra ID
```

---

# Advantages of Microsoft Entra Connect Sync

## Supports Complex Environments

Ideal for:

- Large enterprises
- Multiple forests
- Advanced hybrid identity scenarios

---

## Rich Feature Set

Supports:

- Password hash synchronization
- Pass-through authentication
- Federation
- Device writeback
- Group writeback
- Advanced attribute customization

---

# Challenges of Microsoft Entra Connect Sync

## Infrastructure Requirements

May require:

- Dedicated server
- SQL Server for larger environments
- Ongoing maintenance

---

## Complexity

Can be:

- More difficult to configure
- More expensive to maintain
- More resource intensive

---

# Important Features of Entra Connect Sync

---

# 1. Filtering

Allows organisations to limit synchronized objects.

Can filter by:

- Domains
- OUs
- Attributes

---

# Real Work Example

An organisation only wants to synchronize:

```text
OU=CorporateUsers
```

but not:

```text
OU=ServiceAccounts
```

Filtering allows this.

---

# 2. Password Hash Synchronization (PHS)

Synchronizes password hashes from AD DS to Microsoft Entra ID.

Users:

- Use the same password everywhere
- Manage passwords on-premises

---

# Key Benefit

Users only need:

```text
One username + one password
```

---

# 3. Password Writeback

Allows users to:

- Reset passwords in the cloud
- Write the password back to on-premises AD DS

---

# Real Work Scenario

A user resets their password using:

```text
Self-Service Password Reset (SSPR)
```

The new password updates:

- Microsoft Entra ID
- On-premises Active Directory

---

# 4. Device Writeback

Writes Microsoft Entra registered devices back to on-premises AD DS.

Useful for:

- Conditional Access
- Hybrid device scenarios

---

# 5. Preventing Accidental Deletes

Protects against mass deletion synchronization accidents.

Default limit:

```text
500 deletes per sync cycle
```

---

# Why This Matters

If an administrator accidentally deletes a large OU:

- Entra Connect blocks mass deletion sync
- Cloud users are protected

---

# 6. Automatic Upgrade

Keeps Microsoft Entra Connect Sync updated automatically.

Enabled by default for:

```text
Express installations
```

---

# Microsoft Entra Connect Sync Components

## 1. Synchronization Services

Responsible for:

- Synchronizing users
- Synchronizing groups
- Synchronizing identity information

---

## 2. Microsoft Entra Connect Health

Provides:

- Health monitoring
- Alerts
- Reporting
- Visibility in Microsoft Entra admin center

---

# Real Work Scenario

An administrator notices users are not synchronizing.

Microsoft Entra Connect Health shows:

```text
Synchronization service stopped
```

The admin restarts the service and synchronization resumes.

---

# Microsoft Entra Cloud Sync

## Overview

Microsoft Entra Cloud Sync is Microsoft's modern lightweight synchronization solution.

It synchronizes:

- Users
- Groups
- Contacts

from:

```text
On-premises AD DS → Microsoft Entra ID
```

---

# Major Difference

Unlike Entra Connect Sync:

- Configuration is stored in the cloud
- Provisioning occurs in the cloud
- Uses lightweight agents

---

# Lightweight Agent Model

Instead of deploying a heavy synchronization server:

- Small agents are installed on-premises
- Microsoft manages provisioning in the cloud

---

# Benefits of Cloud Sync

---

# 1. Lower Cost

Cloud Sync reduces:

- Server requirements
- SQL licensing costs
- Maintenance overhead

---

# 2. Easier Deployment

Cloud Sync:

- Is simpler to configure
- Uses lightweight agents
- Has streamlined setup

---

# 3. High Availability

Supports:

```text
Multiple agents
```

for resiliency and failover.

---

# Important Note

Cloud Sync does NOT load balance agents.

Only:

```text
One active agent
```

is used at a time.

---

# 4. Faster Synchronization

Cloud Sync synchronizes changes more frequently.

Advantage:

```text
No 30-minute wait
```

commonly associated with Entra Connect Sync.

---

# 5. Better for Disconnected Forests

Ideal for:

- Mergers
- Acquisitions
- Isolated networks

where forests have:

```text
No direct connectivity
```

---

# Real Work Scenario

A company acquires another business.

The acquired company:

- Has isolated Active Directory forests
- Has no VPN connectivity

Cloud Sync agents can be installed separately in each forest and synchronize independently to Microsoft Entra ID.

---

# Side-by-Side Support

Organisations can use:

```text
Cloud Sync + Entra Connect Sync
```

together.

---

# Key Difference Between the Two Tools

| Feature | Entra Connect Sync | Entra Cloud Sync |
|---|---|---|
| Provisioning configuration location | On-premises | Cloud |
| Provisioning engine location | On-premises server | Microsoft cloud |
| Infrastructure requirement | Higher | Lower |
| Setup complexity | More complex | Simpler |
| Maintenance | Higher | Lower |

---

# Feature Comparison

| Feature | Entra Connect Sync | Entra Cloud Sync |
|---|---|---|
| Single forest support | Yes | Yes |
| Multiple forests | Yes | Yes |
| Disconnected forests | No | Yes |
| Lightweight agent | No | Yes |
| Multiple active agents | No | Yes |
| LDAP directory support | Yes | No |
| User synchronization | Yes | Yes |
| Group synchronization | Yes | Yes |
| Contact synchronization | Yes | Yes |
| Device synchronization | Yes | No |
| Password Hash Sync | Yes | Yes |
| Pass-Through Authentication | Yes | No |
| Federation | Yes | Yes |
| Seamless SSO | Yes | Yes |
| Password writeback | Yes | Yes |
| Device writeback | Yes | No |
| Group writeback | Yes | No |
| Advanced attribute customization | Yes | No |
| Exchange hybrid writeback | Yes | No |
| SQL dependency for large environments | Possible | No |

---

# When to Choose Entra Connect Sync

Choose Entra Connect Sync when:

- You need advanced hybrid features
- You require device writeback
- You use Exchange hybrid
- You need advanced attribute flows
- You use Pass-Through Authentication
- You require LDAP integration
- You have complex enterprise requirements

---

# When to Choose Entra Cloud Sync

Choose Entra Cloud Sync when:

- You want simplified deployment
- You want lower maintenance
- You need lightweight agents
- You have disconnected forests
- You want faster synchronization
- You prefer cloud-managed provisioning
- You want lower infrastructure costs

---

# Real Enterprise Scenario

## Scenario 1 - Large Enterprise

A global organisation has:

- Multiple forests
- Exchange hybrid
- Device writeback
- Advanced identity requirements

Best choice:

```text
Microsoft Entra Connect Sync
```

---

## Scenario 2 - Medium Business

A company wants:

- Simple synchronization
- Minimal infrastructure
- Fast setup
- Lower support overhead

Best choice:

```text
Microsoft Entra Cloud Sync
```

---

# Authentication Support Comparison

| Authentication Method | Connect Sync | Cloud Sync |
|---|---|---|
| Password Hash Sync | Yes | Yes |
| Pass-Through Authentication | Yes | No |
| Federation | Yes | Yes |
| Seamless SSO | Yes | Yes |

---

# Synchronization Frequency

| Tool | Sync Speed |
|---|---|
| Entra Connect Sync | Typically every 30 minutes |
| Entra Cloud Sync | More frequent cloud-based synchronization |

---

# Infrastructure Comparison

| Requirement | Entra Connect Sync | Entra Cloud Sync |
|---|---|---|
| Dedicated server | Usually required | Not required |
| SQL Server | May be required | Not required |
| Maintenance effort | Higher | Lower |
| On-prem footprint | Larger | Smaller |

---

# Important Exam Points

- Microsoft Entra Connect Sync is the traditional synchronization solution
- Cloud Sync is the newer lightweight synchronization solution
- Entra Connect Sync stores configuration on-premises
- Cloud Sync stores configuration in the cloud
- Cloud Sync uses lightweight agents
- Entra Connect Sync supports advanced hybrid features
- Cloud Sync is easier to deploy and maintain
- Password Hash Sync is supported by both tools
- Pass-Through Authentication is only supported by Entra Connect Sync
- Device writeback is only supported by Entra Connect Sync
- Cloud Sync supports disconnected forests
- Entra Connect Sync may require SQL Server for large deployments

---

# Common Interview Questions

## Q1: What are the two Microsoft directory synchronization tools?

- Microsoft Entra Connect Sync
- Microsoft Entra Cloud Sync

---

## Q2: Which tool uses lightweight agents?

Microsoft Entra Cloud Sync.

---

## Q3: Which tool supports Pass-Through Authentication?

Microsoft Entra Connect Sync.

---

## Q4: Which tool is easier to deploy?

Microsoft Entra Cloud Sync.

---

## Q5: Which tool supports advanced hybrid features like device writeback?

Microsoft Entra Connect Sync.

---

## Q6: Which tool is better for disconnected forests?

Microsoft Entra Cloud Sync.

---

## Q7: Where is provisioning configuration stored in Cloud Sync?

In the cloud.

---

## Q8: Where does provisioning run in Entra Connect Sync?

On the on-premises synchronization server.

---

# Best Practices

- Use Cloud Sync for simpler environments
- Use Entra Connect Sync for complex enterprise requirements
- Enable Password Hash Sync whenever possible
- Monitor synchronization health regularly
- Use filtering to reduce unnecessary synchronization
- Protect against accidental deletes
- Plan high availability carefully
- Document synchronization design decisions

---

# Summary

Microsoft provides two synchronization tools for hybrid identity:

## Microsoft Entra Connect Sync

Best for:

- Complex enterprises
- Advanced hybrid identity
- Exchange hybrid
- Device writeback
- Advanced customization

---

## Microsoft Entra Cloud Sync

Best for:

- Simpler deployments
- Lightweight infrastructure
- Lower maintenance
- Faster deployment
- Disconnected forests

Both tools help organisations create a seamless hybrid identity experience between on-premises Active Directory and Microsoft Entra ID.
