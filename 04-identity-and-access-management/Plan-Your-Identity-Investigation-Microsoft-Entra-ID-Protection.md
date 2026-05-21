# Plan Your Identity Investigation

## Overview

Microsoft Entra ID Protection helps organizations:
- Detect compromised identities
- Investigate risky activities
- Analyze risk events
- Mitigate threats
- Remediate compromised accounts

The investigation process usually begins with:
- The Microsoft Entra ID Protection dashboard

---

# Microsoft Entra ID Protection Dashboard

The dashboard provides access to:

## Reports
- Users flagged for risk
- Risk events
- Vulnerabilities

## Settings
- Security policies
- Notifications
- Multifactor authentication registration

---

# Purpose of the Dashboard

The dashboard acts as:
- The central investigation starting point

Organizations use it to:
- Review suspicious activities
- Analyze risk events
- Investigate logs
- Determine remediation actions
- Understand how identities were compromised

---

# Sign-In Risk Events

## What is Sign-In Risk?

Sign-in risk indicates:
- The likelihood that the legitimate user did NOT perform a sign-in attempt

Risk levels include:
- High
- Medium
- Low

---

# What is Mitigation?

A mitigation is:
- An action that limits an attacker’s ability to exploit a compromised identity or device

Important:
- Mitigation does NOT restore the identity to a safe state
- Mitigation does NOT resolve previous risk events

---

# Automatic Mitigation of Risky Sign-Ins

Organizations can configure:
- Sign-in risk security policies

These policies can:
- Block risky sign-ins
- Require multifactor authentication (MFA)

---

# Why Mitigation Matters

Mitigation helps:
- Prevent attackers from exploiting stolen credentials
- Reduce damage
- Buy time for investigation and remediation

---

# Best Practices for Sign-In Risk Policies

Microsoft recommends:

## Exclude Users Who Cannot Use MFA
Examples:
- Legacy systems
- Special-purpose accounts

---

# Exclude Challenging Locales

Examples:
- Regions without helpdesk support
- Locations with limited connectivity

---

# Exclude Users Likely to Generate False Positives

Examples:
- Developers
- Security analysts
- Users using VPNs frequently

---

# High Threshold

Benefits:
- Fewer user interruptions
- Fewer MFA prompts
- Better usability

Disadvantage:
- Low and Medium risks are ignored
- Some attacks may not be blocked

---

# Low Threshold

Benefits:
- Maximum protection
- More aggressive blocking

Disadvantages:
- More MFA prompts
- Increased user friction

---

# Recommended Default Threshold

Microsoft recommends:
- Medium threshold

Reason:
- Best balance between usability and security

---

# Sign-In Risk Policy Scope

Policies apply to:
- Browser traffic
- Modern authentication

Policies do NOT apply to:
- Legacy authentication protocols

---

# Legacy Authentication Note

To prevent bypass:
- Disable WS-Trust endpoint at federated identity providers such as ADFS

---

# User Risk

## What is User Risk?

User risk indicates:
- Likelihood that a user identity is compromised

A risky user is:
- A potentially compromised account

---

# How User Risk is Calculated

Microsoft calculates user risk based on:

- Active risk events
- Severity of risk events
- Remediation actions completed

---

# Risk Event Status

Risk events have two statuses:

| Status | Meaning |
|---|---|
| Active | Still contributes to user risk |
| Closed | No longer contributes to user risk |

---

# User Risk Policies

Organizations can create Conditional Access policies to:
- Block risky users
- Force password resets
- Require MFA

---

# Manual Closure of Risk Events

Sometimes organizations must manually close risk events.

Examples:
- User account deleted
- Investigation confirms legitimate activity
- Remediation impossible

---

# Actions Available During Investigation

## 1. Resolve

Use when:
- Appropriate remediation action was completed

Examples:
- Password reset
- Account secured

Result:
- Event status changes to Closed
- No longer contributes to user risk

---

# 2. Mark as False Positive

Use when:
- Investigation proves detection was incorrect

Benefits:
- Improves Microsoft machine learning accuracy
- Reduces future false positives

Result:
- Event status changes to Closed

