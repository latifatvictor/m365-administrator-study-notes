# Microsoft Entra ID Deployment Planning Guide

# Overview

Microsoft Entra ID is the cloud-based identity and access management solution used by Microsoft 365.

A properly planned Microsoft Entra ID deployment helps organisations:

- Secure identities
- Protect data
- Enable hybrid identity
- Support Zero Trust security
- Manage applications
- Enable secure authentication
- Simplify user management

---

# Important Note

Azure Active Directory (Azure AD) is now called Microsoft Entra ID.

---

# Why Microsoft Entra ID Planning Is Important

A well-designed identity infrastructure ensures:

- Only authorised users access resources
- Devices are trusted and compliant
- Applications are protected
- Security risks are reduced
- Users have a seamless sign-in experience

---

# Zero Trust Principle

Microsoft Entra ID supports a Zero Trust security model.

Zero Trust means:

```text
Never trust
Always verify
```

Every access attempt is:

- Authenticated
- Authorised
- Evaluated continuously

---

# Microsoft Entra ID Deployment Phases

Microsoft recommends deploying Microsoft Entra ID in four major phases:

| Phase | Focus |
|---|---|
| Phase 1 | Build a security foundation |
| Phase 2 | Import users and manage devices |
| Phase 3 | Manage applications |
| Phase 4 | Audit privileged access and automate lifecycle |

---

# Phase 1: Build a Foundation of Security

# Goal

Create a secure Microsoft Entra ID environment before onboarding users.

---

# Why This Matters

This phase ensures:

- Security is implemented from the start
- Administrators follow least privilege
- Users only learn new security processes once
- Risks are reduced early

---

# Phase 1 Tasks

---

# Create Multiple Global Administrators

## Recommendation

Create:

- 2 to 4 cloud-only emergency global admin accounts

---

# Best Practices

- Use long complex passwords
- Do not use daily
- Store credentials securely
- Use break-glass emergency accounts

---

# Required License

Microsoft Entra Free

---

# Use Least Privilege Administration

## Recommendation

Avoid assigning Global Administrator unnecessarily.

Use smaller scoped admin roles such as:

- User Administrator
- Helpdesk Administrator
- Exchange Administrator
- Teams Administrator

---

# Benefit

Reduces attack surface and administrative risk.

---

# Required License

Microsoft Entra Free

---

# Enable Privileged Identity Management (PIM)

## Purpose

Track and manage privileged role usage.

---

# Features

- Just-in-time role activation
- MFA enforcement
- Approval workflows
- Audit logging
- Time-limited access

---

# Example

Instead of permanent Global Admin rights:

```text
User requests admin access
↓
MFA challenge
↓
Approval
↓
Temporary access granted
```

---

# Required License

Microsoft Entra Premium P2

---

# Enable Self-Service Password Reset (SSPR)

## Purpose

Allow users to reset passwords themselves.

---

# Benefits

- Reduces helpdesk calls
- Improves productivity
- Faster recovery

---

# Required License

Microsoft Entra Premium P1

---

# Create a Custom Banned Password List

## Purpose

Prevent weak passwords related to your organisation.

---

# Example Banned Words

- CompanyName123
- London2025
- Welcome1

---

# Required License

Microsoft Entra Premium P1

---

# Enable On-Premises Password Protection

## Purpose

Extend banned password policies to on-premises Active Directory.

---

# Benefit

Consistent password protection across hybrid environments.

---

# Required License

Microsoft Entra Premium P1

---

# Use Microsoft Password Guidance

## Microsoft Recommendations

- Stop mandatory password expiration
- Avoid unnecessary complexity requirements
- Encourage strong memorable passwords

---

# Why

Frequent forced changes often cause:

- Weak password variations
- Password reuse
- Unsafe storage practices

---

# Required License

Microsoft Entra Free

---

# Disable Periodic Password Resets

## Purpose

Avoid forcing users to regularly change passwords.

---

# Benefit

Improves security and usability.

---

# Required License

Microsoft Entra Free

---

# Configure Smart Lockout

## Purpose

Protect accounts from brute force attacks.

---

# Features

- Detect repeated failures
- Temporarily lock accounts
- Prevent password spraying attacks

---

# Required License

Microsoft Entra Premium P1

---

# Enable Extranet Smart Lockout for AD FS

## Purpose

