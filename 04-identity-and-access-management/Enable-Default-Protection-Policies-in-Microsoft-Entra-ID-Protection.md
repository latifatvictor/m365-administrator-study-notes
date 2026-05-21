# Enable the Default Protection Policies in Microsoft Entra ID Protection

## Overview

Microsoft Entra ID Protection is a cloud-based security service that helps organizations:
- Protect identities
- Detect risky sign-ins
- Detect compromised accounts
- Respond to threats automatically
- Improve security posture using machine learning and AI

Identity Protection uses:
- Artificial intelligence
- Machine learning
- Risk analysis
- Behavioral monitoring

to identify suspicious user and sign-in behavior.

---

# Benefits of Microsoft Entra ID Protection

By enabling Identity Protection, organizations can:

- View flagged users and detected risk events
- Automatically protect users using risk-based Conditional Access
- Improve security posture proactively
- Reduce account compromise risks
- Detect threats before attackers cause damage

---

# Adaptive Access Controls

Microsoft Entra ID Protection allows administrators to:
- Define risk-based policies
- Apply adaptive security controls
- Automatically remediate threats

These controls help prevent:
- Credential theft
- Phishing attacks
- Malware-based account compromise
- Account takeover attacks

---

# Default Identity Protection Policies

Microsoft Entra ID Protection provides three default policies:

1. User Risk Policy
2. Sign-In Risk Policy
3. MFA Registration Policy

All three policies are:
- Disabled by default
- Configurable by administrators

---

# 1. User Risk Policy

## What is User Risk?

User risk is:
- The probability that a user's identity has been compromised

Microsoft Entra ID Protection calculates user risk using:
- Password strength
- User behavior patterns
- Device health
- Sign-in locations
- Risk detections

The system learns:
- Normal user behavior
- Anomalous behavior

using machine learning.

---

# Purpose of the User Risk Policy

The User Risk Policy protects:
- Accounts detected as compromised
- High-risk users

It helps prevent attackers from:
- Using stolen credentials
- Accessing sensitive resources
- Moving laterally across the environment

---

# How the User Risk Policy Works

When a user is identified as risky, the policy can require:
- Password reset
- Multifactor authentication (MFA)

before access is granted.

This process:
- Verifies identity
- Blocks unauthorized access

---

# User Risk Policy Configuration

Administrators can:
- Apply policy to all users
- Apply policy to selected groups
- Include applications
- Exclude applications

Example:
- Exclude low-risk applications
- Protect high-value applications

---

# Why Organizations Should Enable User Risk Policy

Benefits include:
- Reduced account compromise
- Reduced identity theft
- Reduced account takeover risk
- Better protection of sensitive resources

---

# 2. Sign-In Risk Policy

## What is Sign-In Risk?

Sign-in risk is:
- The probability that a sign-in attempt is malicious or suspicious

Microsoft Entra ID Protection analyzes:
- Sign-in location
- Device used
- Network used
- Time of sign-in
- User behavior signals

---

# Purpose of Sign-In Risk Policy

The Sign-In Risk Policy protects applications and services from:
- Malicious sign-ins
- Stolen credentials
- Spoofed locations
- Compromised devices

---

# How Sign-In Risk Policy Works

Based on detected risk, the policy can:
- Require MFA
- Block sign-in attempts

This helps:
- Verify user identity
- Prevent unauthorized access

---

# Sign-In Risk Policy Configuration

Administrators can:
- Apply policy to all users
- Apply policy to selected groups
- Include high-risk applications
- Exclude low-risk services

---

# Why Organizations Should Enable Sign-In Risk Policy

Benefits include:
- Reduced unauthorized access
- Reduced credential abuse
- Reduced phishing impact
- Improved protection of applications and services

---

# 3. Multifactor Authentication (MFA) Registration Policy

## What is MFA Registration?

MFA registration is:
- The process where users configure a second authentication factor

