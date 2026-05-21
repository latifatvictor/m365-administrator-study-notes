# Microsoft Defender for Office 365 – Safe Attachments & Safe Links Quick Study Notes

## Safe Attachments
- Protects against malicious email attachments using sandboxing and behavioural analysis.
- No default Safe Attachments policy exists.
- Built-in Protection Preset Policy protects users automatically if no custom policy exists.

### Safe Attachments Actions
- Off = No Safe Attachments scanning
- Monitor = Deliver + monitor malware behaviour
- Block = Quarantine malicious emails (recommended for strict security)
- Dynamic Delivery = Deliver email body immediately while attachment scans in background (recommended for most orgs)

### Dynamic Delivery
- Placeholder attachment shown during scanning
- Safe file = reattached
- Malicious file = replaced with malware warning

### Safe Attachments Policy Components
- Policy = Defines actions
- Rule = Defines recipients, conditions, and priority

### Important Facts
- Lower priority number = higher priority
- Policy processing stops after first match
- Create policy FIRST, then rule in PowerShell

### Important Header
```text
X-MS-Exchange-Organization-SkipSafeAttachmentProcessing

Used to bypass Safe Attachments via transport rule.

Safe Links
Protects against malicious URLs and phishing attacks.
Uses URL rewriting and time-of-click verification.
Works across:
Email
Microsoft Teams
Office Apps
Safe Links Features
Rewrites URLs using:
https://nam01.safelinks.protection.outlook.com
Checks links again when users click them.
Protects against delayed phishing weaponization.
Recommended Safe Links Settings
Safe Links = ON
Internal email protection = ON
Real-time URL scanning = ON
Wait for scan before delivery = ON
Track user clicks = ON
Allow click-through to original URL = OFF
Safe Links Protection Areas
Email
Teams
Office apps (Word, Excel, PowerPoint, Outlook, etc.)
API Only Mode
Do not rewrite URLs, do checks via SafeLinks API only
URLs not rewritten
URLs still checked at click time
Safe Links Warning Pages
Scan in progress
Suspicious message
Phishing attempt
Malicious website
Error warning
Key Exam Points
Dynamic Delivery is Microsoft’s recommended Safe Attachments option.
Safe Links protects users at time-of-click.
Lower priority number = higher priority.
Safe Links URLs remain rewritten after forwarding/replying.
