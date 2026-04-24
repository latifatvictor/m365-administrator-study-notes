# Manage User Account Settings in Microsoft 365

---

## 🔑 Key Concepts (Must Know)

Managing user accounts involves:

- updating user details  
- assigning roles and licenses  
- controlling access and permissions  

👉 This is one of the **most frequent IT support activities**

---

## 🧠 Identity Model Determines Management

### Cloud-Only Environment

- Users managed in:
  - Microsoft 365 Admin Center  
  - Microsoft Entra Admin Center  
  - PowerShell  

---

### Hybrid Environment

- Users managed in:
  - On-prem Active Directory  

👉 Changes sync to Microsoft 365  

---

### Key Rule

👉 If directory sync is enabled →  
You CANNOT edit core attributes in Microsoft 365  

---

## ⚙️ Tools for Managing Users

### Microsoft 365 Admin Center (MOST USED)

- Simple UI  
- Manage users individually or in bulk  

---

### PowerShell

- Script-based management  
- Useful for automation  

---

### Bulk Import (CSV)

- Modify multiple users  

---

### Microsoft Entra ID

- Advanced identity features  
- Self-service password reset  
- Access control  

---

### Directory Synchronisation

- Sync users from on-prem AD  
- Enables SSO  
- Required for hybrid setups  

---

## ⚠️ Important Rule

👉 Users MUST have:

- Location  
- License  

Before they can access Microsoft 365 services  

---

👉 Without a license:
User exists but cannot use services

---

## ⚙️ Managing Users in Admin Center

Path:

Users → Active Users → Select User

---

## 🧾 User Settings You Can Manage

### 1. Account Settings

- Username and aliases  
- Email addresses  
- Group membership  
- Roles  
- Contact details  
- MFA settings  
- Sign-in activity  
- Force sign-out  

---

### 2. Devices

- View enrolled devices  
- Managed via Intune  

---

### 3. Licenses and Apps

- Assign/remove licenses  
- Set user location  
- Enable/disable apps  

---

👉 Real-world:
Disable Teams or Exchange for specific users

---

### 4. Mail Settings

- Mailbox permissions  
- Email forwarding  
- Auto-replies  
- Global address list visibility  
- Litigation hold  

---

### 5. OneDrive Settings

- Access user files  
- Manage storage  
- Control external sharing  

---

## 💼 Real-Life IT Tasks

- resetting passwords  
- assigning licenses  
- enabling MFA  
- adding users to groups  
- granting mailbox access  
- troubleshooting login issues  
- forcing sign-out sessions  
- disabling accounts for leavers  

---

## ⚠️ Common Mistakes

- editing cloud user when sync is enabled  
- forgetting to assign license  
- incorrect user location  
- giving too many admin roles  
- not enforcing MFA  

---

## 🔥 Interview Questions

### Q1: Where do you manage users in Microsoft 365?

👉 Answer:
In the Microsoft 365 admin center, Microsoft Entra admin center, or using PowerShell.

---

### Q2: Can you edit users in Microsoft 365 if directory sync is enabled?

👉 Answer:
No, core user attributes must be managed in on-prem Active Directory.

---

### Q3: What happens if a user has no license?

👉 Answer:
They can sign in but cannot access Microsoft 365 services.

---

### Q4: What key settings do you manage for users?

👉 Answer:
Licenses, roles, MFA, location, mailbox settings, and group membership.

---

### Q5: Why is user location important?

👉 Answer:
Because Microsoft uses it to determine which services are available to the user based on regional regulations.

---

## 🧠 Summary

- user management depends on identity model  
- admin center is the primary tool  
- license + location are mandatory  
- hybrid environments require AD management  

👉 Good user management = secure + functional environment
