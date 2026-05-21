# Microsoft Defender for Office 365 – Create Safe Attachments Policies Using PowerShell Summary

## Overview
Organizations can manage Safe Attachments policies and rules separately using:
- Exchange Online PowerShell
- Standalone EOP PowerShell

A Safe Attachments implementation consists of:
- A Safe Attachments Policy
- A Safe Attachments Rule

---

# Key Difference Between Policy and Rule

## Safe Attachments Rule
Defines:
- Conditions
- Recipient filters
- Exceptions

## Safe Attachments Policy
Defines:
- Actions to take
- Redirect settings
- Malware handling behaviour

---

# Important PowerShell Requirement

When creating Safe Attachments using PowerShell:

1. Create the POLICY first
2. Create the RULE second

Reason:
- The rule must reference an existing policy.

If the rule is created first:
- No policy exists to assign to it.

---

# PowerShell Cmdlet Structure

## Policy Cmdlets
Managed using:
- *-SafeAttachmentPolicy

Examples:
- Get-SafeAttachmentPolicy
- New-SafeAttachmentPolicy
- Set-SafeAttachmentPolicy
- Remove-SafeAttachmentPolicy

---

## Rule Cmdlets
Managed using:
- *-SafeAttachmentRule

Examples:
- Get-SafeAttachmentRule
- New-SafeAttachmentRule
- Set-SafeAttachmentRule
- Remove-SafeAttachmentRule

---

# Behaviour Differences in PowerShell

## Policies and Rules Managed Separately
Unlike Microsoft Defender XDR:
- Rules and policies are fully independent in PowerShell.

---

## Removing Policies
Deleting a policy:
- Does NOT automatically delete the rule.

Deleting a rule:
- Does NOT automatically delete the policy.

---

# Safe Attachments Cmdlets Summary

| Task | Cmdlet |
|---|---|
| View policy settings | Get-SafeAttachmentPolicy |
| Edit policy | Set-SafeAttachmentPolicy |
| Create policy | New-SafeAttachmentPolicy |
| Delete policy | Remove-SafeAttachmentPolicy |
| View rule settings | Get-SafeAttachmentRule |
| Edit rule | Set-SafeAttachmentRule |
| Create rule | New-SafeAttachmentRule |
| Delete rule | Remove-SafeAttachmentRule |

---

# Two-Step Creation Process

## Step 1
Create the Safe Attachments Policy

## Step 2
Create the Safe Attachments Rule
- Assigns the policy to recipients

---

# Important Rule Limitation
A Safe Attachments rule:
- Can only be linked to ONE Safe Attachments policy.

---

# Extra PowerShell Features Not Available During Initial GUI Creation

PowerShell allows admins to:

## Create Disabled Policies
Using:
- Enabled $false

## Set Priority During Creation
Using:
- Priority <Number>

---

# Important Visibility Warning

A Safe Attachments policy created in PowerShell:
- Is NOT visible in Microsoft Defender XDR
until:
- It is assigned to a Safe Attachments rule.

---

# Step 1 – Create Safe Attachments Policy

## Syntax
```powershell
New-SafeAttachmentPolicy -Name "<PolicyName>" 
[-AdminDisplayName "<Comments>"] 
[-Action <Allow | Block | Replace | DynamicDelivery>] 
[-Redirect <$true | $false>] 
[-RedirectAddress <SMTPEmailAddress>] 
[-ActionOnError <$true | $false>]
