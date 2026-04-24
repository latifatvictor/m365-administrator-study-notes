# Guest Users (B2B Collaboration) in Microsoft 365

---

## 🔑 Overview

Microsoft Entra ID B2B collaboration allows organisations to securely work with external users such as:

- partners  
- vendors  
- contractors  
- customers  

👉 External users can access resources using their own credentials.

---

## 🧠 What Happens When You Add a Guest

- A user account is created in your tenant  
- UserType = Guest  
- UPN contains `#EXT#`  
- External user signs in with their own identity provider  

👉 Example UPN:
john_contoso.com#EXT#@yourtenant.onmicrosoft.com  

---

## 🔐 Types of Users

### External Guest (Most Common)

- External identity (Azure AD, Google, Microsoft account)  
- Limited access  
- UserType = Guest  

---

### External Member

- External user but with member-level access  
- Used in multi-tenant organisations  

---

### Internal Member

- Employee  
- Full access  
- UserType = Member  

---

### Internal Guest

- Legacy setup (internal account marked as guest)  

---

## ⚙️ Where Guest Access Is Used

Guest users can access:

- Microsoft Teams  
- SharePoint  
- OneDrive  
- Power Apps  
- Planner  
- Microsoft 365 Groups  

---

## 🔐 Guest Access Control

By default:

- Guests have limited permissions  

---

### Guest Permission Levels

| Level | Description |
|------|------------|
| Same as members | Full access |
| Limited (default) | Can see some directory info |
| Restricted | Can only see their own profile |

---

## ⚙️ External Collaboration Settings

Configured in:

Microsoft Entra Admin Center → Users → User settings → External collaboration settings  

---

### Key Controls

- Who can invite guests  
- Allow/block domains  
- Guest visibility restrictions  
- Self-service sign-up  
- Cross-tenant access  

---

## 📩 Invite a Guest User

### Steps

1. Go to Microsoft Entra Admin Center  
2. Users → All users  
3. Click **New user → Invite external user**  
4. Enter:
   - Email  
   - Name  
   - Optional message  
5. Click **Invite**  

---

👉 Result:

- Guest user added  
- Invitation email sent  
- Status = PendingAcceptance  

---

## 🔄 Invitation Redemption

- Guest receives email  
- Clicks link  
- Signs in with their provider  

---

👉 After acceptance:

- Status changes to Active  
- Identity provider is recorded  

---

## 👥 Add Guest to Group

1. Go to Groups  
2. Select group  
3. Members → Add members  
4. Select or invite guest  

---

👉 Real-world:
Grant Teams or SharePoint access

---

## 📱 Assign Guest to Application

1. Go to Enterprise Applications  
2. Select application  
3. Users and groups  
4. Add user  
5. Assign role  

---

👉 Default role: Default Access  

---

## ⚠️ Important Notes

- Guest invitations do NOT expire  
- Guests must accept invitation before access  
- Guest users can be removed anytime  
- Guest permissions should be restricted  

---

## 🔐 Security Best Practices

- Restrict who can invite guests  
- Use Conditional Access policies  
- Limit guest visibility  
- Review guest access regularly  
- Block untrusted domains  

---

## 💼 Real-Life IT Scenarios

- giving vendors access to SharePoint  
- adding consultants to Teams  
- collaborating with external partners  
- granting app access to third parties  
- removing guest access after project ends  

---

## ⚠️ Common Mistakes

- allowing all users to invite guests  
- not restricting domains  
- giving guests too much access  
- forgetting to remove guest users  
- not monitoring guest activity  

---

## 🔥 Interview Questions

### Q1: What is B2B collaboration?

It allows external users to access your organisation’s resources using their own credentials.

---

### Q2: What is a guest user in Microsoft 365?

A user from outside the organisation with limited access, stored as a Guest in Microsoft Entra ID.

---

### Q3: How do you identify a guest user?

Their UPN contains `#EXT#`.

---

### Q4: Where do you manage guest users?

Microsoft Entra Admin Center → Users → Guest users.

---

### Q5: How do you secure guest access?

By using:

- External collaboration settings  
- Conditional Access  
- Domain restrictions  

---

## 🧠 Summary

- B2B enables secure external collaboration  
- Guest users use their own credentials  
- Permissions must be controlled carefully  
- Guests can be added to groups and apps  

👉 Guest access = powerful but must be secured properly
