# Explore Privileged Identity Management (PIM) in Microsoft Entra ID

## Overview

Privileged Identity Management (PIM) is a Microsoft Entra ID service that helps organizations:

- Manage privileged access
- Control administrator permissions
- Monitor privileged activities
- Reduce standing administrative access
- Improve security and compliance

PIM protects:
- Microsoft Entra ID resources
- Azure resources
- Microsoft 365 services
- Microsoft Intune
- Other Microsoft online services

---

# Why Organizations Use PIM

Organizations use PIM to:
- Reduce unnecessary privileged access
- Minimize attack surfaces
- Prevent misuse of admin permissions
- Improve compliance
- Implement least privilege access

Reducing privileged access lowers the risk of:
- Malicious attacks
- Accidental changes
- Insider threats
- Compromised administrator accounts

---

# Key Features of PIM

PIM provides several important security features.

| Feature | Purpose |
|---|---|
| Just-in-time access | Temporary privileged access |
| Time-bound assignments | Start and end dates for access |
| Approval workflows | Require approval before activation |
| MFA enforcement | Require multifactor authentication |
| Justification prompts | Require business reasons |
| Notifications | Alert administrators |
| Access reviews | Validate ongoing access needs |
| Audit history | Track privileged activity |

---

# Just-in-Time (JIT) Access

JIT access:
- Provides temporary administrator permissions
- Reduces permanent standing access
- Automatically removes privileges after expiration

This approach:
- Minimizes exposure
- Improves security posture
- Supports least privilege principles

---

# Principle of Least Privilege

The principle of least privilege means:
- Users receive only the minimum permissions required

Benefits:
- Reduced attack surface
- Lower risk of privilege abuse
- Better security governance

Microsoft recommends:
- Minimizing Global Administrators
- Using role-specific admin roles whenever possible

---

# Eligible vs Active Assignments

PIM introduces two important assignment types.

---

# Eligible Assignment

An eligible assignment:
- Does NOT provide permanent access
- Requires activation before use

Users must:
- Activate the role when needed

Possible activation requirements:
- MFA
- Approval
- Justification

---

# Active Assignment

An active assignment:
- Provides immediate access
- Does NOT require activation

Users assigned active roles:
- Already possess permissions

---

# Activation Process

Activation is the process where:
- Eligible users temporarily gain access

Possible activation requirements include:
- MFA verification
- Business justification
- Approval workflow

After activation:
- Access remains active temporarily
- Access expires automatically

---

# Permanent vs Time-Bound Assignments

PIM supports:
- Permanent assignments
- Time-bound assignments

---

# Permanent Eligible

User:
- Always eligible to activate the role

Requires:
- Activation before use

---

# Permanent Active

User:
- Always has access

No activation required.

Microsoft recommends:
- Very few permanent active assignments

---

# Time-Bound Eligible

User:
- Eligible only during a specified time period

Requires:
- Activation

---

# Time-Bound Active

User:
- Has active access only during specified dates

No activation required during valid period.

---

# Recommended Best Practice

Microsoft recommends:
- Zero permanently active assignments

Exception:
- Two emergency break-glass Global Administrator accounts

---

# PIM Workflow

The basic PIM workflow includes:

1. Organization selects privileged roles to protect
2. Users are assigned as eligible
3. User requests activation
4. PIM verifies requirements
5. User gains temporary access
6. Access expires automatically

---

# PIM Security Controls

PIM can enforce:
- MFA
- Approval workflows
- Justification requirements
- Time limits
- Notifications
- Audit logging

---

# PIM Audit and Compliance Features

PIM provides:
- Audit logs
- Activity tracking
- Access reviews
- Compliance reporting

Organizations can:
- Download audit history
- Review privileged usage
- Monitor role activations

---

# Access Reviews

Access reviews help organizations:
- Verify users still require access
- Remove unnecessary permissions
- Maintain least privilege

---

# Notifications

PIM sends notifications when:
- Roles are activated
- Requests are approved
- Suspicious activity occurs

---

# Roles Managed by PIM

PIM supports multiple resource types.

---

# Microsoft Entra Roles

Includes:
- Built-in directory roles
- Custom roles

Examples:
- Global Administrator
- Security Administrator
- Privileged Role Administrator

---

# Azure Roles

Azure RBAC roles including:
- Management groups
- Subscriptions
- Resource groups
- Individual resources

---

# PIM for Groups

PIM for Groups enables:
- Just-in-time group ownership
- Temporary group membership

Used for:
- Security groups
- Intune permissions
- Key Vault access

---

# Supported Assignments

PIM can assign:
- Users
- Groups

---

# Important Warning

Microsoft does NOT recommend:
- Nested groups in PIM for Groups

---

# Licensing Requirements

PIM requires:
- Microsoft Entra Premium P2
OR
- EMS E5

---

# Important PIM Roles

## Privileged Role Administrator

Can:
- Configure approvals
- Assign eligible users
- View activation history

---

# Approver

Can:
- Approve activation requests
- Reject activation requests
- Provide approval justification

---

# Eligible User

Can:
- Request role activation
- Activate privileged roles
- Complete privileged tasks temporarily

---

# Important Terminology

| Term | Meaning |
|---|---|
| Eligible | User must activate role |
| Active | User already has access |
| Activate | Temporary elevation process |
| Assigned | User currently has active assignment |
| Activated | Eligible user successfully activated |
| JIT Access | Temporary privileged access |
| Least Privilege | Minimum permissions required |

---

# Assignment Types Summary

| Assignment Type | Description |
|---|---|
| Permanent Eligible | Always eligible |
| Permanent Active | Always active |
| Time-Bound Eligible | Eligible during specified dates |
| Time-Bound Active | Active during specified dates |

---

# Security Benefits of PIM

PIM helps organizations:
- Reduce standing admin access
- Improve auditability
- Prevent privilege abuse
- Strengthen compliance
- Limit attack exposure

---

# Key Exam Points

## PIM Purpose

PIM is used to:
- Manage privileged access
- Reduce permanent admin privileges
- Implement JIT access

---

# Eligible Assignment

Eligible users:
- Must activate roles before use

---

# Active Assignment

Active users:
- Already have permissions

---

# JIT Access

JIT access:
- Provides temporary admin access
- Expires automatically

---

# MFA Enforcement

PIM can require:
- Multifactor authentication before activation

---

# Licensing

PIM requires:
- Microsoft Entra Premium P2

---

# Best Practice

Microsoft recommends:
- Minimal permanent Global Administrators
- Prefer eligible assignments over active assignments

---

# Final Summary

Privileged Identity Management (PIM) helps organizations:
- Secure privileged accounts
- Reduce attack surfaces
- Implement least privilege access
- Enforce temporary administrator access
- Improve security monitoring and compliance

Core concepts include:
- Eligible assignments
- Active assignments
- Just-in-time access
- MFA enforcement
- Approval workflows

---

# Exam Tip

Remember:

| Concept | Meaning |
|---|---|
| Eligible | Requires activation |
| Active | Already active |
| JIT | Temporary privileged access |
| Least Privilege | Minimum permissions required |
| PIM | Privileged access management |

---

# File Reference

Source notes uploaded by user: :contentReference[oaicite:0]{index=0}
