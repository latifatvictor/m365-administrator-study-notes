# Deploy Microsoft 365 Apps for Enterprise Security Baseline

## Overview

A security baseline is a Microsoft-recommended collection of security configuration settings designed to help organisations deploy secure configurations across devices and applications.

These baselines provide a strong starting point for:

- Security hardening
- Compliance enforcement
- Risk reduction
- Standardised configuration management

Microsoft develops these recommendations using guidance from:

- Microsoft security teams
- Product engineering teams
- Enterprise customers
- Security partners

---

# Products with Security Baselines

Microsoft provides security baselines for:

| Product | Baseline Available |
|---|---|
| Windows 10/11 | Yes |
| Microsoft Defender for Endpoint | Yes |
| Microsoft Edge | Yes |
| Windows 365 | Yes |
| Microsoft 365 Apps for enterprise | Yes |

---

# What Is the Microsoft 365 Apps Security Baseline?

The Microsoft 365 Apps for enterprise security baseline is a predefined collection of security settings for Office applications such as:

- Word
- Excel
- PowerPoint
- Outlook
- Teams
- OneNote

The baseline is deployed using Microsoft Intune.

---

# Purpose of the Security Baseline

The baseline helps organisations:

- Secure Office applications
- Standardise security settings
- Reduce attack surface
- Enforce compliance
- Improve administration efficiency

---

# Why Deploy the Security Baseline?

After deploying Microsoft 365 Apps, organisations should secure them properly.

The security baseline provides:

- Recommended Microsoft security settings
- Centralised policy management
- Consistent configuration
- Improved compliance posture

---

# Key Benefits

---

# 1. Enhanced Security

The security baseline applies best-practice security settings.

Examples include:

- Enforcing MFA
- Restricting risky behaviours
- Hardening Office applications
- Enabling secure access policies

---

## Example

If a user's credentials are compromised:

- MFA helps prevent unauthorised access

---

# 2. Compliance Support

The baseline helps organisations comply with regulations such as:

- GDPR
- HIPAA
- ISO 27001
- Financial regulations

---

## Example

An organisation handling sensitive financial data can enforce:

- Encryption
- Secure authentication
- Controlled access

This helps avoid:

- Data breaches
- Regulatory fines
- Compliance failures

---

# 3. Streamlined Management

Administrators can manage security settings centrally through Intune.

Benefits include:

- Faster configuration
- Easier updates
- Consistent policy deployment
- Reduced administrative overhead

---

## Example

If Microsoft identifies a new Office vulnerability:

- Administrators can quickly update the baseline
- Policies are automatically applied to devices

---

# 4. Better User Experience

Security is integrated into the user workflow without major disruption.

Benefits include:

- Automatic updates
- Seamless security controls
- Reduced downtime
- Improved productivity

---

# How Security Baselines Work

When administrators create a security baseline profile in Intune:

- A template of security settings is created
- The template is assigned to users, groups, or devices
- Devices receive and apply the settings automatically

---

# Security Baseline Assignments

Baselines can be assigned to:

| Assignment Type | Description |
|---|---|
| Device groups | Apply to specific devices |
| User groups | Apply to users regardless of device |
| Individual users | User-specific configuration |
| Excluded groups | Exclude specific users/devices |

---

# Example Deployment Scenario

A healthcare organisation deploys Microsoft 365 Apps to:

- Doctors
- Nurses
- Finance staff

The organisation uses the security baseline to enforce:

- MFA
- Secure Office macros
- Encryption settings
- Compliance policies

Result:

- Better protection of patient data
- Improved compliance with healthcare regulations

---

# Common Security Settings Included

Security baselines may include settings such as:

- Disable unsafe macros
- Enable modern authentication
- Enforce MFA
- Restrict legacy authentication
- Secure ActiveX controls
- Configure trusted locations
- Apply DLP-related controls
- Block risky behaviours

---

# Microsoft Intune and Security Baselines

Microsoft Intune enables organisations to:

- Deploy baselines
- Monitor compliance
- Manage updates
- Report on security posture

All from a single cloud-based management portal.

---

# Step-by-Step: Deploy Microsoft 365 Apps Security Baseline

---

# Step 1: Open Microsoft Intune Admin Center

## Navigation

1. Sign into Microsoft 365 admin center
2. Select **Show all**
3. Under Admin centers select:
   - Endpoint Manager

