File Name: microsoft-365-identity-models-guide.md

# Microsoft 365 Identity Models Guide

# Overview

Microsoft 365 uses Microsoft Entra ID for identity management and authentication.

Microsoft Entra ID is a cloud-based identity and access management service included with Microsoft 365 subscriptions.

A properly designed identity infrastructure is essential for:

- Authentication
- Authorization
- User access management
- Zero Trust security
- Secure cloud access
- Hybrid access management

---

# Important Note

Azure Active Directory (Azure AD) is now called Microsoft Entra ID.

---

# Why Identity Infrastructure Matters

A strong identity infrastructure helps organisations:

- Protect Microsoft 365 services
- Restrict access to authorised users
- Support Zero Trust architecture
- Manage permissions securely
- Enable secure remote access
- Protect cloud and on-premises resources

---

# Identity Models in Microsoft 365

Microsoft 365 supports two primary identity models:

1. Cloud-only identity
2. Hybrid identity

---

# Identity Models Comparison

| Attribute | Cloud-only Identity | Hybrid Identity |
|---|---|---|
| User account location | Exists only in Microsoft Entra ID | Exists in AD DS and Microsoft Entra ID |
| Authentication method | Microsoft Entra ID authenticates users | Microsoft Entra ID or another identity provider authenticates users |
| Best for | Cloud-native organisations | Organisations with on-premises AD DS |
| Main benefit | Simplicity | Same credentials for cloud and on-premises resources |
| Infrastructure required | No on-premises servers required | Requires AD DS and synchronisation |
| Management tools | Microsoft 365 admin center and PowerShell | AD DS + Entra synchronisation tools |

---

# Cloud-only Identity

# What Is Cloud-only Identity?

Cloud-only identity means:

- User accounts exist only in Microsoft Entra ID
- No on-premises Active Directory is required
- Microsoft Entra ID handles all authentication

This model is commonly used by:

- Small businesses
- Cloud-first organisations
- Organisations without on-premises servers

---

# How Cloud-only Identity Works

Users authenticate directly against Microsoft Entra ID when accessing:

- Exchange Online
- SharePoint Online
- Microsoft Teams
- OneDrive
- Other Microsoft 365 services

---

# Cloud-only Identity Architecture

```text
Users
   ↓
Microsoft Entra ID
   ↓
Microsoft 365 Services
```

---

# Benefits of Cloud-only Identity

| Benefit | Description |
|---|---|
| Simplicity | Easy to deploy and manage |
| Lower cost | No on-premises infrastructure |
| Cloud-native | Ideal for modern organisations |
| Fast deployment | Quick user provisioning |
| Reduced maintenance | No domain controllers required |

---

# Cloud-only Identity Management Tools

Administrators manage users using:

- Microsoft 365 admin center
- Microsoft Entra admin center
- PowerShell
- Microsoft Graph

---

# User Types in Cloud-only Identity

| User Type | Description |
|---|---|
| Employee accounts | Permanent internal users |
| Vendor accounts | Temporary business users |
| Contractor accounts | External workforce |
| Partner accounts | Business collaboration users |
| Guest accounts | External B2B collaboration |

---

# Business-to-Business (B2B) Accounts

B2B accounts allow external users to collaborate securely.

Examples:

- Suppliers
- Consultants
- Partners
- Customers

---

# Microsoft Entra Groups

Microsoft Entra groups simplify administration.

---

# Uses of Groups

| Use Case | Purpose |
|---|---|
| Group-based licensing | Automatically assign licences |
| Dynamic groups | Add users automatically using attributes |
| SaaS provisioning | Grant application access |
| Conditional Access | Apply security policies |
| SharePoint permissions | Manage collaboration access |

---

# Example Dynamic Group Rule

```text
Department = "Finance"
```

Users are automatically added to the Finance group.

---

# Hybrid Identity

# What Is Hybrid Identity?

Hybrid identity combines:

- On-premises Active Directory Domain Services (AD DS)
- Microsoft Entra ID

