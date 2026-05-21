# Microsoft Defender for Office 365 – Safe Attachments Summary

## What Safe Attachments Does
- Safe Attachments is a Microsoft Defender for Office 365 feature that protects organizations from malicious email attachments.
- It opens supported attachments in an isolated hypervisor environment (sandbox) to test for malicious behaviour before delivery.
- It helps detect threats before traditional antivirus signatures are available.

## Supported File Types
Safe Attachments commonly scans:
- Microsoft Office files (Word, Excel, PowerPoint)
- PDFs
- Executable files
- Flash files

## How Safe Attachments Works

### 1. Attachment Selection
- Scans attachments from both internal and external senders.
- Protection is controlled through policies configured by Microsoft 365 or security administrators.
- When a policy applies to a user, attachments are automatically checked.

### 2. Attachment Testing
- Scanning occurs in the same region as the organization’s Microsoft 365 data.
- Attachments are executed in virtual Windows environments.
- Behavioural analysis is performed to detect malicious activity such as:
  - Trojan installation
  - Registry changes
  - System setting modifications
  - Other suspicious behaviour

## Important Notes
- Microsoft Defender for Office 365 does NOT include a default Safe Attachments policy.
- However, the Built-in Protection Preset Security Policy provides automatic Safe Attachments protection for users not covered by:
  - Standard preset policies
  - Strict preset policies
  - Custom Safe Attachments policies
- Built-in protection is enabled by default for organizations with at least one Defender for Office 365 licence.

## Microsoft Recommendations
- Microsoft recommends purchasing enough Defender for Office 365 licences to cover all users.
- Exceptions to the Built-in protection policy are generally NOT recommended.

## Policy Behaviour Examples

### Scenario 1
- No Safe Attachments policies configured.
- Result:
  - Built-in Protection Preset Policy protects all users.

### Scenario 2
- Custom Safe Attachments policy applies only to Finance users.
- Sales users are not included.
- Result:
  - Sales users are still protected by Built-in Protection.

### Scenario 3
- A new Safe Attachments policy is created for all employees.
- Result:
  - Users are protected once the policy takes effect.
  - Policy propagation typically takes ~30 minutes.

### Scenario 4
- An internal user forwards an email with attachments externally.
- Result:
  - Internal users remain protected by Safe Attachments.
  - External recipients in Microsoft 365 organizations also receive protection.

## Key Takeaways
- Safe Attachments provides proactive protection against malicious email attachments.
- Uses sandboxing and behavioural analysis rather than relying only on antivirus signatures.
- Built-in Protection helps secure users automatically even without custom policies.
- Organizations can create targeted Safe Attachments policies for specific users, groups, or domains.

## Additional Reading
- Preset security policies in EOP and Microsoft Defender for Office 365
- Set up Safe Attachments policies in Microsoft Defender for Office 365