This opens the Microsoft Intune admin center.

---

# Step 2: Open Endpoint Security

In Intune:

- Select **Endpoint security**

---

# Step 3: Open Security Baselines

On the Endpoint security page:

- Select **Security baselines**

---

# Step 4: Select Microsoft 365 Apps Baseline

Choose:

- Microsoft 365 Apps for Enterprise Security Baseline

---

# Step 5: Create Profile

Select:

- **+ Create profile**

Then select:

- **Create**

This launches the Create profile wizard.

---

# Step 6: Configure Basics

Enter:

| Field | Purpose |
|---|---|
| Name | Profile name |
| Description | Baseline description |

Then select:

- Next

---

# Step 7: Configure Security Settings

Review Microsoft recommended settings.

Adjust settings if required based on:

- Business requirements
- Security policies
- Compliance needs

Then select:

- Next

---

# Step 8: Configure Scope Tags

Optionally assign:

- Scope tags

Scope tags help separate administrative responsibilities.

Then select:

- Next

---

# Step 9: Configure Assignments

Assign the baseline to:

- Users
- Groups
- Devices

Optional:

- Exclude groups

Then select:

- Next

---

# Step 10: Review and Create

Review configuration settings.

Select:

- Create

The baseline is deployed.

---

# Important Deployment Considerations

---

# Pilot First

Always deploy to a pilot group before broad deployment.

This helps identify:

- Compatibility issues
- User impact
- Application conflicts

---

# Review Security Settings Carefully

Some settings may:

- Restrict macros
- Block legacy workflows
- Affect older applications

Always test thoroughly.

---

# Keep Baselines Updated

Microsoft periodically updates baselines to address:

- New vulnerabilities
- Threat landscape changes
- Best practices

---

# Common Challenges

| Challenge | Cause |
|---|---|
| Legacy app issues | Strict security settings |
| Macro failures | Macro blocking policies |
| User complaints | Restrictive configurations |
| Compliance gaps | Incomplete assignments |

---

# Best Practices

- Deploy to pilot groups first
- Review all settings before deployment
- Use exclusions when necessary
- Monitor compliance regularly
- Align settings with business requirements
- Train users on security changes

---

# Real Enterprise Example

A finance company deploys Microsoft 365 Apps to 5,000 users.

They apply the security baseline to:

- Disable risky macros
- Enforce MFA
- Harden Office security
- Enable secure authentication

Results:

- Reduced phishing attacks
- Improved compliance
- Faster incident response
- Standardised Office security

---

# Monitoring and Reporting

Administrators can monitor:

- Compliance status
- Failed policy deployments
- Device security posture
- Baseline assignment success

Using:

- Microsoft Intune reports
- Endpoint security dashboards

---

# Security Baseline vs Configuration Profile

| Security Baseline | Configuration Profile |
|---|---|
| Microsoft recommended settings | Fully custom settings |
| Faster deployment | Greater flexibility |
| Best-practice starting point | Granular customisation |

---

# Interview Questions

## Q1: What is a security baseline?

A Microsoft-recommended collection of security settings designed to improve security posture.

---

## Q2: What tool is used to deploy Microsoft 365 Apps security baselines?

Microsoft Intune.

---

## Q3: Why are security baselines important?

They help standardise and secure configurations across devices and applications.

---

## Q4: Can security baselines be assigned to groups?

Yes.

They can be assigned to:

- Users
- Groups
- Devices

---

## Q5: Why should organisations pilot security baselines first?

To identify compatibility and business workflow issues before large-scale deployment.

---

## Q6: What are scope tags in Intune?

Scope tags help control administrative visibility and responsibilities.

---

# Key Exam Points

- Security baselines are Microsoft recommended settings
- Intune deploys Microsoft 365 Apps security baselines
- Baselines improve security and compliance
- Baselines can be assigned to users, groups, or devices
- Pilot testing is essential
- Security baselines centralise configuration management
- MFA and DLP can be enforced through baseline settings

---

# Summary

Deploying the Microsoft 365 Apps for enterprise security baseline using Microsoft Intune helps organisations:

- Improve security
- Reduce vulnerabilities
- Standardise configurations
- Maintain compliance
- Simplify management

The security baseline acts as a strong starting point that organisations can customise based on their operational and compliance requirements.

Using Microsoft Intune allows administrators to centrally deploy, monitor, and maintain these security settings across all managed devices and users.
