# Configure Microsoft Entra Cloud Sync

## Overview
After completing all Microsoft Entra Cloud Sync prerequisites, organizations must install and configure Microsoft Entra Cloud Sync to synchronize users, groups, and contacts between on-premises Active Directory and Microsoft Entra ID.

The deployment process includes:
- Installing the Microsoft Entra Connect provisioning agent
- Verifying the agent installation
- Verifying the agent services are running
- Configuring Cloud Sync provisioning

---

# Task 1 - Install the Microsoft Entra Connect Provisioning Agent

The provisioning agent is supported only on Windows Server operating systems.

## Installation Steps

### Step 1 - Sign in to Microsoft 365
- Sign in to the Microsoft 365 admin center using a Global Administrator account.

### Step 2 - Open Microsoft Entra Admin Center
- Select Show all
- Under Admin centers, select Identity

### Step 3 - Navigate to Microsoft Entra Connect
- Select Show more
- Select Hybrid management
- Select Microsoft Entra Connect

### Step 4 - Open Cloud Sync
- On the Get started page, select Cloud Sync

### Step 5 - Open Agents Page
- On the Cloud sync | Configurations page
- Under Monitor, select Agents

### Step 6 - Download the Agent
- Select Download on-premises agent
- Select Accept terms & download

### Step 7 - Start Installation
- Open the downloaded installer
- Accept licensing terms
- Select Install

### Step 8 - Configure the Agent
On the wizard:
- Review supported integration scenarios
- Select the appropriate extension
- Sign in using a Global Administrator account

---

# Configure gMSA (If Using HR-Driven Provisioning)

If HR-driven provisioning was selected:

## Options
- Create gMSA automatically
- Use custom gMSA

### Automatic gMSA Creation
- Enter Domain Administrator credentials
- The wizard creates:
  provAgentgMSA$

### Custom gMSA
- Provide existing gMSA details manually

---

# Connect Active Directory

## Steps
- Select Next
- Current domain appears automatically
- Add additional domains if required
- Sign in using administrator credentials for each domain

## Optional Domain Controller Preference
Administrators can:
- Select preferred domain controllers
- Prioritize specific domain controllers

---

# Finalize Installation

## Confirm Configuration
- Review settings
- Select Confirm

## Complete Installation
- Wait for completion message
- Select Exit

---

# Task 2 - Verify the Agent Is Installed

Verification occurs in the Microsoft Entra admin center.

## Steps
- Refresh the Cloud sync | Agents page
- Verify:
  - Agent appears
  - Status shows Active

---

# Task 3 - Verify the Agent Is Running

Verification also occurs locally on the server.

## Steps
1. Sign in to the server
2. Open Services
3. Verify these services are running:
   - Microsoft Azure AD Connect Agent Updater
   - Microsoft Azure AD Connect Provisioning Agent

---

# Task 4 - Configure Microsoft Entra Cloud Sync Provisioning

After installation, configure synchronization settings.

## Steps

### Step 1 - Open Configurations
- On the Cloud sync | Agents page
- Select Configurations

### Step 2 - Create New Configuration
- Select + New configuration
- Choose:
  AD to Microsoft Entra ID sync

### Step 3 - Configure Domain and Password Hash Sync
- Select domain to synchronize
- Choose whether to enable Password Hash Sync
- Select Create

---

# Configure Synchronization Settings

The Edit cloud sync configuration page appears.

## Scope Configuration
Administrators can:
- Synchronize all users
- Use scoping filters for specific users or groups

## Manage Attributes
Administrators can:
- Map attributes between on-premises AD and Microsoft Entra ID
- Modify existing mappings
- Create custom mappings
- Remove unnecessary mappings

## Validation (Recommended)
Use:
- Provision a user

Purpose:
- Test synchronization before deployment
- Validate synchronization for specific users

## Settings
Configure:
- Notification email address
- Prevent accidental deletion
- Accidental deletion threshold

Microsoft recommends:
- Keeping Prevent accidental deletion enabled

## Deploy Configuration
- Move selector to Enable
- Select Save

---

# Key Features of Microsoft Entra Cloud Sync

Microsoft Entra Cloud Sync provides:
- Lightweight synchronization
- Cloud-managed configuration
- Faster synchronization intervals
- Simplified deployment
- High availability support
- Easier maintenance compared to Microsoft Entra Connect Sync

---

# Best Practices

Microsoft recommends organizations:
- Validate synchronization before enabling deployment
- Configure notification email alerts
- Keep accidental deletion protection enabled
- Deploy multiple agents for resiliency
- Monitor synchronization health regularly
- Use scoped deployments during pilot testing

---

# Summary

Microsoft Entra Cloud Sync provides a lightweight and cloud-managed synchronization solution for hybrid identity environments. After installing the provisioning agent, organizations should verify agent functionality, configure synchronization settings, validate provisioning, and carefully deploy synchronization to ensure reliable identity synchronization between on-premises Active Directory and Microsoft Entra ID.
