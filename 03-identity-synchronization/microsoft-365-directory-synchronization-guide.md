
# Microsoft 365 Directory Synchronization Guide

# Overview

Directory synchronization is the process of synchronising identities and directory objects between two different directories.

These objects include:

- Users
- Groups
- Contacts
- Computers

In Microsoft 365 environments, directory synchronization usually occurs between:

- On-premises Active Directory Domain Services (AD DS)
- Microsoft Entra ID

---

# Important Note

Azure Active Directory (Azure AD) is now called Microsoft Entra ID.

---

# What Directory Synchronization Does

Directory synchronization helps organisations:

- Keep identities consistent
- Simplify authentication
- Enable hybrid identity
- Improve user experience
- Reduce password fatigue
- Support cloud access

---

# Common Synchronisation Scenario

```text
On-Premises AD DS
        ↓
Directory Synchronization
        ↓
Microsoft Entra ID
        ↓
Microsoft 365 Services
```

---

# Objects That Can Synchronise

| Object Type | Description |
|---|---|
| Users | Employee and service accounts |
| Groups | Security and Microsoft 365 groups |
| Contacts | Mail contacts |
| Computers | Device objects |
| Passwords | Password hashes |
| Attributes | User information such as department and title |

---

# Synchronisation Sources

Although AD DS is the most common source, synchronisation can also include:

- HR databases
- LDAP directories
- Other identity systems

---

# One-Way vs Two-Way Synchronisation

# One-Way Synchronisation

Most Microsoft 365 hybrid environments use:

```text
On-Premises AD DS → Microsoft Entra ID
```

Changes made on-premises synchronise to the cloud.

---

# Two-Way Synchronisation

Microsoft Entra Connect Sync and Microsoft Entra Cloud Sync support limited writeback capabilities.

This allows certain data to synchronise back to on-premises AD DS.

---

# Examples of Writeback Features

| Writeback Feature | Purpose |
|---|---|
| Password writeback | Reset passwords in the cloud and update on-premises |
| Group writeback | Synchronise Microsoft 365 groups to AD DS |
| Device writeback | Write device objects back on-premises |

---

# Synchronisation Tools

Microsoft recommends two main synchronisation tools:

1. Microsoft Entra Connect Sync
2. Microsoft Entra Cloud Sync

---

# Microsoft Entra Connect Sync

## Overview

An on-premises synchronisation solution installed on a dedicated server.

Synchronises:

- Users
- Groups
- Contacts
- Password hashes
- Attributes

---

# Features

| Feature | Description |
|---|---|
| Password hash sync | Synchronises password hashes |
| Password writeback | Enables cloud password resets |
| Device registration | Hybrid device support |
| Federation integration | Supports AD FS |
| Advanced hybrid features | Enterprise-grade functionality |

---

# Best Practice

Microsoft recommends installing Entra Connect Sync on a dedicated server.

---

# Microsoft Entra Cloud Sync

## Overview

A lightweight cloud-managed synchronisation solution hosted by Microsoft.

Designed for:

- Simpler environments
- Smaller organisations
- Reduced infrastructure management

---

# Benefits of Directory Synchronization

# Hybrid Identity

Directory synchronization enables hybrid identity.

Users can use the same identity for:

- On-premises resources
- Microsoft 365
- Cloud applications

---

# Single Sign-On (SSO)

Users sign in once and access:

- Cloud apps
- On-premises applications
- SaaS services

This improves:

- Productivity
- User experience
- Security

---

# Multifactor Authentication (MFA)

Directory synchronization supports MFA integration.

MFA requires:

- Something you know
- Something you have
- Something you are

---

# MFA Examples

| Authentication Factor | Example |
|---|---|
| Something you know | Password |
| Something you have | Mobile device |
| Something you are | Fingerprint |

---

# Conditional Access

Microsoft Entra ID supports Conditional Access policies.

Administrators can control access based on:

- User identity
- Device compliance
- Location
- Application
- Risk level
- MFA status

---

# Example Conditional Access Scenario

```text
If user signs in from outside UK
AND device is unmanaged
THEN require MFA
```

---

# Common Identity

A common identity can be used across:

- Microsoft 365
- Intune
- SaaS applications
- Non-Microsoft applications
- Cloud services

---

# Application Integration

Developers can integrate applications using:

- Microsoft Entra ID
- Entra App Proxy
- Cloud authentication models

---

# Password Hash Synchronization Recommendation

Microsoft strongly recommends enabling Password Hash Synchronization (PHS) regardless of the primary authentication method.

This applies even if using:

- Pass-through Authentication (PTA)
- Federated authentication

---

# Why Microsoft Recommends PHS

# High Availability and Disaster Recovery

PHS improves resilience.

PTA and federation rely on:

- On-premises servers
- Networking
- Authentication agents
- Federation infrastructure
- Domain controllers

If these fail, authentication may fail.

