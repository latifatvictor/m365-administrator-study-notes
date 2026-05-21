## Viewing Sensitive Data with Content Explorer & Activity Explorer – Summary

### Overview:
Microsoft Purview provides two key tools for **data classification analytics**:

- ✅ **Content Explorer** → “What data do we have and where is it?”
- ✅ **Activity Explorer** → “What are users doing with that data?”

Together, they give **full visibility into sensitive data and user behavior**.

---

# 🔍 1. Content Explorer

### Purpose:
- Provides a **snapshot of sensitive data** across the organisation  
- Shows:
  - ✅ Where data is stored  
  - ✅ What type of sensitive data exists  
  - ✅ What labels are applied  

---

## Key Capabilities:

### ✅ Identify Sensitive Data
- Detect:
  - Credit card numbers  
  - Personal data (PII)  
  - Financial data  
- Based on:
  - Sensitive information types  

---

### ✅ View Labelled Content
- Shows:
  - Sensitivity labels  
  - Retention labels  

---

### ✅ Data Location Visibility
- Displays:
  - Exchange  
  - SharePoint  
  - OneDrive  
  - Teams  

---

### ✅ Drill Down into Files
- Navigate:
  - Site → Folder → File  
- Open items directly for inspection  

---

### ✅ Export Results
- Export findings to:
  - CSV file  
- Useful for:
  - Reporting  
  - Auditing  

---

## Permissions Required:

### Two Roles:

| Role | Capability |
|------|------------|
| Content Explorer List Viewer | View items & locations |
| Content Explorer Content Viewer | View file contents |

⚠️ Important:
- These permissions override normal file permissions  

---

## How to Use Content Explorer:

1. Go to:
   - Microsoft Purview → Data classification → **Content explorer**
2. Filter by:
   - Sensitive info type OR label  
3. Select:
   - Data location  
4. Drill down:
   - Folder → File  
5. Review content  

---

## Filtering & Search:

### Search Examples:
- File name  
- File extension (.docx, .txt)  
- Site URL  
- Email address  

---

## Key Notes:
- ⏱️ Data updates can take up to **7 days**  
- ✅ Best used for:
  - Data discovery  
  - Risk identification  

---

# 📊 2. Activity Explorer

### Purpose:
- Tracks **user activities on sensitive data**
- Provides:
  - ✅ Behavioral insights  
  - ✅ Audit trail  
  - ✅ Risk detection  

---

## What It Monitors:

### Sensitive Data Activities:
- File access  
- File edits  
- Sharing actions  

---

### Label Activities:
- Label applied  
- Label changed  
- Label downgraded  

---

### DLP Events:
- Policy matches  
- Blocked actions  

---

### Endpoint Activities:
- File copied to USB  
- Printed  
- Shared  
- Deleted  

---

## Supported Sources:
- Exchange Online  
- SharePoint Online  
- OneDrive  
- Teams  
- Endpoint devices  

---

## Features:

### ✅ 30-Day Activity History
- Shows recent user activity  

---

### ✅ Rich Filtering (30+ Filters):

| Filter Type | Example |
|-------------|--------|
| Date range | Last 7 days |
| User | Specific employee |
| Activity type | File shared |
| Location | SharePoint |
| Label | Confidential |

---

### ✅ Visual Insights:
- Charts showing:
  - Activity trends  
  - Volume of events  

---

### ✅ Detailed Event Data:
- Each event includes:
  - User  
  - Timestamp  
  - File  
  - Action taken  

---

## Permissions Required:

### Roles:
- Information Protection Admin  
- Analyst / Investigator / Reader  

---

### Role Groups:
- Information Protection  
- Compliance Admin  
- Security Admin  

---

## Example Activities Tracked:

- ✅ File created / deleted  
- ✅ Copied to clipboard  
- ✅ Uploaded to cloud  
- ✅ Accessed by app  
- ✅ Shared externally  
- ✅ Label downgraded  

---

## Why Activity Explorer Matters:
- Detect:
  - Risky behavior  
- Validate:
  - DLP policy effectiveness  
- Investigate:
  - Incidents and breaches  

---

# 🔁 Content Explorer vs Activity Explorer

| Feature | Content Explorer | Activity Explorer |
|--------|----------------|------------------|
| Focus | Data at rest | Data in motion/use |
| Shows | What data exists | What users do |
| Insight | Sensitivity & labels | User actions |
| Use case | Discovery | Monitoring |

---

# ✅ Combined Use Case Example:

### Scenario:
- Identify sensitive HR data exposure  

---

### Step 1: Content Explorer
- Find:
  - HR files with PII  
- Locate:
  - Where files are stored  

---

### Step 2: Activity Explorer
- Check:
  - Who accessed/modified files  
  - If shared externally  

---

➡️ Result:
- Full visibility + actionable insights  

---

# ✅ Best Practices:

- ✅ Use Content Explorer for **data discovery**  
- ✅ Use Activity Explorer for **behavior monitoring**  
- ✅ Combine both for investigations  
- ✅ Regularly review reports  
- ✅ Export results for audit/compliance  
- ✅ Ensure proper role-based access  

---

# ⭐ Key Takeaway:
- **Content Explorer** answers:
  - “What sensitive data do we have?”  
- **Activity Explorer** answers:
  - “What is happening to that data?”  

➡️ Together, they provide **complete visibility over data risk, compliance, and user behavior in Microsoft 365**
