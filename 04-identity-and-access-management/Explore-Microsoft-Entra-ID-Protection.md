# Explore Microsoft Entra ID Protection

## Overview

Microsoft Entra ID Protection (formerly Azure AD Identity Protection) is a cloud-based security solution that helps organizations:
- Detect compromised identities
- Monitor suspicious activity
- Investigate risky sign-ins
- Automatically respond to threats
- Protect user identities using risk-based policies

Identity Protection uses:
- Machine learning
- Heuristics
- Threat intelligence
- Real-time analytics

to detect identity-related risks.

---

# Why Identity Protection Matters

Most security breaches occur because:
- Attackers steal user credentials
- Compromised accounts are used for lateral movement
- Low privilege accounts are escalated into privileged access

Organizations must:
- Protect all identities
- Detect compromised accounts
- Prevent abuse
- Automate remediation

---

# Key Features of Microsoft Entra ID Protection

Microsoft Entra ID Protection provides:

- Risk detection
- Risk investigation
- Automated remediation
- Conditional Access integration
- User risk scoring
- Sign-in risk scoring
- Alerting and reporting

---

# Identity Protection Architecture

Microsoft Entra ID Protection:
- Operates inside Microsoft Entra ID
- Detects malicious activity
- Calculates identity risk levels
- Applies automated protections

---

# Microsoft Threat Intelligence Scale

Microsoft detects:
- More than 10,000 attacker-controlled IPs daily
- More than 10 million malicious sign-in attempts daily
- Approximately 1.5 million newly protected credential pairs daily

This intelligence powers:
- Risk detection
- Threat analytics
- Adaptive machine learning

---

# Core Capabilities

## 1. Detecting Vulnerabilities and Risky Accounts

Identity Protection:
- Generates user risk scores
- Generates sign-in risk scores
- Detects compromised accounts
- Detects suspicious sign-ins
- Detects configuration vulnerabilities

Examples:
- Leaked credentials
- Brute-force attacks
- Anonymous IP sign-ins
- Impossible travel

---

# 2. Investigating Risk Events

Identity Protection helps organizations:
- Investigate suspicious activities
- View remediation recommendations
- Analyze attack patterns

It uses:
- Advanced machine learning
- Threat signals
- User behavior analytics

Signals include:
- Brute-force attacks
- Leaked credentials
- Impossible travel
- Unfamiliar sign-in locations
- Infected devices

---

# 3. Risk-Based Conditional Access Policies

Organizations can configure:
- Automated responses to risky events

Examples:
- Block sign-ins
- Require MFA
- Force password reset
- Require credential changes

---

# Example of Adaptive Protection

If Microsoft Entra ID Protection detects:
- Anonymous IP
- Bot-controlled network
- Suspicious location

then Conditional Access can:
- Trigger MFA
- Block access
- Require password reset

---

# Impossible Travel Detection

Identity Protection detects:
- Impossible sign-in activity

Example:
- User signs in from New York
- Three hours later signs in from Sydney

This is considered:
- Impossible travel
- Suspicious activity

---

# Integration with Other Microsoft Security Tools

Identity Protection integrates with:
- Conditional Access
- Microsoft Entra MFA
- Microsoft Entra PIM
- Cloud App Discovery
- Enterprise Mobility + Security (EMS)

---

# Microsoft Entra ID Protection Roles

Users must have specific roles to access Identity Protection.

Supported roles include:
- Security Reader
- Security Operator
- Security Administrator
- Global Reader
- Global Administrator

---

# Role Permissions

| Role | Can Do | Cannot Do |
|---|---|---|
| Security Administrator | Full access to Identity Protection | Reset passwords |
| Security Operator | View reports, dismiss risks, confirm compromise | Configure policies |
| Security Reader | Read reports and overview | Configure policies |
| Global Reader | Read-only access | Administrative changes |
| Global Administrator | Full access | None |

---

# Risk Detection Types

Microsoft Entra ID Protection detects:
- Sign-in risk
- User risk

---

# Sign-In Risk

Sign-in risk reflects:
- Probability that sign-in is unauthorized

---

# Types of Sign-In Risk

## Real-Time Risk