Examples of MFA factors:
- Mobile phone
- Email
- Authenticator app
- SMS code
- Biometrics

---

# Why MFA Matters

MFA improves security because:
- Password alone is not enough
- Attackers need a second factor
- Compromised passwords become less useful

---

# Purpose of MFA Registration Policy

The MFA Registration Policy:
- Forces users to register for MFA

This policy:
- Increases MFA adoption
- Improves account security
- Supports self-remediation

---

# How MFA Registration Policy Works

When enabled:
- Users are prompted to register MFA during sign-in

This ensures users always have:
- A second authentication method available

---

# MFA Registration Policy Configuration

Administrators can:
- Apply policy to all users
- Apply policy to selected groups
- Include applications
- Exclude applications

Example exclusions:
- Apps without MFA support
- Apps using third-party MFA

---

# Benefits of MFA Registration Policy

Benefits include:
- Reduced account compromise
- Improved identity security
- Reduced helpdesk calls
- Better self-remediation capabilities

---

# Self-Remediation

Identity Protection supports:
- User self-remediation

Examples:
- Password reset
- MFA verification

This helps:
- Reduce helpdesk workload
- Speed up incident resolution

---

# Important Security Concepts

| Concept | Meaning |
|---|---|
| User Risk | Probability a user account is compromised |
| Sign-In Risk | Probability a sign-in attempt is malicious |
| MFA | Multifactor authentication |
| Conditional Access | Policy-based access control |
| Self-remediation | User fixes security issue independently |

---

# Steps to Enable Default Identity Protection Policies

## Step 1
Sign in to:
- Microsoft 365 admin center

Use:
- Global Administrator account

---

# Step 2

In the left navigation pane:
- Select Show all

---

# Step 3

Under:
- Admin centers

Select:
- Identity

---

# Step 4

In Microsoft Entra admin center:
- Select Identity
- Select Protection
- Select Identity Protection

---

# Step 5

On the Identity Protection dashboard:
Locate the three default policies:
- User risk policy
- Sign-in risk policy
- Multifactor authentication registration policy

---

# Step 6

Select each policy your organization wants to enforce.

---

# Step 7

On each policy page:
- Toggle Policy enforcement to Enabled

---

# Best Practices

Microsoft recommends:
- Enable all three default policies
- Enable MFA for all users
- Protect administrator accounts
- Use Conditional Access with Identity Protection
- Regularly review risky users and risky sign-ins
- Monitor identity-related alerts

---

# Security Benefits of Identity Protection

Identity Protection helps organizations:
- Detect suspicious activity
- Block risky access
- Reduce attack surface
- Protect identities automatically
- Improve Zero Trust security posture

---

# Exam Tips

## Remember the Three Default Policies

1. User Risk Policy
2. Sign-In Risk Policy
3. MFA Registration Policy

---

# User Risk vs Sign-In Risk

| Policy | Focus |
|---|---|
| User Risk Policy | Compromised user identities |
| Sign-In Risk Policy | Suspicious sign-in attempts |

---

# MFA Registration Policy Purpose

Purpose:
- Force users to register MFA

---

# Common Risk Signals

Identity Protection evaluates:
- Unusual locations
- Anonymous IPs
- Compromised credentials
- Suspicious devices
- Abnormal sign-in behavior

---

# Important Default State

All three Identity Protection policies are:
- Disabled by default

---

# Final Summary

Microsoft Entra ID Protection is a cloud-based identity security solution that:
- Detects risky users
- Detects suspicious sign-ins
- Uses machine learning
- Applies automated protections
- Integrates with Conditional Access
- Improves organizational security posture

The three default policies help organizations:
- Protect compromised accounts
- Prevent malicious sign-ins
- Enforce MFA adoption

---

# Knowledge Check Concepts

## User Risk Policy
Protects:
- Compromised identities

## Sign-In Risk Policy
Protects:
- Malicious sign-in attempts

## MFA Registration Policy
Ensures:
- Users register MFA

---
