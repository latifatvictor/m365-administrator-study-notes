## Cloud Discovery in Microsoft Defender for Cloud Apps Summary

### Overview:
- Analyzes **network traffic logs** against 25,000+ cloud apps
- Uses **90+ risk factors** to score apps
- Provides visibility into:
  - Cloud usage
  - Shadow IT
  - Security risks

---

## Types of Reports:

### 1. Snapshot Reports
- Manual upload of log files (firewalls/proxies)
- Provides **one-time analysis**

---

### 2. Continuous Reports
- Automated log collection and analysis
- Provides **ongoing visibility**
- Methods:
  - Defender for Endpoint integration
  - Log collectors (Syslog/FTP)
  - Secure Web Gateway integrations (Zscaler, iboss, etc.)
  - Cloud Discovery API (automation)

---

## Log Processing Flow:
1. **Upload:** Traffic logs sent to portal  
2. **Parse:** Extract relevant data  
3. **Analyze:** Match against cloud app catalog  
4. **Report:** Generate risk assessment  

- Updates occur **multiple times daily**

---

## Required Log Data:
- Timestamp  
- Source IP (user recommended)  
- Destination URL/IP  
- Data volume (upload/download)  
- Action (allowed/blocked)  

✅ More detailed logs = better visibility  

---

## Key Requirements:
- Supported data source or custom parser  
- Correct log format  
- Logs ≤ 90 days old  
- Must include outbound traffic  

---

## Snapshot Report Setup (Steps):
1. Collect firewall/proxy logs  
2. Go to **Settings → Cloud Apps → Snapshot reports**  
3. Create report and upload logs (max 20 files)  
4. Wait for analysis (minutes → hours)  
5. View generated report  

---

## Continuous Monitoring (Log Collectors):
- Automatically:
  - Receive logs (Syslog/FTP)
  - Compress and upload data
- Maintains:
  - Backup of last 20 logs
- Sends alert if no data received for **48 hours**

---

## Integrations:
- Defender for Endpoint → extended visibility beyond network  
- Secure Web Gateways → block unsanctioned apps  
- SIEM tools → advanced log forwarding  

---

## Key Benefits:
- ✅ Detect Shadow IT  
- ✅ Assess cloud app risk  
- ✅ Monitor user activity  
- ✅ Identify anomalies  
- ✅ Enable app governance decisions  

---

### Key Takeaway:
Cloud Discovery provides **deep visibility into cloud usage and risks** by analyzing traffic logs, helping organizations **detect Shadow IT and enforce secure cloud adoption**.
