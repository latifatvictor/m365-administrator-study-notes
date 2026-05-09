# Add Microsoft 365 Apps for Enterprise to Microsoft Intune

## Overview

Microsoft Intune enables organisations to:

- Deploy applications
- Configure applications
- Protect organisational data
- Control app access
- Monitor application health
- Automate updates

Microsoft 365 Apps for enterprise can be centrally deployed and managed using Intune across Windows, macOS, iOS/iPadOS, and Android devices.

---

# What Are Intune Apps?

Intune apps are applications managed through Microsoft Intune.

Administrators can:

- Deploy apps
- Configure settings
- Apply protection policies
- Control access
- Monitor usage
- Enforce compliance

---

# Benefits of Managing Apps with Intune

| Benefit | Description |
|---|---|
| Centralised management | Manage apps from one portal |
| Security and compliance | Enforce policies and updates |
| Scalability | Suitable for small and large organisations |
| Improved user experience | Consistent app deployment |
| Data protection | Protect organisational data |
| Access control | Restrict app access |
| App configuration | Configure apps centrally |
| Automatic updates | Keep apps secure and updated |

---

# Common Scenarios for Using Intune Apps

Organisations commonly use Intune when they need to:

- Deploy Microsoft 365 Apps
- Protect sensitive company data
- Configure applications with company settings
- Enforce app security policies
- Monitor app compliance
- Control access to corporate apps

---

# App Types in Microsoft Intune

Intune supports multiple application types.

---

# Main Intune App Categories

| App Type | Installation Method | Update Method |
|---|---|---|
| Store apps | Installed by Intune | Automatic |
| Line-of-business (LOB) apps | Installed using installation file | Manual updates required |
| Built-in apps | Installed by Intune | Automatic |
| Web apps | Shortcut created | Automatic |
| Apps from Microsoft services | Shortcut in Company Portal | Automatic |

---

# Store Apps

## Overview

Applications downloaded directly from app stores.

Examples:

- Microsoft Store apps
- Apple App Store apps
- Google Play apps

---

## Benefits

- Easy deployment
- Automatic updates
- Minimal packaging effort

---

# Line-of-Business (LOB) Apps

## Overview

Custom or internally developed applications.

These require installation packages such as:

- `.msi`
- `.apk`
- `.ipa`
- `.pkg`
- `.intunewin`

---

## Benefits

- Supports custom enterprise applications
- Enables internal business app deployment

---

## Drawbacks

- Manual updates required
- Packaging complexity

---

# Built-In Apps

## Overview

Native operating system applications.

Examples:

- Safari
- Calculator
- Native Android apps

---

# Web Apps

## Overview

Web applications deployed as shortcuts.

Examples:

- Internal company portals
- SaaS applications
- Web-based tools

---

# Microsoft 365 Apps for Windows 10/11

## Overview

One of the most common deployments in Intune.

Allows organisations to deploy:

- Word
- Excel
- PowerPoint
- Outlook
- Teams
- OneNote
- Access
- Publisher

Additionally:

- Visio
- Project

(if licensed)

---

# Important Deployment Considerations

## Devices Must Run

- Windows 10 Creators Update or later
- Windows 11 supported

---

## Supported Office Installations

Only Microsoft 365 Apps are supported.

---

## Existing MSI Office Installations

Existing MSI-based Office installations must be removed.

Failure to remove them can cause:

- Installation failures
- Application conflicts
- Deployment issues

---

## Multiple Office Deployments

Not supported.

Only one deployment can exist on a device.

---

## Architecture Selection

Choose:

- 32-bit Office
- 64-bit Office

---

## Open Office Applications

If Office apps are open during deployment:

- Installation may fail
- Unsaved work may be lost

---

# Important Autopilot Consideration

When deploying Office during Autopilot ESP:

Microsoft recommends deploying Office as a:

- Win32 app

Reason:

- Prevent installation concurrency issues
- Avoid Enrollment Status Page failures

---

# Supported App Types in Intune

## Examples

| Platform | App Type |
|---|---|
| Android Store App | Google Play |
| iOS Store App | Apple App Store |
| Microsoft Store App | Microsoft Store |
| Win32 App | `.intunewin` |
| Windows LOB App | `.msi`, `.appx`, `.msix` |
| macOS App | `.pkg`, `.dmg` |
| Web Link | URL shortcut |

---

# Real Work Scenario

A company wants to deploy Microsoft 365 Apps to 2,000 remote users.

Using Intune allows them to:

