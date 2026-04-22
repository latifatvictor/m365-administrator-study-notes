# Create User Accounts in Microsoft 365

---

## 🔑 Key Concepts (Must Know)

User provisioning is the process of:

- creating user accounts  
- assigning licenses  
- granting access to services  

👉 This is one of the most common IT admin tasks

---

## ⚙️ Methods to Create Users

Microsoft 365 supports multiple ways to create users:

---

### 1. Microsoft 365 Admin Center (MOST COMMON)

### What it is

- Web-based interface  
- Simple and user-friendly  

---

### Steps

1. Go to Admin Center  
2. Users → Active Users  
3. Click **Add a user**  
4. Enter user details  
5. Assign license  
6. Assign role (optional)  
7. Review and create  

---

### Best For

- Small number of users  
- Manual onboarding  

---

👉 Real-world:
Used daily by IT support teams

---

## 📥 2. Bulk Import (CSV)

### What it is

- Create multiple users at once  
- Uses CSV file  

---

### Key Steps

1. Prepare CSV file  
2. Upload in Admin Center  
3. Validate file  
4. Assign licenses  
5. Create users  

---

### Benefits

- Saves time  
- Reduces manual work  

---

👉 Real-world:
Used during large onboarding (e.g. new department)

---

## 💻 3. PowerShell (Advanced)

### What it is

- Script-based user creation  
- Uses Microsoft Graph PowerShell  

---

### Setup

```powershell
Install-Module Microsoft.Graph -Scope CurrentUser
Import-Module Microsoft.Graph.Identity.DirectoryManagement
Connect-MgGraph -Scopes 'User.ReadWrite.All'