User accounts originate in AD DS and synchronise to Microsoft Entra ID.

---

# How Hybrid Identity Works

1. User accounts are created in AD DS
2. Accounts synchronise to Microsoft Entra ID
3. Users access cloud and on-premises resources using the same credentials

---

# Hybrid Identity Architecture

```text
On-Premises AD DS
        ↓
Synchronization
        ↓
Microsoft Entra ID
        ↓
Microsoft 365 Services
```

---

# Benefits of Hybrid Identity

| Benefit | Description |
|---|---|
| Single identity | Same credentials everywhere |
| Seamless access | Easier user experience |
| Existing infrastructure | Uses current AD DS |
| Centralised management | Continue managing identities on-premises |
| Enterprise-ready | Supports large environments |

---

# Hybrid Identity Authentication

Authentication can occur through:

- Password Hash Synchronization (PHS)
- Pass-through Authentication (PTA)
- Federation with AD FS

---

# Synchronisation Options

Microsoft provides two synchronisation methods:

1. Microsoft Entra Connect Sync
2. Microsoft Entra Cloud Sync

---

# Microsoft Entra Connect Sync

# Overview

An on-premises synchronisation solution.

Runs on a local server and synchronises AD DS changes to Microsoft Entra ID.

---

# Features

| Feature | Description |
|---|---|
| Password hash sync | Synchronises password hashes |
| Device registration | Registers devices in Entra ID |
| AD FS integration | Supports federated authentication |
| Enterprise scalability | Supports complex environments |

---

# Advantages

- Supports large enterprises
- Highly configurable
- Supports advanced hybrid scenarios

---

# Disadvantages

- Requires server maintenance
- Organisation manages infrastructure
- More complex deployment

---

# Microsoft Entra Cloud Sync

# Overview

A lightweight cloud-managed synchronisation solution.

Designed for:

- Smaller organisations
- Simpler Active Directory environments

---

# Features

| Feature | Description |
|---|---|
| Cloud-managed | Microsoft manages the service |
| Lightweight | Minimal infrastructure |
| User synchronisation | Syncs users, groups, contacts |
| Simpler deployment | Faster setup |

---

# Advantages

- Easier maintenance
- Cloud-managed
- Faster deployment
- Reduced infrastructure

---

# Disadvantages

- Fewer advanced features
- Less flexible than Entra Connect Sync

---

# Entra Connect Sync vs Cloud Sync

| Feature | Entra Connect Sync | Cloud Sync |
|---|---|---|
| Hosted on-premises | Yes | No |
| Microsoft-managed | No | Yes |
| Enterprise scalability | High | Medium |
| AD FS support | Yes | No |
| Complexity | Higher | Lower |
| Best for | Large enterprises | Smaller organisations |

---

# Password Hash Synchronization (PHS)

# What Is PHS?

Password Hash Synchronization synchronises a hashed version of the user password to Microsoft Entra ID.

Important:

- Passwords are never stored in plain text
- Additional hashing occurs before synchronisation

---

# Benefits of PHS

- Simple deployment
- Cloud authentication
- Reduced infrastructure
- High availability

---

# Pass-through Authentication (PTA)

# What Is PTA?

Pass-through Authentication validates passwords directly against on-premises AD DS.

Passwords are not stored in Microsoft Entra ID.

---

# PTA Authentication Flow

```text
User Login
   ↓
Microsoft Entra ID
   ↓
PTA Agent
   ↓
On-Premises AD DS
```

---

# Federation with AD FS

# What Is Federation?

Federation redirects authentication to an external identity provider such as AD FS.

---

# AD FS Benefits

- Full authentication control
- Smart card support
- Advanced authentication scenarios

---

# AD FS Disadvantages

- Complex deployment
- Requires high availability
- More infrastructure management

---

# Zero Trust and Identity

Identity is a core component of Zero Trust.

Microsoft 365 uses identity to:

- Verify every access request
- Enforce Conditional Access
- Protect cloud workloads
- Validate device compliance

---

# Common Security Features

