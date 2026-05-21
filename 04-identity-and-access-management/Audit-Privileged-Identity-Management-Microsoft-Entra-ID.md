# Audit Privileged Identity Management (PIM)

## Overview

Microsoft Entra Privileged Identity Management (PIM) enables organizations to:
- Audit privileged access
- Monitor activations
- Track administrator activities
- Review audit history
- Export role assignments for compliance purposes

PIM auditing applies to Azure resources including:
- Subscriptions
- Resource groups
- Virtual machines
- Other Azure RBAC-enabled resources

---

# Important Note

If an organization uses:
- Azure delegated resource management
- External service providers

then:
- PIM does NOT display role assignments authorized by the service provider.

---

# PIM Auditing Capabilities

PIM provides visibility into:
- User activities
- Role activations
- Audit history
- Resource activity
- Assignment exports
- Compliance reporting

---

# View Activity and Activations

Administrators can:
- Monitor actions performed by users
- Review role activations
- Analyze resource activity

This helps organizations:
- Detect suspicious actions
- Verify privileged usage
- Improve accountability

---

# Steps to View Activity and Activations

## Step 1

In Microsoft Entra admin center:
- Select Identity governance
- Select Privileged Identity Management

---

## Step 2

On the Quick start page:
- Under Manage
- Select Azure resources

---

## Step 3

Select:
- The resource you want to monitor

Examples:
- Subscription
- Resource group
- Virtual machine

---

## Step 4

Select:
- Roles
OR
- Members

---

## Step 5

Select a user to view:
- Resource activity summary
- Role activation history
- Activity timelines

---

# User Activity Information

PIM displays:
- User actions
- Date of actions
- Activated roles
- Resource activity during activation

---

# View Specific Role Activation Details

Administrators can:
- Select a specific activation

PIM then displays:
- Detailed role activation information
- Corresponding Azure resource activity

---

# Navigate to Audit History

Audit history enables organizations to:
- Review privileged activity
- Track activations
- Monitor administrative changes
- Investigate security incidents

---

# Steps to Access Audit History

## Step 1

From Microsoft Entra dashboard:
- Open Privileged Identity Management app

---

## Step 2

Select:
- Manage privileged roles
- Audit history

---

# Resource Audit

Resource audit provides:
- Complete role activity history for a resource

---

# Steps to Access Resource Audit

## Step 1

In Microsoft Entra admin center:
- Select Identity governance
- Select Privileged Identity Management

---

## Step 2

Select:
- Azure resources

---

## Step 3

Choose:
- Resource to audit

---

## Step 4

Select:
- Resource audit

---

# Filtering Audit History

Administrators can filter by:
- Date range
- Custom time periods
- Audit types

---

# Audit Type Filtering

Example:
- Activate (Assigned + Activated)

This filter shows:
- Role activations
- Assignment activations

---

# User Activity Details

Under Action:
- Select activity

PIM displays:
- Detailed Azure resource activity
- User operations during activation

---

# Audit History Analytics

PIM audit history can display:
- Total activations
- Maximum activations per day
- Average activations per day

---

# Role-Based Filtering

If multiple roles exist:
- Audit history can filter by role

This helps:
- Simplify investigations
- Focus on specific privileged roles

---

# Export Role Assignments

Organizations may need:
- Compliance reporting
- Audit evidence
- Complete role assignment exports

PIM supports exporting:
- Active assignments
- Eligible assignments
- Child resource assignments

---

# Previous Limitation

Previously:
- Administrators exported assignments resource-by-resource

This process was:
- Time consuming
- Difficult to manage

---

# Improved PIM Export Capability

PIM now allows:
- Exporting all role assignments from a subscription

Including:
- Resource groups
- Child resources
- All nested resources

---

# Steps to Export Role Assignments

## Step 1

In Microsoft Entra admin center:
- Select Identity governance
- Select Privileged Identity Management

---

## Step 2

Select:
- Azure resources

---

## Step 3

Choose:
- Resource to export

Example:
- Subscription

---

## Step 4

Select:
- Members

---

## Step 5

Select:
- Export

---

## Step 6

In Export membership pane:
- Select Export all members

---

# Export Output

PIM exports:
- CSV file containing role assignments

Includes:
- Active assignments
- Eligible assignments
- Child resource assignments

---

# Compliance Benefits

Exporting assignments helps organizations:
- Meet audit requirements
- Demonstrate compliance
- Track privileged access
- Support governance initiatives

---

# Key Security Benefits of PIM Auditing

PIM auditing helps organizations:
- Improve visibility
- Detect misuse
- Monitor privileged activity
- Reduce insider threats
- Support investigations
- Meet compliance standards

---

# Key Exam Points

## What Can PIM Audit?

- Activations
- Resource activity
- Privileged actions
- Role assignments

---

# What Resources Support PIM Auditing?

Any Azure RBAC-enabled resource:
- Subscriptions
- Resource groups
- Virtual machines

---

# What Can Be Exported?

- Active role assignments
- Eligible role assignments
- Child resource assignments

---

# Export Format

Exports are downloaded as:
- CSV files

---

# Audit History Filtering

Audit history can filter by:
- Date
- Role
- Audit type

---

# Important Limitation

PIM does NOT show:
- Role assignments managed by external delegated providers

---

# Common Audit Metrics

PIM tracks:
- Total activations
- Maximum activations
- Average activations

---

# Best Practices

Microsoft recommends:
- Regularly reviewing audit logs
- Monitoring privileged activations
- Exporting assignments for compliance
- Investigating unusual activity
- Using least privilege principles

---

# Important Concepts

| Concept | Meaning |
|---|---|
| Activation | Temporary privileged access |
| Audit History | Record of privileged activity |
| Resource Audit | Role activity for a resource |
| Eligible Assignment | Requires activation |
| Active Assignment | Immediate privileges |
| Export Membership | CSV export of assignments |

---

# Final Summary

Microsoft Entra PIM auditing helps organizations:
- Monitor privileged activities
- Review role activations
- Investigate security events
- Export assignment data
- Meet compliance requirements

PIM provides:
- Visibility
- Governance
- Security monitoring
- Compliance reporting

---

# Exam Tip

Remember:

PIM auditing focuses on:
- Activities
- Activations
- Audit history
- Assignment exports