- Automatically install Office
- Standardise configurations
- Remove old MSI Office versions
- Apply security policies
- Ensure users stay updated

Result:

- Simplified deployment
- Improved security
- Reduced manual support

---

# Step-by-Step: Add Microsoft 365 Apps to Intune

---

# Step 1: Open Microsoft Intune Admin Center

## Navigation

1. Sign into Microsoft 365 admin center
2. Select **Show all**
3. Select **Endpoint Manager**
4. Open Microsoft Intune admin center

---

# Step 2: Navigate to Apps

In Intune:

- Select **Apps**

---

# Step 3: Add Application

Choose either:

- All apps
- By platform

Then select:

- **+ Add**

---

# Step 4: Select App Type

Choose:

- Windows 10 and later
- Microsoft 365 Apps

Then select:

- **Select**

This launches the Add Microsoft 365 Apps wizard.

---

# Step 5: Configure App Suite Information

## Common Fields

| Setting | Purpose |
|---|---|
| Suite Name | Application name |
| Description | App description |
| Publisher | Microsoft |
| Category | Company Portal categorisation |
| Featured App | Display prominently |

---

# Step 6: Configure App Suite

## Architecture

Choose:

- 32-bit
- 64-bit

---

## Default File Format

Options:

- Office Open XML
- Open Document Format

Microsoft generally recommends:

- Office Open XML

---

## Update Channel

Choose:

- Current Channel
- Monthly Enterprise Channel
- Semi-Annual Enterprise Channel
- Semi-Annual Enterprise Channel (Preview)

---

## Languages

Choose required languages.

---

## Remove MSI

Enable removal of existing MSI Office versions.

---

# Step 7: Configure Assignments

Assign the application to:

- Users
- Groups
- Devices

---

# Step 8: Review and Create

Review settings.

Select:

- Create

Deployment begins.

---

# Microsoft 365 Update Channel Recommendations

| Channel | Best Use Case |
|---|---|
| Current Channel | Fastest features |
| Monthly Enterprise | Predictable monthly updates |
| Semi-Annual Enterprise | Stable enterprise deployments |

---

# Security Benefits of Intune App Management

- Controlled deployments
- Patch management
- App protection policies
- Compliance enforcement
- Conditional access integration
- Secure remote work support

---

# Common Intune Deployment Challenges

| Challenge | Cause |
|---|---|
| Office install failure | Existing MSI Office |
| ESP failures | Concurrent installations |
| App conflicts | Multiple Office deployments |
| User disruption | Apps open during install |
| Architecture mismatch | Incorrect Office bitness |

---

# Best Practices

- Remove MSI Office versions
- Use pilot deployment groups
- Test before broad deployment
- Use appropriate update channels
- Monitor installation status
- Use Win32 packaging during Autopilot
- Assign apps carefully

---

# Common Mistakes

- Deploying multiple Office suites
- Ignoring MSI removal
- Using wrong architecture
- Deploying during active user sessions
- Skipping pilot testing

---

# Interview Questions

## Q1: What is Microsoft Intune used for?

Managing devices, applications, security, and compliance.

---

## Q2: What are Intune apps?

Applications managed through Microsoft Intune.

---

## Q3: What happens if MSI Office versions are not removed?

Microsoft 365 Apps installation may fail.

---

## Q4: What app type is recommended during Autopilot ESP?

Win32 app.

---

## Q5: Which update channels are available for Microsoft 365 Apps?

- Current Channel
- Monthly Enterprise Channel
- Semi-Annual Enterprise Channel
- Semi-Annual Enterprise Channel Preview

---

## Q6: What file extension is used for Win32 apps?

`.intunewin`

---

## Q7: Can multiple Microsoft 365 deployments exist on one device?

No.

---

# Key Exam Points

- Intune manages apps, devices, and security
- Microsoft 365 Apps can be deployed through Intune
- Existing MSI Office apps should be removed
- Win32 apps are recommended during Autopilot
- Multiple Office deployments are unsupported
- Intune supports store, LOB, built-in, and web apps
- Office update channels can be configured during deployment

---

# Summary

Microsoft Intune provides a modern cloud-based platform for managing Microsoft 365 Apps deployments.

Benefits include:

- Centralised management
- Improved security
- Simplified deployment
- Better compliance
- Automated updates

Key deployment considerations include:

- Removing MSI Office versions
- Choosing correct architecture
- Selecting appropriate update channels
- Using pilot groups
- Monitoring deployments

Intune enables organisations to securely deploy and manage Microsoft 365 Apps at enterprise scale.
