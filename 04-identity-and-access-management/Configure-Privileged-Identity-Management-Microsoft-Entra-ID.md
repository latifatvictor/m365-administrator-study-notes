# Configure Privileged Identity Management (PIM)

## Overview

Microsoft Entra Privileged Identity Management (PIM) provides organizations with a secure way to manage privileged access to Microsoft Entra ID, Azure, and Microsoft online services.

PIM helps organizations:
- Reduce standing administrator access
- Enforce least privilege access
- Control privileged role activation
- Monitor privileged activities
- Improve security and compliance

Only Privileged Role Administrators can manage Microsoft Entra directory role assignments in PIM.

---

# PIM Role Assignment Process

The PIM role assignment process includes:

1. Configure PIM role settings
2. Assign roles to users
3. Activate role assignments
4. Approve or deny requests
5. Extend and renew assignments

---

# Email Notifications in PIM

PIM sends email notifications when:
- Roles are assigned
- Roles are activated
- Approvals are required
- Assignments are expiring
- Requests are approved or denied

Notifications can include:
- Links to tasks
- Activation requests
- Renewal requests
- Approval requests

---

# Configure PIM Role Settings

Role settings define:
- MFA requirements
- Approval requirements
- Assignment duration
- Notification settings
- Activation controls

Only:
- Global Administrators
OR
- Privileged Role Administrators

can configure PIM role settings.

Role settings are configured per role.

---

# Task 1 - Discover and Mitigate Privileged Roles

Organizations should:
- Review privileged role assignments
- Identify unnecessary administrators
- Remove excessive access
- Conduct access reviews

Microsoft Entra access reviews help automate:
- Discovery
- Review
- Approval
- Removal

---

# Task 2 - Determine Roles to Protect

Organizations should prioritize:
- Global Administrator
- Security Administrator

These roles:
- Have broad permissions
- Present the highest security risk if compromised

Organizations should also protect:
- Other sensitive privileged roles

---

# Task 3 - Configure Role Settings

Organizations should:
- Configure settings for every privileged role
- Define security requirements
- Configure assignment durations
- Enable approval workflows

---

# PIM Role Settings

## Activation Maximum Duration

Defines:
- Maximum activation time before expiration

Range:
- 1 to 24 hours

If greater than 24 hours:
- PIM resets value to 24 hours

---

# Require MFA on Activation

Organizations can require:
- Multifactor authentication before role activation

Benefits:
- Prevents compromised account abuse
- Confirms user identity

Microsoft recommends:
- MFA for all administrators

---

# Require Justification on Activation

Users must:
- Provide business justification before activation

Purpose:
- Improves accountability
- Supports auditing

---

# Require Ticket Information

Users can be required to enter:
- Support ticket number

Important:
- Information-only field
- No ticket validation occurs

---

# Require Approval to Activate

Organizations can require:
- Approval before activation

Requirements:
- At least one approver
- Microsoft recommends at least two approvers

Approvers:
- Do NOT require admin roles

---

# Assignment Duration Settings

PIM supports:
- Eligible assignments
- Active assignments

Each can be:
- Permanent
OR
- Time-bound

---

# Eligible Assignment Duration Options

## Permanent Eligible

User:
- Always eligible for activation

---

# Expire Eligible Assignment After

User:
- Eligible only during specified dates

---

# Active Assignment Duration Options

## Permanent Active

User:
- Permanently active

Microsoft recommends:
- Avoid permanent active assignments

---

# Expire Active Assignment After

User:
- Active only during specified dates

---

# MFA on Active Assignment

Organizations can require:
- MFA when creating active assignments

Important:
- PIM cannot enforce MFA during usage because access is already active

---

# Justification on Active Assignment

Organizations can require:
- Business justification when creating active assignments

---

# Notification Settings

PIM provides granular email notification control.

Organizations can:
- Disable notifications
- Specify recipients
- Send critical alerts only
- Add additional recipients

Multiple recipients:
- Separate with semicolon (;)

---

# Critical Emails Only

Critical-only notifications include:
- Immediate action requests
- Approval requests

Noncritical notifications:
- Extension reminders
- Informational messages

