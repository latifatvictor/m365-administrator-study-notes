# Manage User Licenses in Microsoft 365

---

## 🔑 Key Concepts (Must Know)

### What is a License?

A license:

- grants access to Microsoft 365 services  
- is assigned per user  

👉 Example:
Without a license → no Outlook, Teams, or SharePoint access

---

## 🧠 Why License Management Matters

- controls user access  
- impacts cost  
- affects service provisioning  

👉 Real-world:
Wrong licensing = user cannot work OR wasted money

---

## ⚙️ Who Can Manage Licenses

Only users with roles like:

- Global Administrator  
- User Administrator  

---

## ⚠️ CRITICAL RULE

👉 Removing a license:

- deletes associated service data  
- 30-day recovery window  

👉 After 30 days → data is permanently lost  

---

## 📊 Viewing License Usage

### In Admin Center

Path:
Billing → Licenses

You can see:

- total licenses  
- assigned licenses  
- available licenses  

---

### Finding Unlicensed Users

Path:
Users → Active Users → Filter → Unlicensed users  

---

👉 Real-world:
Used when troubleshooting “user has no email”

---

## ⚙️ Assigning Licenses (Admin Center)

### Steps

1. Users → Active Users  
2. Select user(s)  
3. Manage product licenses  
4. Choose:

- Assign more  
- Replace  
- Unassign  

---

### Options Explained

- **Assign more** → add licenses  
- **Replace** → swap licenses  
- **Unassign all** → remove all licenses  

---

## ⚠️ Important Requirement

👉 Users MUST have a **Usage Location** set  

Otherwise:
- license assignment fails  

---

## 💻 Managing Licenses with PowerShell

### Connect to Microsoft Graph

```powershell
Connect-MgGraph -Scopes User.ReadWrite.All, Organization.Read.All
