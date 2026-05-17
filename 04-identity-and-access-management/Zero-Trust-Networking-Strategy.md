# Examine Microsoft’s Strategy for Zero Trust Networking

## Overview

The Zero Trust security model focuses on protecting:
- Users
- Devices
- Applications
- Networks
- Infrastructure
- Data

Instead of trusting anything inside the corporate network, Zero Trust assumes:
- Breaches are inevitable
- Every request must be verified
- Every session may be risky

---

# Big Data and Zero Trust

Modern organizations process enormous volumes of data often referred to as:
- Big Data

Big data is characterized by:
- Volume
- Velocity
- Variety

Organizations analyze this data to identify:
- Trends
- Behaviour patterns
- Threats
- Business insights

---

# Why Big Data Matters in Zero Trust

Modern IT environments no longer operate within clearly defined network boundaries.

Cloud services, remote work, mobile devices, and BYOD models have expanded organizational attack surfaces significantly.

This means:
- Traditional perimeter security is no longer enough.

---

# Core Objectives of Zero Trust Networking

Zero Trust networking focuses on three major objectives:

1. Prepare for attacks before they happen
2. Minimize the impact of breaches
3. Increase the difficulty of compromising systems

---

# Zero Trust Principles

Organizations should follow three Zero Trust principles:

1. Verify explicitly
2. Use least-privileged access
3. Assume breach

---

# Verify Explicitly

Always authenticate and authorize access requests using:
- User identity
- Device health
- Location
- Application
- Service or workload
- Data classification
- Risk signals
- Anomalies

---

# Use Least-Privileged Access

Organizations should:
- Limit permissions
- Apply Just-In-Time access
- Apply Just-Enough-Access
- Use adaptive access policies
- Protect sensitive data

---

# Assume Breach

Organizations should assume attackers may already exist within the environment.

Security strategies should:
- Limit blast radius
- Prevent lateral movement
- Encrypt sessions end to end
- Use analytics for detection

---

# Traditional Perimeter-Based Security

Traditional networks assumed:
- Anything inside the network is trusted

This model is now obsolete because:
- Remote work increased
- Cloud adoption expanded
- BYOD usage increased
- Attackers can compromise internal devices

---

# Risks of Traditional Networks

If attackers compromise one endpoint:
- They may move laterally across the network
- They may access additional systems
- They may steal sensitive data

---

# Zero Trust Network Architecture

Zero Trust networking removes trust based on:
- Network location

Instead, it uses:
- Identity trust
- Device trust
- Risk evaluation
- Policy enforcement

to control access.

---

# Core Components of a Zero Trust Network

A Zero Trust network typically includes:

1. Identity Provider
2. Device Directory
3. Policy Evaluation Service
4. Access Proxy

---

# Identity Provider

The identity provider:
- Manages user identities
- Stores authentication information
- Verifies user sessions

Example:
- Microsoft Entra ID

---

# Device Directory

The device directory maintains:
- Device inventory
- Device compliance status
- Device health information

Examples include:
- Corporate laptops
- Mobile devices
- BYOD devices

---

# Policy Evaluation Service

The policy evaluation service determines:
- Whether users or devices satisfy organizational security policies

It evaluates:
- Risk
- Compliance
- User role
- Device state

---

# Access Proxy

The access proxy:
- Grants or blocks access to resources based on trust signals and policy decisions

---

# Dynamic Trust Decisions

Zero Trust networking makes:
- Dynamic trust decisions

based on:
- User identity
- Device compliance
- Session risk
- Application sensitivity

---

# Preventing Lateral Movement

Attackers often use:
- Hopping

to move across systems after compromising one device.

Zero Trust helps prevent this by:
- Segmenting access
- Verifying sessions continuously
- Restricting privileged access

---

# Modern Workplace Support

Zero Trust supports modern work environments by allowing employees to:
- Work remotely
- Access cloud services securely
- Use mobile devices safely

without relying on traditional perimeter security.

---

# Initial Zero Trust Deployment Objectives

Microsoft recommends organizations first focus on:

## Network Segmentation
- Cloud micro-perimeters
- Basic micro-segmentation

## Threat Protection
- Cloud-native filtering
- Protection against known threats

## Encryption
- Encrypt user-to-app traffic

---

# Advanced Zero Trust Deployment Objectives

After initial deployment, organizations should focus on:

## Advanced Network Segmentation
- Fully distributed micro-perimeters
- Deep micro-segmentation

## Advanced Threat Protection
- Machine learning-based detection
- Context-aware filtering

## Full Encryption
- Encrypt all traffic

---

# Microsoft Entra Conditional Access

Conditional Access is the foundational component of Zero Trust networking in Microsoft environments.

It helps organizations:
- Evaluate access requests dynamically
- Enforce access controls
- Reduce risk

---

# Conditional Access Factors

Conditional Access evaluates:
- User identity
- User role
- Group membership
- Device health
- Device compliance
- Application
- Location
- Sign-in risk
- Session risk

---

# Conditional Access Decisions

Conditional Access can:
- Allow access
- Block access
- Require MFA
- Restrict sessions
- Require Terms of Use acceptance

---

# Example Conditional Access Policies

Examples include:
- Require MFA from unknown locations
- Block access from embargoed countries
- Require compliant devices
- Restrict access to high-risk applications

---

# Sign-In Risk

Microsoft Entra ID Protection calculates:
- Sign-In Risk

based on suspicious authentication behaviour.

Examples include:
- Impossible travel
- Anonymous IP addresses
- Malware-linked sign-ins
- Leaked credentials

---

# Device Trust Signals

Microsoft uses:
- Device compliance
- Device health
- Runtime security signals

to determine whether a device should access resources.

---

# Security Defaults

Microsoft provides:
- Security Defaults

for Microsoft Entra ID environments.

These defaults:
- Enable baseline protections
- Encourage MFA
- Reduce account compromise risks

---

# Benefits of Conditional Access

Conditional Access helps organizations:
- Improve security
- Reduce unauthorized access
- Protect sensitive data
- Balance productivity and security

---

# Continuous Access Evaluation

Microsoft Entra ID continuously:
- Evaluates sessions
- Monitors risk
- Applies policies dynamically

This ensures:
- Only compliant access remains active

---

# Knowledge Check

Question:
Which of the following can Holly use to control access to resources at Lucerne Publishing?

Options:
- External sharing policies
- Sign-in risk
- Data loss prevention policies

Correct Answer:
- Sign-in risk

---

# Key Takeaway

Zero Trust networking assumes breaches are inevitable and requires continuous verification of users, devices, applications, and sessions. Microsoft Entra Conditional Access provides dynamic policy enforcement based on user identity, device compliance, sign-in risk, and session context to secure modern hybrid environments.