---

# Assign Roles to Users

Global Administrators can:
- Assign permanent roles

Privileged Role Administrators can:
- Assign eligible roles
- Manage PIM assignments

PIM supports:
- Built-in roles
- Custom roles

---

# Assignment Components

Assignments include:
- Members
- Scope
- Assignment type
- Assignment duration

---

# Assignment Scope

Scope limits access to:
- Specific resources
- Administrative units
- Applications
- Resource groups

---

# Assignment Types

## Eligible Assignment

Requires activation before use.

Possible activation requirements:
- MFA
- Justification
- Approval

---

# Active Assignment

Provides immediate access.

No activation required.

---

# Assignment Duration Types

## Permanent

No expiration date.

Best for:
- Long-term employees needing frequent access

---

# Time-Bound

Assignment expires automatically.

Best for:
- Contractors
- Temporary staff
- Project-based work

---

# Activate Role Assignments

Eligible users must:
- Activate their role before use

Example:
- User eligible for Exchange Administrator role
- Activates role only when needed

Benefits:
- Reduces standing privileged access

---

# Approval Workflow

If approval is required:
- PIM sends email notifications to approvers

Approvers can:
- Approve requests
- Deny requests

After approval:
- User receives temporary access

---

# Approve or Deny Requests

Approvers can:
- Review requests
- Approve activation
- Reject activation
- View pending approvals

Once approved:
- User can use assigned privileges

---

# Extend and Renew Assignments

Time-bound assignments can:
- Expire automatically

Users can:
- Request extensions
- Request renewals

---

# Extend Assignment

Extension occurs:
- Before expiration

User requests:
- Additional assignment time

---

# Renew Assignment

Renewal occurs:
- After assignment expiration

User requests:
- New assignment period

---

# Approval for Extension or Renewal

Requires approval from:
- Global Administrator
OR
- Privileged Role Administrator

---

# Expiration Notifications

PIM sends notifications:
- 14 days before expiration
- 1 day before expiration
- At expiration

---

# Administrator Notifications

Administrators receive notifications when:
- Users request extensions
- Users request renewals

After resolution:
- Other administrators are notified
- User receives decision notification

---

# Assignment Changes During Approval

Administrators can change:
- Start date
- End date
- Assignment type

Example:
- Change Eligible to Active temporarily

---

# Administrative Extensions

Administrators can extend assignments:
- On behalf of users

Administrative extensions:
- Do not require approval

Notifications are still sent.

---

# Best Practices for PIM

Microsoft recommends:
- Require MFA
- Use approval workflows
- Minimize permanent active assignments
- Regularly review assignments
- Use least privilege access
- Protect Global Administrator roles

---

# Key Exam Points

## Who Can Configure PIM?

- Global Administrator
- Privileged Role Administrator

---

# What Does Eligible Mean?

User:
- Must activate role before use

---

# What Does Active Mean?

User:
- Already has privileges

---

# What Is Just-In-Time Access?

Temporary privileged access that:
- Expires automatically

---

# MFA Recommendation

Microsoft recommends:
- MFA for all administrators

---

# Approval Requirement

PIM can require:
- Approval before role activation

---

# Notification Timing

PIM sends expiration notifications:
- 14 days before expiration
- 1 day before expiration

---

# Important Security Concepts

| Concept | Meaning |
|---|---|
| Eligible | Requires activation |
| Active | Already active |
| JIT Access | Temporary admin access |
| Least Privilege | Minimum required access |
| MFA | Multifactor authentication |

---

# Final Summary

Microsoft Entra PIM helps organizations:
- Secure privileged access
- Reduce standing admin permissions
- Implement temporary access
- Enforce MFA and approvals
- Monitor privileged activities
- Improve compliance

Core PIM processes include:
- Configuring role settings
- Assigning roles
- Activating roles
- Approving requests
- Extending assignments

---

# Exam Tip

Remember the sequence:

1. Configure role settings
2. Assign users
3. Activate roles
4. Approve requests
5. Extend or renew access

---

# File Reference

Source notes uploaded by user: :contentReference[oaicite:0]{index=0}