---

# 3. Ignore

Use when:
- No remediation was completed
- Organization wants to remove event from active list

Important:
- Should only be used in rare circumstances

Result:
- Event status changes to Closed

---

# 4. Reactivate

Use when:
- Previously closed event must become active again

Reactivated events:
- Contribute to user risk calculation

---

# Important Limitation

You CANNOT reactivate:
- Events automatically closed by remediation

Example:
- Secure password reset

---

# Remediation of User Risk Events

## What is Remediation?

Remediation:
- Restores compromised identities or devices to a safe state

Unlike mitigation:
- Remediation resolves previous risk events

---

# Ways to Remediate User Risk Events

## 1. Secure Password Reset

Organizations can:
- Reset passwords manually

---

# 2. User Risk Security Policies

Organizations can:
- Automate remediation using Conditional Access

Examples:
- Require password change
- Require MFA

---

# 3. Reimage Infected Devices

For malware-infected systems:
- Reimage device
- Remove compromise

---

# Microsoft Entra ID Protection Notifications

Identity Protection sends two automated email notifications:

1. Users at risk detected email
2. Weekly digest email

---

# Users at Risk Detected Email

Triggered when:
- Risky account detected

Email subject:
- Users at risk detected

---

# Email Includes

- Link to Users flagged for risk report
- Risk details

---

# Best Practice

Microsoft recommends:
- Immediately investigating risky users

---

# Weekly Digest Email

Provides:
- Summary of risky users
- Summary of risk events
- Ongoing monitoring visibility

---

# Microsoft Entra ID Protection Playbook

The playbook helps organizations:
- Understand Identity Protection
- Simulate risk events
- Simulate vulnerabilities
- Test Conditional Access policies
- Learn investigation workflows

---

# Key Security Concepts

| Concept | Meaning |
|---|---|
| Sign-In Risk | Likelihood sign-in is malicious |
| User Risk | Likelihood account is compromised |
| Mitigation | Limits attacker actions without fully fixing issue |
| Remediation | Fully restores identity/device to safe state |
| Active Risk Event | Contributes to risk score |
| Closed Risk Event | No longer contributes to risk score |

---

# Mitigation vs Remediation

| Mitigation | Remediation |
|---|---|
| Limits attacker activity | Fully secures identity/device |
| Temporary protection | Permanent resolution |
| Does not close previous events | Closes associated events |
| Example: Require MFA | Example: Password reset |

---

# Best Practices

Microsoft recommends:
- Use Medium threshold by default
- Enable MFA
- Investigate risky users immediately
- Reduce legacy authentication usage
- Use Conditional Access policies
- Regularly review risk reports
- Exclude service accounts carefully
- Monitor notification emails

---

# Security Benefits

Identity investigations help organizations:
- Detect compromised accounts
- Prevent lateral movement
- Stop identity attacks early
- Reduce attack surface
- Improve Zero Trust posture
- Improve visibility into threats

---

# Exam Tips

## Dashboard Starting Point

Investigations usually begin at:
- Microsoft Entra ID Protection dashboard

---

# Difference Between Mitigation and Remediation

Mitigation:
- Limits attacker capability

Remediation:
- Restores identity/device safety

---

# Recommended Default Sign-In Risk Threshold

- Medium

---

# Risk Event Statuses

1. Active
2. Closed

---

# Manual Investigation Actions

1. Resolve
2. False positive
3. Ignore
4. Reactivate

---

# Important Notification Types

1. Users at risk detected
2. Weekly digest

---

# Final Summary

Microsoft Entra ID Protection helps organizations:
- Investigate risky users
- Analyze risk events
- Mitigate attacks
- Remediate compromised identities
- Automate protections
- Improve identity security posture

Organizations should:
- Use Conditional Access
- Enable MFA
- Investigate risks immediately
- Apply risk-based policies
- Monitor notifications regularly

---

# Knowledge Check Concepts

## Mitigation
Limits attacker actions without fully restoring safety.

## Remediation
Restores identity or device to safe state.

## Recommended Risk Threshold
Medium threshold balances usability and security.

---

