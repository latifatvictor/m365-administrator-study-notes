## Troubleshooting Cloud Discovery – Microsoft Defender for Cloud Apps Summary

### Common Integration Issues (Defender for Endpoint):
- **Missing reports (Windows devices):**
  - Ensure devices are **Windows 10 v1809+**
  - Wait **up to 2 hours** for data ingestion

- **Empty discovery reports:**
  - If behind proxy → use **log collector to send logs**

---

## Log Parsing Errors:

- **Unsupported file type:**
  - Upload valid **text, ZIP, or GZIP log files**

- **Incorrect log format:**
  - Verify log isn’t corrupt
  - Match with **sample log format**

- **Logs older than 90 days:**
  - Export and upload **recent logs**

- **No cloud app traffic:**
  - Ensure logs include **outbound internet traffic**

- **Unsupported data source:**
  - Microsoft reviews and creates **custom parser**

---

## Log Collector Issues:

- **FTP connection failure:**
  - Use **FTP (not SFTP/SSH)**
  
- **Collector configuration failure:**
  - Check:
    - Access token
    - Port **443 outbound connectivity**

- **Logs not appearing:**
  - Check:
    - Governance log for parsing errors
    - Data source and collector linkage
    - Network configuration (ports, protocol)
    - Incoming connections (netstat)

- **Collector stuck in "Created":**
  - Deployment incomplete → finish setup

- **Collector "Disconnected":**
  - No logs received in **24 hours**

- **Docker deployment error:**
  - Insufficient disk space → increase host storage

---

## Dashboard Issues:

- **Empty dashboard despite successful upload:**
  - Caused by **overly restrictive filters**
  - Adjust filters to display available data

---

## Key Troubleshooting Tips:
- ✅ Validate log format and data completeness  
- ✅ Ensure correct network and port configurations  
- ✅ Monitor governance logs for errors  
- ✅ Confirm proper integration setup  
- ✅ Check filters if data seems missing  

---

### Key Takeaway:
Most Cloud Discovery issues stem from **log format problems, misconfigurations, or missing data**. Correct setup and validation ensure **accurate visibility into cloud usage and risks**.
