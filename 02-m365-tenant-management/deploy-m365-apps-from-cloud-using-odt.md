# Deploy Microsoft 365 Apps for Enterprise from the Cloud

## Overview

Organizations can deploy Microsoft 365 Apps for enterprise from the cloud using:

- Office Content Delivery Network (CDN)
- Office Deployment Tool (ODT)
- Office Customization Tool (OCT)

This method gives administrators more control than self-service installation while still using Microsoft’s cloud infrastructure for installation files and updates.

---

## Office Content Delivery Network (CDN)

The Office CDN is Microsoft’s global delivery network.

It helps to:

- Deliver Office installation files
- Deliver Office updates
- Improve download performance
- Reduce latency
- Provide content from locations close to users

---

## Public vs Private CDN

| CDN Type | Use Case | Access |
|---|---|---|
| Public CDN | JavaScript, CSS, fonts, logos, generic images | Anonymous/public |
| Private CDN | SharePoint Online content, internal images, proprietary files | Permission-based |

---

## Office Deployment Tool (ODT)

The Office Deployment Tool is a command-line tool used to deploy and manage Microsoft 365 Apps.

ODT can:

- Download Office source files
- Install Microsoft 365 Apps
- Remove Office versions
- Configure update channels
- Deploy language packs
- Apply installation settings

Scripts can be run with ODT to automate deployment.

---

## Requirements

Users/devices need:

- Internet access
- Access to Microsoft CDN endpoints
- Local admin rights unless deployment is run through an elevated tool
- Read access to the deployment share
- Latest Office Deployment Tool

---

## Recommended Deployment Model

Use two groups:

| Group | Update Channel | Purpose |
|---|---|---|
| Pilot Group | Semi-Annual Enterprise Channel (Preview) | Test first |
| Broad Group | Semi-Annual Enterprise Channel | Production rollout |

---

## Recommended Packages

Create two installation packages:

- 64-bit Semi-Annual Enterprise Channel (Preview)
- 64-bit Semi-Annual Enterprise Channel

Optional:

- 32-bit package if legacy app compatibility requires it
- Visio and Project if licensed

---

## Deployment Steps

### Step 1: Create Deployment Share

Create a shared folder such as:

`\\Server\Share\M365`

Give users read access.

---

### Step 2: Download ODT

Download the Office Deployment Tool from Microsoft.

ODT includes:

- `setup.exe`
- Sample `configuration.xml`

---

### Step 3: Create Pilot Configuration

Use the Office Customization Tool to create the pilot XML configuration.

Recommended pilot settings:

- Product: Microsoft 365 Apps for enterprise
- Update channel: Semi-Annual Enterprise Channel (Preview)
- Architecture: 64-bit
- Language: Match operating system
- Fallback language source: CDN
- Installation source: Office CDN
- Updates: Automatically from CDN
- Remove previous MSI versions: Yes
- Display level: Off
- Accept EULA: On

Save as:

`config-pilot-SECP.xml`

---

### Step 4: Create Broad Configuration

Use the same settings as the pilot configuration, except:

- Update channel: Semi-Annual Enterprise Channel

Save as:

`config-broad-SEC.xml`

---

### Step 5: Deploy to Pilot Group

Deploy using ODT and the pilot configuration file.

This can be run manually, by script, or through an elevated deployment tool.

Purpose of pilot deployment:

- Test Office installation
- Check app compatibility
- Validate hardware and drivers
- Confirm update behaviour

---

### Step 6: Deploy to Broad Group

After pilot testing succeeds, deploy the broad configuration to production users.

Purpose of broad deployment:

- Stable production rollout
- Controlled update channel
- Wider organisation deployment

---

## What Happens During Deployment

ODT will:

- Download Office files from CDN
- Install Microsoft 365 Apps
- Apply configuration settings
- Remove older MSI Office versions if configured
- Configure update channel
- Enable automatic updates

---

## Troubleshooting

Check:

- ODT is the latest version
- XML configuration is valid
- File paths are correct
- Users/devices have permissions
- Devices can reach CDN endpoints
- Internet access is available

Log files can be reviewed in:

`%temp%`

---

## Real Work Scenario

A company wants to deploy Microsoft 365 Apps to 4,000 users.

Approach:

- Create pilot group for IT and business testers
- Use Semi-Annual Enterprise Channel (Preview)
- Validate compatibility
- Deploy stable Semi-Annual Enterprise Channel to all users
- Use scripts or deployment tools to automate rollout

Benefits:

- Controlled deployment
- Reduced risk
- Better compatibility testing
- Centralised configuration
- Less infrastructure than full Configuration Manager deployment

---

## ODT Cloud Deployment vs Configuration Manager

| Feature | ODT Cloud Deployment | Configuration Manager |
|---|---|---|
| Infrastructure required | Low | High |
| Control level | Medium | High |
| Reporting | Limited | Advanced |
| Uses cloud CDN | Yes | Optional |
| Best for | Small to medium deployments | Large enterprises |
| Automation | Script-based | Built-in deployment management |

---

## Best Practices

- Use pilot deployment first
- Use 64-bit Office unless legacy compatibility requires 32-bit
- Remove old MSI Office versions during deployment
- Use silent installation for users
- Match operating system language
- Keep ODT updated
- Use CDN fallback for language packs
- Document configuration files
- Test before broad rollout

---

## Common Mistakes

- Skipping pilot testing
- Using wrong update channel
- Not removing old Office versions
- Invalid XML configuration
- Users lacking admin rights
- Devices blocked from Microsoft CDN
- Not checking installation logs

---

## Interview Questions

### Q1: What is the Office Deployment Tool?

A command-line tool used to deploy and configure Microsoft 365 Apps installations.

---

### Q2: What is the Office CDN?

Microsoft’s global content delivery network for Office installation files and updates.

---

### Q3: Why use a pilot group?

To test deployment and updates before rolling out to the wider organisation.

---

### Q4: What file format does ODT use?

XML configuration files.

---

### Q5: What is Click-to-Run?

Microsoft’s streaming installation technology for Office applications.

---

### Q6: Why use Semi-Annual Enterprise Channel?

It provides a more stable update cadence for enterprise environments.

---

## Key Exam Points

- Microsoft 365 Apps can be deployed from the cloud using ODT
- ODT uses XML configuration files
- Office files come from the Office CDN
- Pilot and broad deployment groups are recommended
- Semi-Annual Enterprise Channel is common for enterprises
- ODT supports silent installation
- ODT can remove previous MSI Office versions
- Users need local admin rights unless deployment is elevated through IT tools

---

## Summary

Deploying Microsoft 365 Apps for enterprise from the cloud using ODT and Office CDN provides a flexible, scalable deployment option.

It is useful when organisations want:

- More control than self-service installation
- Less infrastructure than Configuration Manager
- Cloud-based installation files
- Standardised deployment settings
- Pilot and broad rollout strategy