| Feature | Purpose |
|---|---|
| MFA | Multi-factor authentication |
| Conditional Access | Policy-based access control |
| Passwordless authentication | Reduce password risks |
| Identity Protection | Detect risky sign-ins |
| Privileged Identity Management | Protect admin roles |

---

# Authentication Flow in Microsoft 365

```text
User
   ↓
Microsoft Entra ID
   ↓
Authentication
   ↓
Conditional Access
   ↓
Microsoft 365 Resource Access
```

---

# Cloud-only Identity Best Practices

- Enable MFA
- Use Conditional Access
- Use dynamic groups
- Implement passwordless authentication
- Protect administrator accounts
- Use least privilege access

---

# Hybrid Identity Best Practices

- Keep AD DS healthy
- Secure synchronisation servers
- Monitor synchronisation health
- Use MFA
- Limit privileged accounts
- Protect domain controllers

---

# Common Use Cases

# Cloud-only Identity Example

A startup company:

- Uses only Microsoft 365
- Has no on-premises infrastructure
- Manages users directly in Entra ID

Best model:

Cloud-only identity

---

# Hybrid Identity Example

A large enterprise:

- Uses on-premises AD DS
- Has legacy applications
- Needs single sign-on

Best model:

Hybrid identity

---

# Common Challenges

| Challenge | Solution |
|---|---|
| Password synchronisation issues | Monitor Entra Connect health |
| Duplicate accounts | Clean AD DS before sync |
| Authentication failures | Review Conditional Access |
| Legacy authentication | Disable legacy protocols |
| Hybrid complexity | Simplify authentication model |

---

# Important Exam Points

- Microsoft 365 uses Microsoft Entra ID for identity management
- Two main identity models exist:
  - Cloud-only identity
  - Hybrid identity
- Cloud-only identity stores users only in Microsoft Entra ID
- Hybrid identity synchronises AD DS with Microsoft Entra ID
- Entra Connect Sync is on-premises
- Entra Cloud Sync is cloud-managed
- Hybrid identity enables single sign-on
- Microsoft Entra groups simplify management
- MFA and Conditional Access are critical security controls

---

# Interview Questions

## Q1: What are the two Microsoft 365 identity models?

- Cloud-only identity
- Hybrid identity

---

## Q2: What is Microsoft Entra ID?

A cloud-based identity and authentication service used by Microsoft 365.

---

## Q3: What is the main advantage of hybrid identity?

Users can use the same credentials for on-premises and cloud resources.

---

## Q4: What is the difference between Entra Connect Sync and Cloud Sync?

Entra Connect Sync is on-premises and enterprise-focused, while Cloud Sync is Microsoft-managed and lightweight.

---

## Q5: What is Password Hash Synchronization?

A method that synchronises password hashes from AD DS to Microsoft Entra ID.

---

## Q6: What is the best identity model for a cloud-only company?

Cloud-only identity.

---

## Q7: Why is identity important in Zero Trust?

Because every access request must be authenticated and authorised.

---

# Real World Example

A company currently uses:

- Active Directory
- Domain-joined devices
- On-premises applications

They migrate to Microsoft 365.

The company implements:

- Hybrid identity
- Entra Connect Sync
- Password Hash Synchronization
- Conditional Access
- MFA

Users can now:

- Use one password
- Access cloud and on-premises apps
- Work securely remotely

---

# Summary

Microsoft 365 identity management relies on Microsoft Entra ID.

The two identity models are:

1. Cloud-only identity
2. Hybrid identity

Cloud-only identity is:

- Simple
- Cloud-native
- Easy to manage

Hybrid identity is:

- Enterprise-focused
- Integrated with AD DS
- Designed for existing infrastructure

Hybrid identity uses:

- Microsoft Entra Connect Sync
- Microsoft Entra Cloud Sync
- Password Hash Synchronization
- Pass-through Authentication
- Federation

Strong identity management is foundational to:

- Zero Trust
- Secure access
- Microsoft 365 security
- Compliance
- User productivity