Detected during authentication.

Examples:
- Anonymous IP
- TOR browser
- Bot activity

---

# Total Sign-In Risk

Combination of:
- Real-time risks
- Offline analysis
- Later detections

Example:
- Impossible travel discovered later

---

# User Risk

User risk reflects:
- Likelihood that account is compromised

Includes:
- Sign-in risks
- User detections
- Offline detections
- Risk history

---

# Automated Notifications

Identity Protection sends:
- Users at risk detected alerts
- Weekly digest emails

---

# Users at Risk Detected Email

Triggered when:
- User reaches specified risk level

Default trigger:
- High risk

---

# Email Includes

- User details
- Risk information
- Link to risky users report

---

# Best Practice

Microsoft recommends:
- Immediately investigating risky users

---

# Alert Configuration Options

Administrators can configure:
- Risk threshold
- Email recipients
- Notification behavior

---

# Risk Recalculation Notifications

New notifications are generated when:
- Risk score recalculates
- New risky activity occurs

---

# Email Aggregation

To prevent overload:
- Identity Protection aggregates alerts within 5 seconds

Multiple risky users:
- Sent in a single email

---

# Self-Remediation

If self-remediation is enabled:
- Users may fix their own risk

Examples:
- MFA verification
- Password reset

Administrators can still view:
- Remediated risky users
- Remediated risky sign-ins

---

# Weekly Digest Email

Weekly digest summarizes:
- New risky users
- New risky sign-ins
- Links to reports

Administrators can:
- Enable or disable digest
- Configure recipients

---

# Configuring Notifications

Configure under:
Protection → Identity Protection

Options include:
- Users at risk detected alerts
- Weekly digest

---

# Risk-Based Conditional Access

Identity Protection can automatically:
- Block risky sign-ins
- Require MFA
- Force password change

This helps:
- Reduce account compromise
- Protect identities in real time

---

# Conditional Access Integration

Conditional Access administrators can:
- Use user risk as policy condition
- Use sign-in risk as policy condition

---

# Security Benefits

Identity Protection helps organizations:
- Detect threats early
- Prevent account compromise
- Reduce attack surface
- Automate remediation
- Improve visibility
- Strengthen Zero Trust strategy

---

# Important Exam Points

## What Detects Suspicious Activity?

- Machine learning
- Heuristics
- Threat intelligence

---

# Two Main Risk Types

1. Sign-in risk
2. User risk

---

# Real-Time Risk Examples

- Anonymous IP
- Bot networks
- Suspicious sign-in location

---

# Impossible Travel

Example:
- New York to Sydney within hours

---

# Automatic Responses

Identity Protection can:
- Require MFA
- Block sign-ins
- Force password reset

---

# Default Users at Risk Alert Level

- High risk

---

# Key Notification Types

1. Users at risk detected
2. Weekly digest

---

# Best Practices

Microsoft recommends:
- Enable MFA
- Configure risk-based Conditional Access
- Investigate risky users immediately
- Monitor weekly digest reports
- Use least privilege access
- Protect all identities

---

# Important Concepts

| Concept | Meaning |
|---|---|
| Sign-in Risk | Risk of unauthorized authentication |
| User Risk | Likelihood account is compromised |
| Impossible Travel | Physically impossible sign-in pattern |
| Adaptive Remediation | Automated protective response |
| Conditional Access | Policy-based access control |
| MFA | Multifactor authentication |

---

# Final Summary

Microsoft Entra ID Protection is a cloud-based identity security solution that:
- Detects compromised identities
- Monitors risky sign-ins
- Uses machine learning
- Automates remediation
- Integrates with Conditional Access
- Helps organizations reduce identity-based attacks

Identity Protection provides:
- Risk visibility
- Threat intelligence
- Automated security controls
- Risk-based access enforcement

---

# Exam Tip

Remember:

Identity Protection focuses on:
- User risk
- Sign-in risk
- Risk-based Conditional Access
- Automated remediation
- Machine learning-based detections

---

# Knowledge Check Answer

Q: How does Microsoft Entra ID Protection investigate risk events?

Answer:
It uses advanced machine learning to detect suspicious activities based on signals.

---
