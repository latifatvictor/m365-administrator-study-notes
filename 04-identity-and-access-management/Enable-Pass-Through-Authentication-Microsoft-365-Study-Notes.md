# Suggested File Name
Enable-Pass-Through-Authentication-Microsoft-365-Study-Notes.md

# Enable Pass-Through Authentication (PTA)

## Overview

Microsoft Entra Pass-Through Authentication (PTA) enables users to authenticate to Microsoft 365 services using their on-premises Active Directory credentials without storing passwords in the cloud.

PTA improves security while allowing organizations to continue using on-premises identity systems.



---

# What is Pass-Through Authentication?

Pass-Through Authentication:
- Uses on-premises Active Directory credentials
- Avoids storing passwords in Microsoft Entra ID
- Provides real-time authentication validation
- Supports Conditional Access and MFA

---

# Benefits of PTA

## Reduced Password Risks

PTA helps reduce:
- Password spraying attacks
- Phishing attacks
- Password theft risks

Because:
- Password validation happens on-premises

---

# Supports MFA and Conditional Access

PTA integrates with:
- Multifactor Authentication (MFA)
- Conditional Access policies

Even if credentials are compromised:
- Additional authentication factors are still required

Examples:
- One-time passcodes
- Biometrics
- Microsoft Authenticator approval

---

# Real-Time Authentication

PTA validates credentials directly against:
- On-premises Active Directory

Advantages:
- Immediate enforcement of account states
- Real-time password policy validation
- Sign-in hour enforcement
- Improved authentication accuracy

---

# Why Organizations Use PTA

Organizations implement PTA when they:
- Want to maintain on-premises identity systems
- Need immediate enforcement of account restrictions
- Want stronger password security
- Prefer not to store password hashes in the cloud

Source: :contentReference[oaicite:1]{index=1}

---

# Traditional Authentication Approach

Previously, organizations used:
- Active Directory Federation Services (AD FS)

AD FS allowed:
- On-premises authentication for cloud services

---

# Challenges with AD FS

AD FS deployments were often:
- Complex
- Expensive
- Difficult to manage
- Infrastructure heavy

This complexity led Microsoft to introduce:
- Pass-Through Authentication (PTA)

---

# PTA Compared to AD FS

## PTA Advantages

PTA is:
- Easier to deploy
- Easier to maintain
- Less infrastructure intensive
- Simpler to troubleshoot

Unlike AD FS:
- No perimeter network deployment required
- Communication is outbound only

---

# Automatic Failover

If PTA fails:
- Microsoft Entra ID can automatically fail over to Password Hash Synchronization (PHS)

Requirement:
- PHS automatic failover must be enabled

---

# PTA Architecture

PTA works using:
- Connector agents installed on-premises

These agents:
- Listen for authentication requests
- Validate credentials against Active Directory
- Return results to Microsoft Entra ID

---

# High Availability

Organizations can deploy:
- Multiple PTA agents

Benefits:
- High availability
- Redundancy
- Load balancing

Microsoft recommends:
- At least two connectors

---

# PTA Communication Design

Important security point:
- All PTA communication is outbound only

Benefits:
- No inbound firewall openings required
- Reduced attack surface
- Simpler network configuration

---

# PTA Sign-In Process

## Step 1

User accesses:
- Microsoft 365 service
- Cloud application

---

# Step 2

Microsoft Entra ID displays:
- Sign-in page

---

# Step 3

User enters:
- Username
- Password

---

# Step 4

Microsoft Entra ID checks:
- Whether PTA is enabled for the domain

---

# Step 5

User credentials are placed:
- On the PTA connector queue

---

# Step 6

On-premises PTA agent:
- Retrieves credentials
- Authenticates user against Active Directory

---

# Step 7

Authentication response returns:
- To Microsoft Entra ID

---

# Step 8

Access is:
- Granted or denied

Based on:
- Active Directory response

---

# PTA Deployment Requirements

Organizations must:
- Run Microsoft Entra Connect Sync Setup Wizard
- Select Pass-through Authentication option

---

# First Connector Requirement

The first PTA connector:
- Must be installed on the same server as Microsoft Entra Connect Sync

---

# Additional Connectors

Microsoft recommends:
- Installing additional connectors on separate servers

Purpose:
- Redundancy
- Load balancing
- High availability

---

# Connector Installation

Additional PTA connectors use:
- Microsoft Entra Application Proxy Connector

Installed separately on:
- Additional servers

---

# Server Requirements

PTA connector servers should:
- Be domain joined
- Have connectivity to Active Directory
- Support outbound internet communication

---

# PTA Required Ports

## Port 80

Purpose:
- HTTP traffic
- TLS/SSL certificate validation
- Certificate revocation list downloads

---

# Port 443

Purpose:
- User authentication against Microsoft Entra ID

---

# Port 8080 / 443

Purpose:
- Connector bootstrap
- Connector updates

---

# Port 9090

Purpose:
- Connector registration

Note:
- Required only during registration

---

# Port 9091

Purpose:
- Automatic renewal of trust certificates

---

# Ports 9352 and 5671

Purpose:
- Communication between Connector and Microsoft Entra services

Used for:
- Incoming authentication requests

---

# Port 9350

Optional port used for:
- Better performance for incoming requests

---

# Ports 10100–10120

Purpose:
- Connector responses back to Microsoft Entra ID

---

# Security Benefits of PTA

PTA provides:
- Real-time authentication
- Reduced password exposure
- MFA integration
- Conditional Access integration
- No inbound firewall exposure

---

# PTA Best Practices

Microsoft recommends:
- Deploying multiple PTA connectors
- Enabling MFA
- Using Conditional Access
- Enabling PHS failover
- Monitoring authentication logs

---

# PTA and User Experience

Benefits for users:
- Single set of credentials
- Seamless authentication
- Improved login experience
- Reduced password fatigue

---

# PTA and Hybrid Identity

PTA supports:
- Hybrid identity environments

Users can:
- Access on-premises resources
- Access cloud services
- Use same credentials everywhere

---

# Key Takeaways

Pass-Through Authentication:
- Validates passwords on-premises
- Reduces password-related risks
- Supports MFA and Conditional Access
- Is simpler than AD FS
- Uses outbound-only communication
- Supports high availability through multiple connectors

PTA is ideal for organizations that:
- Require on-premises authentication
- Want stronger identity security
- Prefer not to store passwords in the cloud