Protect federated environments from external password attacks.

---

# Benefit

Valid users continue working while attacks are blocked.

---

# Block Legacy Authentication

## Legacy Protocols to Block

- POP
- IMAP
- SMTP
- MAPI

---

# Why Block Them

These protocols:

- Cannot enforce MFA
- Are common attack targets

---

# Use Conditional Access

Example policy:

```text
If authentication method is legacy
THEN block access
```

---

# Required License

Microsoft Entra Premium P1

---

# Deploy Multifactor Authentication (MFA)

## Purpose

Require two-step verification.

---

# MFA Factors

| Type | Example |
|---|---|
| Something you know | Password |
| Something you have | Phone |
| Something you are | Fingerprint |

---

# Benefits

- Reduces credential attacks
- Protects cloud identities
- Improves compliance

---

# Required License

Microsoft Entra Premium P1

---

# Enable Microsoft Entra Identity Protection

## Purpose

Detect:

- Risky sign-ins
- Leaked credentials
- Impossible travel
- Anonymous IP usage

---

# Required License

Microsoft Entra Premium P2

---

# Use Risk-Based Policies

## Automated Responses

- Trigger MFA
- Force password reset
- Block sign-in

---

# Example

```text
High-risk sign-in detected
↓
Force password reset
```

---

# Required License

Microsoft Entra Premium P2

---

# Enable Combined Registration

## Purpose

Allow users to register:

- MFA methods
- SSPR methods

from one portal.

---

# Benefit

Simplifies onboarding.

---

# Required License

Microsoft Entra Premium P1

---

# Phase 2: Import Users, Enable Synchronization, and Manage Devices

# Goal

Synchronise identities and prepare device management.

---

# Install Microsoft Entra Connect Sync

## Purpose

Synchronise:

- Users
- Groups
- Contacts
- Password hashes

between:

- On-premises AD DS
- Microsoft Entra ID

---

# Required License

Microsoft Entra Free

---

# Implement Password Hash Synchronization (PHS)

## Benefits

- Synchronises password hashes
- Supports Identity Protection
- Enables leaked credential detection
- Improves resilience

---

# Required License

Microsoft Entra Free

---

# Implement Password Writeback

## Purpose

Allow cloud password changes to update on-premises AD DS.

---

# Benefit

Supports hybrid self-service password reset.

---

# Required License

Microsoft Entra Premium P1

---

# Enable Microsoft Entra Connect Health

## Purpose

Monitor:

- Sync servers
- AD FS servers
- Domain controllers

---

# Benefits

- Health alerts
- Performance monitoring
- Sync troubleshooting

---

# Required License

Microsoft Entra Premium P1

---

# Assign Licenses Using Groups

## Purpose

Automatically assign Microsoft 365 licenses.

---

# Example

```text
Sales Group
↓
Automatically receives E3 license
```

---

# Benefits

- Faster onboarding
- Simplified management
- Reduced errors

---

# Required License

Microsoft Entra Premium P1

---

# Plan Guest Access

## Purpose

Allow external collaboration.

---

# Guest Users Can Use

- Work accounts
- School accounts
- Social identities

---

# Benefits

- Secure collaboration
- External access management
- B2B integration

---

# Device Management Strategy

## Decide Between

| Option | Description |
|---|---|
| Registered | Personal devices |
| Joined | Corporate devices |
| Hybrid joined | On-premises + cloud |
| BYOD | Bring your own device |
| Company owned | Corporate managed |

---

# Deploy Windows Hello for Business

## Purpose

Enable passwordless authentication.

---

# Authentication Methods

- PIN
- Face recognition
- Fingerprint

---

# Benefits

- Improved security
- Better user experience
- Reduced password reliance

---

# Deploy Passwordless Authentication

## Examples

- Microsoft Authenticator
- FIDO2 keys
- Windows Hello

---

# Required License

Microsoft Entra Premium P1

---

# Phase 3: Manage Applications

# Goal

Integrate applications with Microsoft Entra ID.

---

# Identify Applications

## Application Types

- SaaS applications
- On-premises applications
- Line-of-business applications

---

# Questions to Ask

- Can it use SSO?
- Does it support MFA?
- Can it integrate with Entra ID?

---

# Required License

No license required

---

# Integrate SaaS Applications

## Microsoft Entra Gallery

Contains thousands of pre-integrated applications.

