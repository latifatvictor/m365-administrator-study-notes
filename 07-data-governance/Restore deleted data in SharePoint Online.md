## Restore Deleted Data in SharePoint Online Summary

### Overview:
- SharePoint Online uses **two recycle bins** for recovery:
  1. **Site (first-stage) recycle bin**
  2. **Site Collection (second-stage) recycle bin**
- Total retention period: **93 days (fixed, not configurable)**

---

## Recycle Bin Structure:

### 1. Site Recycle Bin (First Stage)
- Items go here immediately after deletion
- Users can:
  - View
  - Restore items
- Items remain here:
  - Until manually deleted OR
  - Until moved to second-stage bin

---

### 2. Site Collection Recycle Bin (Second Stage)
- Stores items deleted from Site recycle bin
- Accessible by:
  - Site collection administrators only
- Items remain here:
  - For the remainder of the **93-day retention period**

---

## Hard Deletion:
Occurs when:
- Items are permanently removed from second-stage recycle bin  
- Retention period expires  
- Admin deletes site using PowerShell  

---

## Restore Deleted Items (Site Recycle Bin):

### Steps:
1. Go to SharePoint site  
2. Select **Recycle bin**
3. Choose items/files  
4. Select **Restore**

✅ Restores items to original location  

---

## Restore from Site Collection Recycle Bin:

### Steps:
1. Go to **Recycle bin**
2. Select **Second-stage recycle bin**
3. Choose items
4. Select **Restore**

---

## Important Behavior:
- Restored items return to **original location**
- If original container (folder/library) is deleted:
  - Must restore container first
- Exception:
  - Folder may auto-recreate when restoring items

---

## Special Considerations:
- Restoring a library restores **all its contents**
- Restoring a file restores **all its versions**
- If file already exists:
  - Restored item gets renamed (e.g., appended number)

---

## Deleted Site Collections:
- Retained for **93 days**
- Can be restored by:
  - Global Administrator
  - SharePoint Administrator
- After 93 days → permanently deleted

---

## Storage Notes:
- Recycle bin storage counts toward site quota
- Second-stage recycle bin can use up to:
  - **200% of site collection quota**

---

## Backup Option:
- Microsoft retains backups for an additional **14 days**
- Admin can contact Microsoft Support for recovery within this window

---

## Key Takeaway:
SharePoint Online provides a **multi-stage recovery system with a 93-day retention window**, allowing users and administrators to restore deleted content efficiently before permanent deletion.
