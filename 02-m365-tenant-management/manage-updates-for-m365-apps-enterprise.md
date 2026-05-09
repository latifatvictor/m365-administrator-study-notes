# Manage Updates for Microsoft 365 Apps for Enterprise

## Overview

Microsoft 365 Apps for enterprise uses Click-to-Run technology for installations and updates.

Unlike traditional MSI-based Office deployments, Click-to-Run provides:

- Faster updates
- Smaller downloads
- Background installations
- Delta updates
- Simplified patching
- Automatic update management

Microsoft releases updated Office builds monthly on:

- Patch Tuesday
- Second Tuesday of every month

---

## Click-to-Run Update Model

Click-to-Run uses an optimized update process.

Instead of downloading full Office packages every time:

- The client compares the installed version with the new version
- Only changed files (deltas) are downloaded
- This reduces bandwidth usage
- Updates are smaller and faster

---

## Benefits of Click-to-Run Updates

- Silent background updates
- Reduced network bandwidth usage
- Faster deployment
- Minimal user disruption
- No separate service packs
- No separate security updates
- No cumulative update packages
- Automatic update management

---

## User Experience During Updates

Updates happen silently in the background.

If users are actively using Office applications:

- Updates continue in the background
- Office apps are not interrupted
- New version activates after app restart

Example:

- User works in Word
- Update installs silently
- User closes Word
- Next launch uses updated version

---

## Update Options

Microsoft 365 Apps supports three major update methods.

---

# 1. Automatic Updates from the Cloud

## Overview

Default update method.

Office automatically downloads updates directly from Microsoft CDN.

---

## Characteristics

- Automatic
- Cloud-based
- No admin infrastructure required
- Best for:
  - Home users
  - Small businesses
  - Simple deployments

---

## Process

- Daily scheduled task checks for updates
- Client connects to Microsoft CDN
- Downloads delta changes only
- Installs updates silently

---

## Benefits

- Minimal management
- Always updated
- Simplest deployment method

---

## Drawbacks

- Less control
- Internet bandwidth usage
- Limited scheduling control

---

# 2. Automatic Updates from Network Share

## Overview

Office updates come from an internal network source instead of Microsoft CDN.

Administrators define:

- Shared folder
- Local update source
- Update timing

---

## Characteristics

- Managed deployment
- Controlled updates
- Internal file share
- Common in medium-sized organisations

---

## Benefits

- Reduces internet bandwidth
- Greater update control
- Centralised management

---

## Drawbacks

- Requires local infrastructure
- Requires maintaining update source

---

# 3. Electronic Software Distribution (ESD)

## Overview

Large organisations often use deployment platforms like:

- Microsoft Configuration Manager
- Microsoft Endpoint Manager
- Other ESD tools

---

## Characteristics

- Highly controlled deployments
- Scheduled updates
- Phased rollouts
- Enterprise-level management

---

## Benefits

- Fine-grained control
- Staged deployments
- Pilot testing support
- Enterprise reporting
- Controlled bandwidth usage

---

## Drawbacks

- More complex
- Requires infrastructure
- Requires deployment expertise

---

## Pilot and Production Update Strategy

Best practice:

1. Download updates to test share
2. Deploy to pilot users first
3. Test compatibility
4. Move updates to production share
5. Deploy broadly after validation

---

## Why Pilot Testing Matters

Pilot testing helps detect:

- Application compatibility issues
- Add-in failures
- Driver problems
- Business process interruptions
- Performance issues

---

## Office Deployment Tool and Updates

Administrators can manage updates using:

- Office Deployment Tool (ODT)
- XML configuration files
- Group Policy
- Deployment tools

Scripts can also be run to automate update management.

---

## XML Configuration Settings

ODT uses configuration.xml to manage update behaviour.

Common settings include:

| Setting | Purpose |
|---|---|
| Enabled | Turns updates on/off |
| UpdatePath | Defines update source |
| TargetVersion | Specifies Office version |

---

## Enabled Attribute

Controls whether updates are enabled.

| Value | Meaning |
|---|---|
| TRUE | Updates enabled |
| FALSE | Updates disabled |

Default:
- TRUE

---

## UpdatePath Attribute

Defines update source location.

Possible locations:

- Local file share
- Network path
- HTTP path
- Microsoft CDN

Example:
- `\\Server\Share\Office`

---

## TargetVersion Attribute

Forces Office to update to a specific version.

Example:
- `16.0.6366.2036`

Useful for:
- Controlled rollouts
- Compatibility testing
- Standardisation

---

## Microsoft Support Lifecycle Warning

Microsoft only supports Office builds for:

- 12 months

If clients remain outdated longer than 12 months:

- They fall out of support
- Must upgrade to supported version

---

## Common Enterprise Update Approaches

| Organisation Size | Typical Update Method |
|---|---|
| Small Business | Automatic from cloud |
| Medium Business | Network share |
| Large Enterprise | Configuration Manager / ESD |

---

## Real Work Scenario

A company has 5,000 users across multiple countries.

Challenge:

- Reduce bandwidth usage
- Prevent unstable updates reaching production
- Maintain version control

Solution:

- Download Office updates to internal share
- Test with pilot group
- Use Configuration Manager to stage rollout
- Deploy gradually to production users

Benefits:

- Better control
- Reduced risk
- Lower bandwidth usage
- Improved user experience

---

## Common Mistakes

- Disabling updates completely
- Skipping pilot testing
- Keeping unsupported Office versions
- Using outdated deployment tools
- Not monitoring update failures
- Not documenting update channels

---

## Best Practices

- Always use pilot groups
- Keep Office within support lifecycle
- Use Semi-Annual Enterprise Channel for stability
- Use Configuration Manager for large environments
- Monitor update compliance
- Document update policies
- Test business-critical add-ins before deployment
- Keep ODT updated

---

## Troubleshooting Tips

Check:

- XML configuration syntax
- Network share permissions
- Office version compatibility
- CDN connectivity
- Update channel settings
- Client logs
- Group Policy conflicts

Logs may be reviewed in:

`%temp%`

---

## Interview Questions

### Q1: What technology does Microsoft 365 Apps use for updates?

Click-to-Run technology.

---

### Q2: What are delta updates?

Only changed files are downloaded instead of the full Office package.

---

### Q3: When are Office updates typically released?

Patch Tuesday (second Tuesday of each month).

---

### Q4: What are the three main update methods?

- Automatic from cloud
- Automatic from network share
- Electronic Software Distribution (ESD)

---

### Q5: What is the purpose of UpdatePath?

Defines where Office updates are downloaded from.

---

### Q6: Why use pilot update groups?

To test updates before broad deployment.

---

### Q7: What happens if Office apps are open during updates?

Updates install silently and activate after the apps restart.

---

## Key Exam Points

- Microsoft 365 Apps uses Click-to-Run
- Updates use delta downloads
- Patch Tuesday releases monthly builds
- Updates install silently in background
- ODT XML can manage updates
- UpdatePath defines update source
- TargetVersion specifies Office build
- Clients unsupported after 12 months without updates
- Pilot testing is best practice

---

## Summary

Managing updates for Microsoft 365 Apps for enterprise is critical for:

- Security
- Stability
- Compatibility
- Performance
- Compliance

Microsoft 365 Apps uses Click-to-Run technology to:

- Simplify updates
- Reduce bandwidth usage
- Improve user experience
- Deliver silent background updates

Organisations can manage updates using:

- Microsoft CDN
- Internal file shares
- Configuration Manager
- Deployment tools
- XML configuration files

The best enterprise strategy is:

- Pilot first
- Test carefully
- Deploy gradually
- Keep builds supported