PHS provides cloud-based fallback authentication.

---

# Example Outage Scenario

## Organisation Using PHS

- On-premises systems fail
- Users still authenticate to Microsoft 365
- Email and cloud apps remain accessible

Recovery time:

Hours

---

## Organisation Without PHS

- On-premises systems fail
- Authentication completely fails
- Users lose Microsoft 365 access

Recovery time:

Days or weeks

---

# Cyberattack and Ransomware Protection

PHS helps organisations survive:

- Ransomware attacks
- Domain controller outages
- Infrastructure failures

This is critical during disaster recovery.

---

# Identity Protection

Microsoft Entra Identity Protection requires Password Hash Synchronization.

---

# What Identity Protection Does

Microsoft scans for:

- Leaked credentials
- Password dumps
- Compromised usernames
- Dark web password exposure

---

# Identity Protection Actions

Administrators can:

- Block sign-ins
- Force password resets
- Require MFA
- Detect risky sign-ins

---

# Important Security Point

Even when using PTA or federation, Microsoft recommends enabling PHS for Identity Protection capabilities.

---

# Authentication Infrastructure Dependencies

# PTA Dependencies

PTA relies on:

- PTA agents
- On-premises networking
- Domain controllers

---

# Federation Dependencies

Federation relies on:

- AD FS servers
- Web Application Proxy
- Federation infrastructure
- Load balancing
- Domain controllers

---

# Why PHS Is More Resilient

PHS authenticates directly in Microsoft Entra ID.

This reduces dependence on:

- On-premises infrastructure
- Federation services
- Authentication agents

---

# Directory Synchronization Best Practices

- Use Password Hash Synchronization
- Use redundant synchronisation servers
- Monitor synchronisation health
- Protect synchronisation servers
- Enable MFA
- Use Conditional Access
- Keep AD DS healthy
- Use least privilege access
- Backup synchronisation configurations

---

# Common Synchronisation Challenges

| Issue | Possible Cause |
|---|---|
| Duplicate users | Improper matching |
| Password sync failure | Connectivity or permissions |
| Missing users | OU filtering |
| Attribute conflicts | Duplicate attributes |
| Delayed synchronisation | Synchronisation schedule |

---

# Synchronisation Troubleshooting Areas

- Synchronisation service status
- AD DS connectivity
- Entra Connect health
- Password writeback
- OU filtering
- Attribute matching
- Licensing
- Usage location assignment

---

# Real World Example

A company uses:

- On-premises Active Directory
- Microsoft 365
- Microsoft Teams
- Exchange Online

They deploy:

- Microsoft Entra Connect Sync
- Password Hash Synchronization
- Conditional Access
- MFA

Result:

- Users sign in once
- Same password works everywhere
- Cloud services stay available during outages
- Identity Protection detects compromised credentials

---

# Common Interview Questions

## Q1: What is directory synchronization?

The process of synchronising identities and directory objects between directories such as AD DS and Microsoft Entra ID.

---

## Q2: What objects can synchronise?

- Users
- Groups
- Contacts
- Computers
- Password hashes
- Attributes

---

## Q3: What are the main synchronisation tools?

- Microsoft Entra Connect Sync
- Microsoft Entra Cloud Sync

---

## Q4: What is hybrid identity?

A common identity across on-premises and cloud services.

---

## Q5: Why does Microsoft recommend Password Hash Synchronization?

For resilience, disaster recovery, Identity Protection, and high availability.

---

## Q6: What is password writeback?

A feature that allows password resets in the cloud to synchronise back to on-premises AD DS.

---

## Q7: What is Conditional Access?

Policies that control access based on identity, device, location, and risk.

---

## Q8: Why is MFA important?

It provides additional authentication security beyond passwords.

---

# Key Exam Points

- Directory synchronization connects on-premises AD DS with Microsoft Entra ID
- Most synchronisation is one-way from on-premises to cloud
- Microsoft Entra Connect Sync supports writeback features
- Hybrid identity enables single sign-on
- MFA improves authentication security
- Conditional Access controls access dynamically
- Microsoft strongly recommends Password Hash Synchronization
- Identity Protection depends on PHS
- PHS improves disaster recovery and outage resilience
- Synchronised users require licences and usage locations

---

# Summary

Directory synchronization is a core part of Microsoft 365 hybrid identity.

It synchronises:

- Users
- Groups
- Contacts
- Passwords
- Directory attributes

between:

- On-premises AD DS
- Microsoft Entra ID

The main synchronisation solutions are:

- Microsoft Entra Connect Sync
- Microsoft Entra Cloud Sync

Directory synchronization enables:

- Hybrid identity
- Single sign-on
- MFA
- Conditional Access
- Common identity management

Microsoft strongly recommends enabling Password Hash Synchronization to improve:

- High availability
- Disaster recovery
- Identity Protection
- Cyberattack resilience
