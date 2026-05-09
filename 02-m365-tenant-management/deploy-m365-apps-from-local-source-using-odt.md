# Deploy Microsoft 365 Apps for Enterprise from a Local Source

## Overview

Microsoft 365 Apps for enterprise can be deployed from a local network source using the Office Deployment Tool (ODT).

In this method, the Office installation files are first downloaded to a shared folder on the local network, then deployed to users from that local source.

This approach is useful when organisations want to:

- Reduce internet bandwidth usage
- Improve installation speed for local users
- Support branch office deployments
- Maintain more control over Office installation files
- Use local file shares or DFS replication

---

## Key Tools Used

- Office Deployment Tool (ODT)
- Office Customization Tool (OCT)
- Local shared folders
- XML configuration files
- Scripts or deployment tools for automation

---

## Local Source vs Cloud Deployment

| Cloud Deployment | Local Source Deployment |
|---|---|
| Office files download from Microsoft CDN | Office files download from local network share |
| Fewer steps | More setup required |
| Depends heavily on internet bandwidth | Reduces internet bandwidth usage |
| Easier for smaller environments | Better for controlled or distributed environments |

---

## Folder Structure

Create one parent folder and two child folders.

Recommended structure:

- `\\Server\Share\M365`
- `\\Server\Share\M365\SECP`
- `\\Server\Share\M365\SEC`

Purpose:

| Folder | Purpose |
|---|---|
| `M365` | Stores ODT and configuration files |
| `SECP` | Stores Semi-Annual Enterprise Channel Preview files |
| `SEC` | Stores Semi-Annual Enterprise Channel files |

---

## Permissions

Users need:

- Read permission to the shared folder
- Local admin rights if installing manually

In managed deployments, scripts can be run with elevated permissions.

---

## Branch Office Consideration

For remote offices, organisations can create local copies of the Office source files.

Possible method:

- Use Distributed File System (DFS)
- Replicate Office files to branch offices
- Allow users to install from nearby local source

This helps reduce WAN bandwidth usage.

---

## Recommended Deployment Model

Use two deployment groups:

| Group | Update Channel | Purpose |
|---|---|---|
| Pilot Group | Semi-Annual Enterprise Channel (Preview) | Testing |
| Broad Group | Semi-Annual Enterprise Channel | Production |

---

## Step 1: Create Shared Folders

Create:

- `\\Server\Share\M365`
- `\\Server\Share\M365\SECP`
- `\\Server\Share\M365\SEC`

Assign read permissions to users.

---

## Step 2: Download Office Deployment Tool

Download the latest Office Deployment Tool from Microsoft.

ODT includes:

- `setup.exe`
- sample `configuration.xml`

Save these files in:

`\\Server\Share\M365`

---

## Step 3: Create Pilot Configuration File

Use the Office Customization Tool to create the pilot XML configuration.

Recommended pilot settings:

- Product: Microsoft 365 Apps for enterprise
- Update channel: Semi-Annual Enterprise Channel (Preview)
- Installation source: Local source
- Source path: `\\Server\Share\M365\SECP`
- Language: Match operating system
- Fallback language source: CDN
- Updates: Automatically from CDN
- Remove previous MSI Office versions: Yes
- Display level: Off
- Accept EULA: On

Save as:

`config-pilot-SECP.xml`

---

## Step 4: Create Broad Configuration File

Use the same settings as the pilot configuration, except:

- Update channel: Semi-Annual Enterprise Channel
- Source path: `\\Server\Share\M365\SEC`

Save as:

`config-broad-SEC.xml`

---

## Step 5: Download Pilot Office Installation Files

Use ODT in download mode with the pilot configuration file.

This downloads the Semi-Annual Enterprise Channel Preview installation files to:

`\\Server\Share\M365\SECP`

This can be automated using scripts.

---

## Step 6: Download Broad Office Installation Files

Use ODT in download mode with the broad configuration file.

This downloads the Semi-Annual Enterprise Channel installation files to:

`\\Server\Share\M365\SEC`

This can also be automated using scripts.

---

## Step 7: Deploy Office to Pilot Group

Use ODT in configure mode with the pilot configuration file.

Purpose:

