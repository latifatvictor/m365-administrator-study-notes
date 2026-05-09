# Deploy Microsoft 365 Apps for Enterprise with Microsoft Configuration Manager

---

# 📌 Overview

Microsoft Configuration Manager (Current Branch), now part of Microsoft Endpoint Manager, enables organizations to centrally deploy and manage Microsoft 365 Apps for enterprise.

Managed deployment provides:
- Greater administrative control
- Centralized configuration
- Scalable enterprise deployment
- Controlled update management
- Improved reporting and monitoring

---

# 🖥️ What is Microsoft Endpoint Manager?

Microsoft Endpoint Manager combines:
- Microsoft Configuration Manager (SCCM)
- Microsoft Intune

This integration allows organizations to:
- Manage on-premises devices
- Manage cloud devices
- Use co-management
- Simplify administration

---

# 🚀 Benefits of Using Configuration Manager

Configuration Manager provides:

- Large-scale deployment support
- Centralized Office management
- Update management
- Reporting dashboards
- Advanced customization
- Peer caching
- Application settings deployment

---

# 📊 Key Office Deployment Features

Configuration Manager includes:

- Office Client Management Dashboard
- Office Customization Tool integration
- Automatic MSI Office removal
- Office update management
- Peer cache support
- Application configuration deployment

---

# 🧩 Office Client Management Dashboard

The dashboard allows admins to:
- Deploy Office
- Monitor versions
- Track update channels
- View deployment status
- Monitor languages installed

---

# ⚙️ Office Customization Tool (OCT)

The integrated Office Customization Tool enables:
- App selection
- Update channel selection
- Language configuration
- Silent installs
- EULA acceptance
- Office settings management

---

# 📌 Recommended Best Practice Deployment Model

Microsoft recommends creating:

## 1️⃣ Pilot Deployment

- Semi-Annual Enterprise Channel (Preview)
- Small test collection
- Early validation group

---

## 2️⃣ Broad Deployment

- Semi-Annual Enterprise Channel
- Organization-wide deployment
- Stable production users

---

# 📦 Recommended Applications

Microsoft recommends building:

- One 64-bit Semi-Annual Enterprise Channel package
- One 64-bit Semi-Annual Enterprise Channel Preview package

---

# 📌 Deployment Collections

Recommended collections:

| Collection | Purpose |
|---|---|
| Pilot Group | Testing Preview Channel |
| Broad Group | Production deployment |

---

# 🔄 Update Channels

Common channels include:

- Semi-Annual Enterprise Channel
- Semi-Annual Enterprise Channel (Preview)

---

# 📌 Why Use Pilot Groups?

Pilot groups help organizations:
- Test updates safely
- Identify compatibility issues
- Validate business applications
- Reduce production risk

---

# 🛠️ Step 1 — Review Configuration Manager Infrastructure

Before deployment:

- Upgrade to Current Branch
- Verify internet connectivity
- Configure deployment shares
- Review network performance

---

# 📌 Important Requirements

Client devices must:
- Access the Internet for activation
- Reach Microsoft services over HTTPS 443

---

# 🌐 Required URLs

Add to Trusted Sites if Enhanced Security enabled:

- https://office.com
- https://officeconfig.msocdn.com

---

# 📡 Peer Cache Feature

Peer cache:
- Reduces WAN bandwidth usage
- Shares installation files locally
- Helps remote offices

---

# 📌 Peer Cache Benefits

Useful for:
- Remote branches
- Limited bandwidth sites
- Large Office deployments

---

# 🧩 Step 2 — Review Collections

Create collections representing:

- Pilot users
- Production users

Collections control:
- Deployment targeting
- Update rollout
- Reporting scope

---

# 🚀 Step 3 — Create Pilot Office Application

Navigate to:

Software Library → Overview → Office 365 Client Management

---

# 📌 Office 365 Installer Wizard

Use:
- Office 365 Installer Wizard

to create deployment packages.

---

# ⚙️ Recommended Office Customization Settings

---

# Software Selection

Select:
- Microsoft 365 Apps for enterprise

Optional:
- Visio
- Project

---

# Update Channel

Pilot Group:
- Semi-Annual Enterprise Channel (Preview)

---

# Languages

Include:
- All required language packs

---

# Upgrades

Enable:
- Automatically remove previous MSI Office versions

---

# Display Settings

Recommended:
- Display Level = Off
- Automatically Accept EULA = On

---

# 📂 Application Settings

Admins can configure:
- VBA macro notifications
- Default save locations
- File formats
- Office policies

---

# 🚀 Step 4 — Deploy to Broad Group

After pilot testing:

- Create production deployment
- Use same settings
- Change update channel to:
  - Semi-Annual Enterprise Channel

---

# 📊 Step 5 — Review Exit Criteria

Use:
- Office 365 Client Management Dashboard

to validate deployment success.

---

# 📌 Dashboard Reports Include

- Number of Office clients
- Office versions
- Installed languages
- Update channels

---

# ⚠️ Important Inventory Requirement

If dashboard data missing:
- Enable hardware inventory
- Enable Office 365 ProPlus Configurations inventory class

---

# 🔐 Security & Management Benefits

Managed deployments provide:
- Better compliance
- Controlled updates
- Reduced user disruption
- Improved security
- Centralized governance

---

# 🧠 Real Work Example

Scenario:
A multinational company deploys Microsoft 365 Apps to 15,000 devices globally.

Deployment strategy:
- Pilot collection tests Preview channel
- Production collection uses stable channel
- Peer cache enabled at remote sites
- Office updates controlled via SCCM

Benefits:
- Reduced WAN usage
- Controlled rollout
- Faster troubleshooting
- Improved reporting

---

# 📈 Managed vs Self-Service Deployment

| Feature | Self-Service | Configuration Manager |
|---|---|---|
| Admin Control | Limited | Extensive |
| Update Control | Minimal | Full |
| Reporting | Basic | Advanced |
| Pilot Testing | No | Yes |
| Peer Cache | No | Yes |
| Centralized Settings | No | Yes |
| Enterprise Scale | Limited | Excellent |

---

# 🔥 Key Exam Points

- Configuration Manager is part of Microsoft Endpoint Manager
- Office deployment uses Office 365 Installer Wizard
- Pilot and broad deployment groups recommended
- Peer cache improves bandwidth efficiency
- Semi-Annual Enterprise Channel commonly used for enterprises
- Office Customization Tool integrated into SCCM
- Dashboard monitors deployment health and versions

---

# 🎯 Interview Questions

## Q1: Why use Configuration Manager for Office deployment?
For centralized enterprise deployment and management.

---

## Q2: What is peer cache?
A feature that shares deployment content locally to reduce WAN usage.

---

## Q3: Why use pilot groups?
To test updates before organization-wide deployment.

---

## Q4: What update channel is commonly used in enterprises?
Semi-Annual Enterprise Channel.

---

## Q5: What dashboard monitors Office deployments?
Office Client Management Dashboard.

---

# 📌 Best Practices

- Use pilot deployments first
- Enable peer cache
- Remove old MSI Office versions automatically
- Use 64-bit Office unless compatibility issues exist
- Standardize update channels
- Monitor deployments through dashboards
- Keep SCCM Current Branch updated

---

# 🧩 Summary

Microsoft Configuration Manager enables organizations to:
- Centrally deploy Microsoft 365 Apps
- Manage updates efficiently
- Monitor Office health
- Control deployment channels
- Optimize bandwidth usage

The combination of:
- Pilot deployments
- Peer cache
- Office Customization Tool
- Office Client Management Dashboard

provides enterprise-grade deployment and lifecycle management for Microsoft 365 Apps.

---
