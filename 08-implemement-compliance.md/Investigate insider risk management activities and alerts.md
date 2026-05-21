## Investigate Insider Risk Management Activities & Alerts – Summary

### Overview:
Investigating insider risks involves two primary tools:
- ✅ **User Activity Reports** → analyze individual user behavior  
- ✅ **Alerts Dashboard** → identify and triage risk events  

These tools help organizations **detect, assess, and respond** to risky user activity effectively.

---

## 1. User Activity Reports

### Purpose:
- Investigate **specific users** without needing a policy
- View **all detected activities** (even without alerts)

---

### Key Features:
- Covers up to **90 days of activity**
- No need for:
  - Policy assignment  
  - Triggering events  
- Requires:
  - Enabled **policy indicators**

---

### What You Can Do:
- View full user activity timeline  
- Identify risky patterns  
- Dismiss benign activities  
- Share reports with investigators  
- Assign user to policy if needed  

---

### User Activity Report Tabs:

#### 1. User Activity Tab:
- Timeline of activities  
- Risk score  
- Sequence detection (pattern view)  
- Filtering tools  

---

#### 2. Activity Explorer:
- Detailed analytics of activities  
- Filter and drill down into events  
- Analyze data behind alerts  

---

### How to Create Report:
1. Go to **Insider Risk Management → Overview**
2. Select **Manage reports**
3. Create report:
   - Select user  
   - Define date range (max 90 days)

⏱️ Reports ready in ~10 hours  

---

## 2. Alerts Dashboard

### Purpose:
- View and manage **alerts from policies**
- Central place for:
  - Risk visibility  
  - Alert triage  

---

### Dashboard Insights:
- Total alerts needing review  
- Alert trends (last 30 days)  
- Average resolution time  
- Severity distribution  

---

## Alert Statuses:

| Status | Meaning |
|--------|--------|
| Needs review | New alert |
| Confirmed | Escalated to case |
| Dismissed | Considered benign |
| Resolved | Closed case |

---

## Alert Severity Levels:

| Severity | Description |
|----------|------------|
| High | Significant risk |
| Medium | Moderate risk |
| Low | Minor risk |

---

### How Severity is Calculated:
- Activity type  
- Frequency of actions  
- User risk history  
- Risk boosters  

⚠️ Severity is automatic and cannot be customized  

---

## Alert Triage Process:

### Steps:
1. Open alert from dashboard  
2. Review:
   - Activity details  
   - User behavior  
3. Choose action:
   - ✅ Confirm → create case  
   - ✅ Assign to existing case  
   - ✅ Dismiss alert  

---

## Activity Explorer (Deep Analysis Tool)

### Purpose:
- Detailed investigation of alert-related activity  

---

### Features:
- Timeline of risky activity  
- Drill-down into event details  
- Filter by:
  - Activity type  
  - Risk factors  
  - User behavior  

---

### Key Filters:

#### Activity Scope:
- All activity  
- Only activity within alert  

---

#### Risk Insights:
- Unusual activity  
- Priority content  
- External sharing  
- Sequence detection  
- Exfiltration patterns  

---

## Important Notes:

### Alert Throttling:
- Built-in mechanism:
  - Prevents alert overload  
- May delay alert visibility  

---

### Data Differences:
- Activity counts may differ due to:
  - Deduplication (exfiltration detection)  
  - Policy/config changes  

---

## Best Practices:
- ✅ Use User Activity Reports for proactive investigation  
- ✅ Prioritize high-severity alerts  
- ✅ Leverage Activity Explorer for deep analysis  
- ✅ Provide reasons when dismissing alerts  
- ✅ Continuously refine policies to reduce noise  

---

## Key Takeaway:
Effective investigation in Insider Risk Management involves:
- Monitoring user behavior (reports)  
- Responding to alerts (dashboard)  
- Performing deep analysis (activity explorer)  

➡️ These tools together enable organizations to **identify, triage, and resolve insider risks efficiently while maintaining compliance and security**