- Test installation
- Validate application compatibility
- Confirm drivers and hardware work correctly
- Check business add-ins
- Confirm update behaviour

This can be done manually, by script, or with a deployment platform.

---

## Step 8: Deploy Office to Broad Group

After successful pilot testing, deploy the broad configuration to production users.

Purpose:

- Stable rollout
- Wider organisation deployment
- Controlled update channel

---

## What Happens During Local Source Deployment

ODT will:

- Use the local shared folder as the installation source
- Install Microsoft 365 Apps
- Apply XML configuration settings
- Remove old MSI Office versions if configured
- Configure update channel
- Apply Office preferences

---

## Updates

Even though installation files come from a local source, updates can still be configured to come from:

- Office CDN
- Local source
- Managed deployment tools

In this Microsoft Learn scenario, updates are configured to come automatically from the CDN.

---

## Troubleshooting

Check:

- Latest ODT version is being used
- XML configuration file is valid
- Source path is correct
- Files exist in the correct folders
- Users have read permission to the share
- Devices have local admin rights if installing manually
- Internet access is available for activation
- Logs are reviewed in `%temp%`

---

## Real Work Scenario

A company has a head office and several branch offices.

Challenge:

- Internet bandwidth is limited at branches
- Many users need Microsoft 365 Apps installed

Solution:

- Download Office files once
- Store them on local network shares
- Replicate files to branch offices using DFS
- Deploy Office from the nearest local source

Benefits:

- Reduced internet bandwidth usage
- Faster installations
- More controlled deployment
- Better branch office experience

---

## Local Source Deployment Benefits

- Reduces internet bandwidth usage
- Improves installation performance
- Supports controlled rollout
- Useful for remote or branch offices
- Allows reuse of downloaded Office files
- Works well with scripts or deployment tools

---

## Local Source Deployment Challenges

- More setup required
- Admins must manage source files
- Local folders must be maintained
- Permissions must be configured correctly
- Requires planning for updates and versions

---

## Common Mistakes

- Wrong source path in XML file
- Not downloading files before deployment
- Users lacking read access to share
- Using outdated Office Deployment Tool
- Skipping pilot deployment
- Not testing Office add-ins
- Forgetting local admin requirement for manual install

---

## Best Practices

- Use pilot group before broad rollout
- Use 64-bit Office unless 32-bit is required
- Keep ODT updated
- Use clear folder structure
- Use DFS for branch offices
- Remove previous MSI Office versions
- Use silent installation
- Document XML configuration files
- Review installation logs when troubleshooting

---

## Interview Questions

### Q1: What is local source deployment?

Deploying Microsoft 365 Apps from Office files stored on a local network share.

---

### Q2: What tool is used?

Office Deployment Tool (ODT).

---

### Q3: Why deploy from a local source?

To reduce internet bandwidth usage and improve deployment control.

---

### Q4: What is the difference between cloud and local deployment?

Cloud deployment downloads from Microsoft CDN. Local deployment installs from a local network share.

---

### Q5: What folder stores the pilot Office files?

The folder for Semi-Annual Enterprise Channel Preview, for example `\\Server\Share\M365\SECP`.

---

### Q6: What must users have to install manually?

Local administrator rights and read access to the share.

---

### Q7: What should you do before broad deployment?

Test with a pilot group.

---

## Key Exam Points

- Local source deployment uses ODT
- Office files must be downloaded first
- Local shared folders store installation files
- Pilot and broad groups are recommended
- XML configuration files define deployment settings
- Users need read access to the share
- Local deployment helps reduce internet bandwidth usage
- DFS can help distribute Office files to branch offices
- Logs can be checked in `%temp%`

---

## Summary

Deploying Microsoft 365 Apps for enterprise from a local source gives organisations more control over installation files and helps reduce internet bandwidth usage.

It is especially useful for:

- Large organisations
- Branch offices
- Limited bandwidth environments
- Controlled enterprise deployments

The main process is:

1. Create shared folders
2. Download ODT
3. Create XML configuration files
4. Download Office files locally
5. Deploy to pilot group
6. Deploy to broad group

This deployment method is best when organisations want predictable, controlled, and network-efficient Office installations.
