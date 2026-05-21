# Microsoft Defender for Office 365 – Safe Links Summary

## Overview
Safe Links is a Microsoft Defender for Office 365 feature that protects users from malicious URLs used in:
- Phishing attacks
- Malware attacks
- Credential theft
- Other malicious web-based threats

Safe Links provides:
- URL scanning and rewriting
- Time-of-click verification
- Protection across:
  - Email
  - Microsoft Teams
  - Microsoft Office apps

---

# Core Safe Links Features

## 1. URL Scanning and Rewriting
Safe Links:
- Scans inbound email URLs
- Rewrites URLs using Microsoft Safe Links format

Example:
```text
https://nam01.safelinks.protection.outlook.com


2. Time-of-Click Protection

When users click a link:

Safe Links rechecks the URL in real time
Protects against delayed weaponization attacks
Why Safe Links Is Important

Attackers may:

Send links that initially appear safe
Weaponize them AFTER delivery

Safe Links still protects users because:

URLs are checked again at click time
Built-In Protection
Important Note

Microsoft Defender for Office 365 has:

NO default Safe Links policy

However:

Built-in Protection Preset Security Policy provides Safe Links protection automatically for users not covered by:
Standard preset policies
Strict preset policies
Custom Safe Links policies
Safe Links Protection Areas
1. Email Messages
2. Microsoft Teams
3. Office Apps
Safe Links for Email Messages
URL Rewriting

URLs are rewritten/wrapped during mail flow.

URL Behaviour
Rewritten URLs Stay Rewritten

Even when:

Emails are forwarded
Emails are replied to
Automatic Forwarding Behaviour

URLs are NOT rewritten during automatic forwarding unless:

Recipient is protected by Safe Links
OR
URL was already rewritten earlier
Time-of-Click Verification

Supported Outlook clients:

Windows
Mac
Outlook on the Web

perform Safe Links API checks at click time.

Email Safe Links Settings
1. Safe Links On/Off

Recommended:

ON

Features enabled:

URL rewriting
Click-time verification
Background scanning
2. Apply Safe Links to Internal Emails

Recommended:

ON

Protects:

Internal sender → Internal recipient emails
3. Real-Time URL Scanning

Recommended:

ON

Scans:

Suspicious URLs
Downloadable files
4. Wait for URL Scanning Before Delivery

Recommended:

ON

Behaviour:

Holds email until URLs are confirmed safe
5. Do Not Rewrite URLs, Use API Only

When enabled:

URLs are NOT rewritten
URLs are still scanned at click time using Safe Links API
Safe Links Limitations
Not Supported
Mail-enabled public folders
Rich Text Format (RTF) emails
Non HTTP(S)/FTP URLs
S/MIME signed messages
SharePoint and OneDrive URLs

Safe Links:

No longer wraps SharePoint/OneDrive URLs
Still scans them

Purpose:

Improve performance
Safe Links Email Flow Process
High-Level Flow
Email enters EOP
Anti-spam and anti-malware checks occur
Email delivered
User clicks URL
Safe Links checks URL
Safe Links Click Outcomes
Malicious URL
Warning page displayed
Downloadable File URL

If real-time scanning enabled:

File is scanned
Safe URL
Website opens normally
Safe Links for Microsoft Teams
Protection Behaviour
URLs checked at click time
URLs are NOT rewritten
Teams Protection Requirements
User must be included in active Safe Links policy
Teams protection must be enabled
Teams Warning Behaviour
Chat/Channel Links
Warning opens in browser
Pinned Tab Links
Warning appears inside Teams
Open-in-browser option disabled
Click-Through Behaviour

Controlled by:

Let users click through to the original URL

Microsoft Recommendation:

Disable click-through access
Teams Protection Delay

Policy changes may take:

Up to 24 hours
Safe Links for Office Apps
Protected Apps
Word
Excel
PowerPoint
Visio
OneNote Web
Outlook
Office mobile apps
Office App Requirements

Users must:

Use supported Office apps
Use modern authentication
Sign in with work/school account
Office Apps Protection Process
Workflow
User opens Office document
User clicks URL
Safe Links checks URL
Office Apps Outcomes
Malicious URL
Warning page displayed
Downloadable File
File scanned if enabled
Safe URL
Website opens normally
If Safe Links Cannot Scan

Desktop Office apps:

Warn the user before continuing
Safe Links Scenarios
Scenario 1

Marketing user opens PowerPoint with URL.
Result:

Protected if Office apps protection enabled.
Scenario 2

No custom policies configured.
Result:

Built-in Protection still protects users.
Scenario 3

Office apps protection disabled.
Result:

User NOT protected in Office documents.
Scenario 4

Internal user sends malicious URL internally.
Result:

Recipient protected if internal scanning enabled.
Do Not Rewrite URLs List

Each Safe Links policy includes:

Do not rewrite the following URLs

Purpose:

Exclude trusted URLs from rewriting/scanning during mail flow
Important Behaviour

Excluded URLs:

May STILL be blocked at click time

To fully allow:

Report URL as clean
Add to Tenant Allow/Block List
Safe Links Warning Pages
1. Scan in Progress
URL currently being scanned
2. Suspicious Message Warning
Message resembles suspicious/phishing emails
3. Phishing Attempt Warning
Email identified as phishing
URLs blocked
4. Malicious Website Warning
URL confirmed malicious
5. Error Warning
URL could not be opened
Important User Behaviour

Selecting:

Go Back

returns user safely.

Clicking the original URL again:

Triggers another Safe Links scan
Knowledge Check Answer

Question:
How can URLs be scanned before delivery without rewriting them?

Correct Answer:

Do not rewrite URLs, do checks via SafeLinks API only.
Key Takeaways
Safe Links protects users from malicious URLs using real-time click protection.
Protection extends across:
Email
Teams
Office apps
URLs can be rewritten and scanned during mail flow.
Safe Links protects against delayed phishing weaponization attacks.
Dynamic click-time analysis is one of Safe Links’ strongest security features.
Microsoft recommends enabling:
Real-time scanning
Internal email protection
Office apps protection
Teams protection
