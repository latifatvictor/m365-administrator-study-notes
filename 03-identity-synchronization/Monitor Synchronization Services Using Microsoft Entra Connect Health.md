# Monitor Synchronization Services Using Microsoft Entra Connect Health

## Overview

Microsoft Entra Connect Health helps organisations monitor and maintain their hybrid identity infrastructure.

It provides visibility into:

- Synchronisation health
- AD FS health
- Active Directory health
- Performance issues
- Alerts
- Usage analytics
- Configuration settings

---

# Important Note

Azure Active Directory is now called:

```text
Microsoft Entra ID
```

---

# What Microsoft Entra Connect Health Does

Microsoft Entra Connect Health monitors:

- On-premises identity infrastructure
- Microsoft Entra Connect Sync services
- AD FS services
- Active Directory Domain Services (AD DS)

It helps organisations maintain a reliable connection between:

```text
On-premises Active Directory ↔ Microsoft Entra ID ↔ Microsoft 365
```

---

# How It Works

Microsoft Entra Connect Health uses:

```text
Health monitoring agents
```

These agents are installed on the relevant servers.

The agents send monitoring information to the:

```text
Microsoft Entra Connect Health portal
```

---

# What You Can Monitor

Using the Microsoft Entra Connect Health portal, organisations can monitor:

- Alerts
- Synchronisation status
- Performance
- Usage patterns
- Configuration settings
- Replication status
- AD FS activity

---

# Main Monitoring Areas

## 1. Microsoft Entra Connect Health for Sync

This monitors:

```text
Directory synchronisation between on-premises AD and Microsoft Entra ID
```

---

## What It Provides

- Sync alerts
- Sync failures
- Sync performance
- Synchronisation analytics
- Synchronisation reliability information

---

# Key Features of Connect Health for Sync

## Alerts

Administrators can:

- View alerts
- Investigate issues
- Take corrective action

This helps maintain reliable synchronisation.

---

## Email Notifications

Critical alerts can generate:

```text
Email notifications
```

This allows faster response to issues.

---

## Performance Monitoring

Administrators can monitor:

- Synchronisation performance
- Processing delays
- Synchronisation bottlenecks

---

# Real Work Scenario

A synchronisation cycle suddenly fails because of duplicate proxyAddresses.

Microsoft Entra Connect Health generates:

- An alert
- Email notification
- Synchronisation error details

The admin can quickly investigate and resolve the issue.

---

# 2. Microsoft Entra Connect Health for AD FS

This monitors:

```text
Active Directory Federation Services (AD FS)
```

---

# What It Provides

- AD FS alerts
- Authentication activity
- Usage analytics
- Performance metrics
- Federation server monitoring

---

# Real Work Scenario

Users cannot sign in because an AD FS federation server is down.

Microsoft Entra Connect Health identifies:

- The failed server
- Authentication errors
- Performance degradation

This helps administrators resolve the outage faster.

---

# 3. Microsoft Entra Connect Health for AD DS

This monitors:

```text
Active Directory Domain Services
```

---

# What It Provides

- Forest health
- Replication status
- Domain controller monitoring
- AD DS alerts

---

# Real Work Scenario

A domain controller replication issue occurs between sites.

Connect Health highlights:

- Replication failure
- Affected domain controllers
- Replication latency

---

# Microsoft Entra Connect Health Portal

The portal provides a central dashboard for monitoring.

When opened for the first time, the portal displays:

```text
Quick Start page
```

---

# Quick Start Page Features

## Get Tools

Allows administrators to:

- Download Health agents
- Install monitoring components

---

## Documentation

Provides setup and troubleshooting guidance.

---

## Feedback

Allows organisations to submit product feedback.

---

# Portal Sections

---

# Microsoft Entra Connect (Sync)

Displays all monitored:

```text
Microsoft Entra Connect Sync servers
```

---

# Active Directory Federation Services

Displays all monitored:

```text
AD FS services
```

Selecting a service displays:

- Overview
- Properties
- Alerts
- Monitoring data
- Usage analytics

---

# Active Directory Domain Services

Displays all monitored:

```text
Active Directory forests
```

Provides:

- Alerts
- Monitoring
- Replication status

---

# Configure Section

The Configure section allows administrators to enable or disable settings.

---

# Auto Update

Automatically updates the:

```text
Microsoft Entra Connect Health agent
```

to the latest version.

---

# Why Auto Update Is Useful

- Keeps monitoring agents current
- Improves reliability
- Reduces manual maintenance
- Provides latest fixes and features

---

# Allow Microsoft Access for Troubleshooting

Allows Microsoft support engineers to view health data for troubleshooting purposes.

Important:

```text
Disabled by default
```

---

# Licensing Requirement

Microsoft Entra Connect Health requires:

```text
Microsoft Entra Premium licensing
```

---

# Benefits of Microsoft Entra Connect Health

- Centralised monitoring
- Faster troubleshooting
- Better hybrid identity visibility
- Early issue detection
- Improved synchronisation reliability
- Improved AD FS monitoring
- Better operational awareness

---

# Common Issues It Helps Detect

- Synchronisation failures
- Duplicate attributes
- Password sync issues
- AD FS outages
- Replication failures
- Performance bottlenecks
- Authentication failures
- Service interruptions

---

# Real IT Support Examples

## Example 1 - Password Hash Sync Failure

A password synchronisation process fails.

Connect Health alerts the administrator before users begin reporting sign-in issues.

---

## Example 2 - AD FS Certificate Expiry

An AD FS certificate is close to expiring.

Connect Health generates alerts to help avoid authentication outages.

---

## Example 3 - Replication Delay

A domain controller stops replicating properly.

Connect Health identifies the replication issue and affected servers.

---

# Important Exam Points

- Microsoft Entra Connect Health monitors hybrid identity infrastructure
- It uses monitoring agents installed on servers
- Connect Health for Sync monitors directory synchronisation
- Connect Health for AD FS monitors federation services
- Connect Health for AD DS monitors Active Directory forests
- The portal provides alerts, analytics, and monitoring
- Email notifications are available for critical alerts
- Auto update can automatically update agents
- Microsoft Entra Connect Health requires Microsoft Entra Premium licensing

---

# Common Interview Questions

## Q1: What does Microsoft Entra Connect Health monitor?

It monitors:

- Microsoft Entra Connect Sync
- AD FS
- Active Directory Domain Services

---

## Q2: What is the purpose of Microsoft Entra Connect Health?

To monitor and provide insight into hybrid identity infrastructure and synchronisation health.

---

## Q3: What does Connect Health for Sync monitor?

Synchronisation between on-premises Active Directory and Microsoft Entra ID.

---

## Q4: Does Microsoft Entra Connect Health support email alerts?

Yes. It can send email notifications for critical alerts.

---

## Q5: What licensing is required for Microsoft Entra Connect Health?

Microsoft Entra Premium licensing.

---

## Q6: What can administrators see in the Health portal?

- Alerts
- Performance data
- Usage analytics
- Configuration settings
- Replication information

---

## Q7: What does Auto Update do?

Automatically updates the Microsoft Entra Connect Health agents.

---

# Summary

Microsoft Entra Connect Health is a monitoring solution for hybrid identity environments.

It provides monitoring for:

- Synchronisation services
- AD FS
- Active Directory Domain Services

Using health agents and the Connect Health portal, administrators can:

- Detect issues early
- Monitor synchronisation
- Receive alerts
- View performance data
- Improve reliability of hybrid identity services
