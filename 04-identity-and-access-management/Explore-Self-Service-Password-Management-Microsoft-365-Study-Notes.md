# Explore Self-Service Password Management (SSPR)

## Overview

Self-Service Password Reset (SSPR) enables users to:
- Reset their own passwords
- Unlock accounts without administrator assistance
- Reduce helpdesk dependency

SSPR improves:
- User productivity
- Security
- Operational efficiency

---

# Important Notes

- SSPR is NOT enabled by default
- Microsoft 365 Administrators must enable it
- Can be enabled:
  - For all users
  - For selected groups

---

# Purpose of SSPR

SSPR helps organizations:
- Reduce password reset tickets
- Improve user experience
- Enable faster account recovery
- Support remote and hybrid workers

---

# Verification Methods

Before resetting a password, users must verify their identity.

Supported verification methods include:

- Alternate email address
- Office phone call
- Mobile phone call
- Text message (SMS)
- Security questions

---

# Password Reset Process

Users reset passwords by:
1. Going to the Microsoft 365 sign-in page
2. Selecting:
   - “Can’t access your account?”
3. Completing identity verification
4. Creating a new password

---

# User Profile Requirement

Users must:
- Configure alternate authentication information beforehand

Examples:
- Personal email
- Mobile number
- Security questions

If not configured:
- Administrator assistance is required

---

# Important Restriction

Microsoft Support:
- Cannot reset forgotten passwords for users

Only:
- The user
- Or the organization administrator
can perform password resets.

---

# Administrator Requirements

Administrators using SSPR:
- Must use TWO verification methods
- Cannot use security questions

---

# SSPR and Cloud Identities

## Supported Scenario

SSPR works directly for:
- Cloud-only identities

These users:
- Exist only in Microsoft Entra ID
- Are not synchronized with on-premises AD

---

# Cloud Identity Password Reset

When cloud-only users reset passwords:
- Password changes occur only in Microsoft Entra ID
- No on-premises synchronization is required

---

# Hybrid Identity Scenario

## Hybrid Users

Hybrid users:
- Exist in on-premises AD DS
- Synchronize to Microsoft Entra ID

---

# Password Reset Complexity

For hybrid users:
- Password reset in cloud does NOT automatically update on-premises AD

Why?
- Microsoft Entra ID cannot write passwords back without extra configuration

---

# Password Writeback Requirement

To enable SSPR for hybrid users:
- Password writeback must be configured

This requires:
- Microsoft Entra Connect Sync
- Password writeback enabled

---

# Licensing Requirement

Hybrid SSPR requires:
- Microsoft Entra ID Premium license

Examples:
- Entra ID P1
- Entra ID P2

---

# Password Writeback Process

## Workflow

1. User resets password in cloud
2. Microsoft Entra Connect Sync detects change
3. New password writes back to on-premises AD DS
4. Identity remains synchronized

---

# Benefits of Password Writeback

Benefits include:
- Consistent credentials
- Better user experience
- Reduced administrative effort
- Hybrid identity support

---

# Microsoft Entra Basic Limitation

Microsoft Entra Basic:
- Cannot write passwords back to on-premises AD DS

Only Microsoft Entra Premium supports:
- Password writeback

---

# Microsoft Entra Premium Features

Microsoft Entra Premium enables:
- Password writeback
- SSPR for hybrid users
- Enhanced identity management

---

# SSPR Supported Identity Types

## Cloud-Only Identities

Supported:
- Fully supported with no extra configuration

---

# Hybrid Identities

Supported only when:
- Entra Connect Sync configured
- Password writeback enabled
- Premium licensing available

---

# Security Benefits of SSPR

SSPR improves security by:
- Reducing helpdesk social engineering risks
- Supporting MFA verification
- Enabling secure identity recovery

---

# Operational Benefits

Organizations benefit from:
- Fewer support calls
- Reduced password reset workload
- Faster issue resolution
- Better end-user productivity

---

# Password Reset Verification Best Practices

Microsoft recommends:
- Multiple verification methods
- MFA-enabled environments
- Strong authentication policies

---

# Common SSPR Components

Key components include:
- Microsoft Entra ID
- Microsoft Entra Connect Sync
- Password writeback
- Verification methods
- Hybrid identity synchronization

---

# Hybrid Identity Password Flow

## Without Password Writeback

- Password changes only in cloud
- On-premises password remains unchanged
- Credential inconsistency occurs

---

# Hybrid Identity Password Flow

## With Password Writeback

- Password changes synchronize back to on-premises AD
- Credentials remain consistent
- Better hybrid experience

---

# Knowledge Check

## Question

When passwords are changed in Microsoft 365, they can be written back to the on-premises Active Directory. Which requirement must be met?

## Correct Answer

- You need a Microsoft Entra Premium license

---

# Key Takeaways

SSPR:
- Allows users to reset passwords independently
- Improves productivity and security
- Requires administrator configuration

Cloud-only users:
- Fully supported immediately

Hybrid users:
- Require:
  - Microsoft Entra Connect Sync
  - Password writeback
  - Microsoft Entra Premium licensing

Password writeback:
- Synchronizes cloud password changes back to on-premises AD DS
- Maintains identity consistency across environments
