# Investigate Authentication Issues Using Sign-In Logs

## Overview

Microsoft Entra ID provides activity logs that help administrators:
- Monitor system health
- Investigate authentication issues
- Track user activity
- Detect suspicious behavior
- Troubleshoot access problems

---

# Types of Microsoft Entra Activity Logs

Microsoft Entra admin center provides three major activity logs:

| Log Type | Purpose |
|---|---|
| Sign-in logs | Tracks user sign-ins and access activity |
| Audit logs | Tracks configuration and tenant changes |
| Provisioning logs | Tracks provisioning-related activities |

---

# Sign-In Logs

## Purpose

Sign-in logs provide:
- Authentication details
- Access attempts
- User behavior insights
- Security investigation data

---

# Questions Sign-In Logs Help Answer

Examples include:

- How many users signed into an app this week?
- How many failed sign-ins occurred?
- Which browsers are users using?
- Which operating systems are being used?
- Which resources are being accessed?
- Which managed identities are accessing resources?

---

# Sign-In Log Core Details

Sign-in logs identify:

| Category | Description |
|---|---|
| Who | The user or identity performing the sign-in |
| How | The application/client used |
| What | The target resource accessed |

---

# Four Types of Sign-In Logs

Microsoft Entra sign-in events include:

1. Interactive user sign-ins
2. Non-interactive user sign-ins
3. Service principal sign-ins
4. Managed identity sign-ins

---

# Classic Sign-In Logs

Classic sign-in logs:
- Only contain interactive sign-ins

---

# Important Note

Sign-in log entries:
- Are system generated
- Cannot be edited
- Cannot be deleted by administrators

---

# Interactive User Sign-Ins

## Definition

Interactive sign-ins occur when:
- Users manually authenticate
- Users provide authentication factors

Examples:
- Passwords
- MFA approvals
- Biometrics
- QR codes

---

# Examples of Interactive Sign-Ins

Includes:

- Username and password entry
- SMS MFA challenge
- Windows Hello biometric login
- AD FS federated sign-ins

---

# Additional Information in Interactive Logs

Interactive logs show:
- Sign-in location
- Conditional Access information

---

# Interactive Sign-In Limitations

## Non-Interactive Sign-Ins May Appear

Some non-interactive sign-ins:
- May still appear as interactive

Examples:
- FIDO2 key usage

Reason:
- Historical logging design before separate non-interactive logs existed

---

# Passthrough Sign-Ins

## Definition

A passthrough token:
- Is issued without authorization
- Does not grant access

---

# Passthrough Example

Scenario:
- User signs into Contoso
- Attempts access to Fabrikam
- No authorization exists

Result:
- Passthrough token issued
- Access denied
- Home tenant logs may not record the attempt

---

# Service Principal Logging Limitation

First-party Microsoft app-only tokens:
- May not appear in service principal logs

These are:
- Internal Microsoft operations
- Excluded to reduce unnecessary log volume

---

# Non-Interactive User Sign-Ins

## Definition

Non-interactive sign-ins occur:
- Without direct user interaction

Microsoft Entra refreshes tokens automatically.

---

# User Experience

Users usually:
- Do not notice these sign-ins
- Experience them silently in the background

---

# Examples of Non-Interactive Sign-Ins

Includes:

- OAuth refresh token requests
- OAuth authorization code exchanges
- Seamless SSO
- Office app token reuse
- Mobile session token renewals

---

# Additional Fields in Non-Interactive Logs

Includes:
- Resource ID
- Number of grouped sign-ins

---

# Sign-In Aggregation

Microsoft Entra groups:
- Similar non-interactive sign-ins together

Purpose:
- Improve readability
- Reduce log clutter

---

# Aggregation Criteria

Non-interactive sign-ins are grouped when these match:

- Application
- User
- IP address
- Status
- Resource ID

---

# Aggregated Sign-In Indicators

If grouped:
- # sign-ins column becomes greater than 1

---

# Time Aggregation Filters

Administrators can aggregate by:
- 1 hour
- 6 hours
- 24 hours

---

# Important IP Address Note

For confidential clients:
- Displayed IP may not equal actual source IP

Instead:
- Original token issuance IP is shown

---

# Service Principal Sign-Ins

## Definition

Service principal sign-ins:
- Are non-user sign-ins
- Performed by applications/services

Authentication methods include:
- Certificates
- Client secrets

---

# Examples of Service Principal Sign-Ins

Includes:

- Microsoft Graph access using certificates
- OAuth client credential flow authentication

---

# Service Principal Aggregation

Logs aggregate when these match:

- Service principal name or ID
- Status
- IP address
- Resource name or ID

---

# Managed Identity Sign-Ins

## Definition

Managed identities:
- Are Azure resources with Azure-managed credentials

Purpose:
- Simplify credential management

---

# Example

A virtual machine:
- Uses managed identity
- Requests an access token from Microsoft Entra ID

---

# Managed Identity Aggregation

Managed identity logs aggregate when these match:

- Managed identity name or ID
- Status
- Resource name or ID

---

# Viewing Sign-In Details

Administrators can:
- Expand grouped sign-ins
- View detailed timestamps
- Investigate authentication activity

---

# Importance of Sign-In Logs

Sign-in logs help organizations:

- Investigate authentication failures
- Detect suspicious access
- Analyze user behavior
- Monitor application usage
- Troubleshoot Conditional Access
- Detect compromised accounts

---

# Key Security Benefits

Sign-in logs support:

- Identity monitoring
- Threat detection
- Incident response
- Compliance investigations
- Access auditing

---

# Summary

Microsoft Entra sign-in logs provide detailed visibility into:
- User authentication
- Application access
- Service authentication
- Managed identity usage

The four major sign-in types are:

1. Interactive user sign-ins
2. Non-interactive user sign-ins
3. Service principal sign-ins
4. Managed identity sign-ins

Sign-in logs are essential for:
- Security monitoring
- Troubleshooting
- Compliance
- Authentication analysis

