## Microsoft Defender for Office 365 Protection Stack Summary

### Overview:
- Provides **multi-layered email security** across Microsoft 365
- Protects against:
  - Spam
  - Phishing
  - Malware
  - Advanced attacks
- Consists of **4 layers** that filter messages at different stages

---

## Layer 1: Edge Protection
- First contact point for incoming email
- Blocks threats before entering the organization

### Key Features:
- Network throttling (prevents DoS attacks)
- IP/domain reputation blocking
- Directory-based edge filtering (prevents harvesting)
- Backscatter detection (blocks fake NDRs)
- Enhanced filtering for connectors

---

## Layer 2: Sender Intelligence
- Validates sender identity and behavior

### Key Features:
- Account compromise detection
- Email authentication (SPF, DKIM, DMARC, ARC)
- Spoof intelligence (internal & external)
- Mailbox intelligence (learns normal behavior)
- Impersonation protection:
  - User impersonation
  - Domain impersonation
- Bulk email filtering

---

## Layer 3: Content Filtering
- Analyzes email content, links, and attachments

### Key Features:
- Mail flow rules (transport rules)
- Anti-malware scanning (Microsoft + third-party engines)
- Attachment & URL reputation blocking
- Heuristics and machine learning detection
- Safe Attachments (sandboxing)
- URL/linked content detonation
- Common attachment filtering

---

## Layer 4: Post-Delivery Protection
- Protects users **after email delivery**

### Key Features:
- Safe Links (time-of-click protection)
- Zero-hour auto purge (ZAP):
  - Phishing
  - Malware
  - Spam
- Campaign Views (attack visibility)
- Report message/phishing tools
- Protection across:
  - OneDrive
  - SharePoint
  - Teams
  - Office apps

---

## Key Takeaway:
Microsoft Defender for Office 365 uses a **defense-in-depth approach**, combining **pre-delivery filtering, intelligent analysis, and post-delivery protection** to defend against modern email-based threats.