---

# Examples

- Salesforce
- ServiceNow
- Workday
- Zoom

---

# Benefits

- SSO
- MFA
- Centralised access management

---

# Required License

Microsoft Entra Free

---

# Use Application Proxy

## Purpose

Provide secure access to on-premises applications.

---

# Benefits

- Remote access
- SSO integration
- No VPN dependency

---

# Required License

Microsoft Entra Premium P1

---

# Phase 4: Audit Privileged Access and Manage User Lifecycle

# Goal

Enforce least privilege and automate identity management.

---

# Enforce Privileged Identity Management (PIM)

## Purpose

Remove permanent admin access.

---

# Benefits

- Just-in-time access
- Reduced risk
- Approval workflows
- Auditing

---

# Required License

Microsoft Entra Premium P2

---

# Complete Access Reviews

## Purpose

Review privileged access regularly.

---

# Benefits

- Remove unnecessary access
- Meet compliance requirements
- Improve governance

---

# Required License

Microsoft Entra Premium P2

---

# Implement Dynamic Groups

## Purpose

Automatically place users into groups.

---

# Example

```text
If Department = HR
↓
Automatically join HR group
```

---

# Common Attributes

- Department
- Region
- Job title
- Country
- Office location

---

# Required License

Microsoft Entra Premium P1

---

# Enable Group-Based Provisioning

## Purpose

Automatically provision SaaS app access.

---

# Benefits

- Faster onboarding
- Consistent permissions
- Reduced admin effort

---

# Required License

Microsoft Entra Premium P1

---

# Automate Provisioning and Deprovisioning

## Purpose

Automate user lifecycle management.

---

# Benefits

- Faster onboarding
- Immediate access removal
- Reduced security risks

---

# Example Workflow

```text
HR creates employee
↓
Account automatically created
↓
Groups assigned
↓
Licenses assigned
↓
Apps provisioned
```

---

# Key Microsoft Entra Security Features

| Feature | Purpose |
|---|---|
| MFA | Strong authentication |
| Conditional Access | Policy-based access |
| PIM | Privileged access control |
| Identity Protection | Detect risky activity |
| SSPR | User password reset |
| Passwordless auth | Remove password reliance |
| Dynamic groups | Automated group management |

---

# Real World Example

A company migrating to Microsoft 365 implements:

- Microsoft Entra Connect Sync
- Password Hash Synchronization
- MFA
- Conditional Access
- PIM
- Dynamic licensing
- Windows Hello for Business

Result:

- Hybrid identity enabled
- Secure cloud access
- Reduced helpdesk workload
- Improved compliance
- Centralised identity management

---

# Common Interview Questions

## Q1: What is Microsoft Entra ID?

Microsoft’s cloud identity and access management platform.

---

## Q2: Why is MFA important?

It protects accounts using multiple authentication factors.

---

## Q3: What is PIM?

Privileged Identity Management provides just-in-time admin access.

---

## Q4: What is Conditional Access?

Policies that control access based on conditions like device, user, or location.

---

## Q5: What is Password Hash Synchronization?

A method that synchronises password hashes from AD DS to Microsoft Entra ID.

---

## Q6: Why block legacy authentication?

Legacy protocols cannot enforce MFA and are commonly targeted by attackers.

---

## Q7: What are dynamic groups?

Groups that automatically update membership based on user attributes.

---

## Q8: What is Application Proxy?

A service that securely publishes on-premises applications externally.

---

# Key Exam Points

- Microsoft Entra ID supports Zero Trust security
- MFA is critical for protecting identities
- PIM enforces least privilege
- Conditional Access controls secure access
- Password Hash Synchronization improves resilience
- Dynamic groups automate administration
- Application Proxy provides secure remote access
- Identity Protection detects risky sign-ins
- Windows Hello supports passwordless authentication
- Group-based licensing simplifies management

---

# Summary

Microsoft Entra ID deployment should follow a phased approach:

1. Build a security foundation
2. Import users and manage devices
3. Integrate applications
4. Audit privileged access and automate lifecycle management

Key technologies include:

- MFA
- Conditional Access
- PIM
- Password Hash Synchronization
- Dynamic groups
- Identity Protection
- Passwordless authentication

A properly planned deployment improves:

- Security
- User experience
- Compliance
- Productivity
- Operational efficiency
