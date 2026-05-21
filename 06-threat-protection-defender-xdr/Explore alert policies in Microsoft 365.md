## Alert Policies in Microsoft 365 (Defender XDR) Summary

### Overview:
- Alerts detect **suspicious or potentially malicious activities**
- Multiple related alerts are grouped into **incidents** for full attack context
- Not all alerts are malicious — some are for **monitoring sensitive actions**

---

### Alerts Management:
- Located in **Microsoft Defender portal → Incidents & Alerts → Alerts**
- Default view: **last 30 days (new & in-progress)**
- Can filter by:
  - Severity
  - Status
  - Service source
  - Affected entities (users, devices, mailboxes)
  - Investigation state

---

### Alert Analysis:
- Each alert includes:
  - **Alert story** (timeline of events and related alerts)
  - **Summary + detailed view**
- Enables:
  - Investigating attack flow
  - Viewing impacted assets
  - Taking actions directly (e.g., isolate device, disable user)

---

### Alert Sources:
- Defender for Endpoint  
- Defender for Office 365  
- Defender for Identity  
- Defender for Cloud Apps  

(Identified by prefixes like fa, da/ed, aa, ca in alert IDs)

---

### Key Features:
- **Alert story (process tree):** shows relationships & attack chain  
- **Entity details:** contextual info + history  
- **Action center integration:** view response actions  

---

### Managing Alerts:
- Set:
  - Status: New / In progress / Resolved
  - Assignment (analyst)
  - Classification:
    - True positive (real threat)
    - False positive (benign)
    - Informational (expected activity)

- Add comments for collaboration  
- Bulk manage **similar alerts**  
- Use **Recommendations** for guided response actions  

---

### Resolution:
- Mark alert as **Resolved**
- Classify outcome to improve detection accuracy
- Helps strengthen future threat detection models

---

### Key Takeaway:
Alerts provide **granular visibility into security events**, while incidents provide the **big picture**. Effective alert management improves detection, response, and overall security posture.
