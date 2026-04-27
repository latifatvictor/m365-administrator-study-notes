# Create and Manage Groups in Microsoft 365

---

## 🔑 Overview

Groups in Microsoft 365 are essential for:

- managing access to resources
- assigning permissions
- enabling collaboration
- simplifying administration

Instead of assigning permissions to individual users, organisations should use groups.

---

## 🧠 Real-World Example

A company creates a **Security Group for Marketing users** and grants that group access to a SharePoint site.

👉 Result:
- Easy access management
- No need to manage users individually

---

## ✅ Best Practices

- Use **clear and simple naming conventions**
- Define **group governance policies**
- Assign **permissions to groups, not users**
- Maintain a **consistent provisioning process**
- Always assign **at least 2 group owners**

---

## 🛠️ Create a Group (Admin Center)

1. Go to **Microsoft 365 Admin Center**
2. Select:
   - Groups → Active groups
3. Click **Add a group**
4. Select **Group type**
5. Enter:
   - Name
   - Description
6. Assign **Owners**
7. Configure:
   - Email (if applicable)
   - Privacy (Public / Private)
   - Teams (optional)
8. Review and click **Create**

---

## ⚠️ Important

- Synced groups from on-prem AD **cannot be edited in M365**. You can only use local Active Directory management tools to modify security groups that are synchronized with your on-premises Active Directory.
- Must use **on-prem Active Directory tools**

---

## 💻 Create Group with PowerShell

```powershell


⚠️ Warning
Poor nesting = permission issues
Plan group structure carefully


🗑️ Delete a Group
Admin Center:
Groups → Active groups
Select group
Click Delete


PowerShell:
Remove-MgGroup -GroupId <GroupID>


♻️ Restore Groups
Only Microsoft 365 Groups can be restored
Recovery window = 30 days


🔄 What Gets Restored?
Group object & members
Email & calendar
SharePoint site
Teams
Planner
OneNote
Power BI workspace



❌ What Cannot Be Restored
Security groups
Distribution groups


🎯 Group-Based Licensing
What is it?

Assign licenses to a group instead of users.

👉 Example:

Assign M365 E3 to "Marketing Group"
All members automatically get licenses



⚙️ Benefits
Automatic license assignment
Auto removal when users leave group
No manual admin work


📋 Requirements
Microsoft Entra ID P1 or higher
Or:
M365 Business Premium
M365 E3/E5


🧩 Features
Works with Security Groups
Supports:
M365
EMS
Dynamics 365
Can disable specific services (e.g. Yammer)


⚡ Key Behaviour
Changes apply automatically within minutes
User in multiple groups:
License counted once
Conflicts may prevent assignment


⚠️ Common Issues
Not enough licenses
Conflicting service plans
Overlapping group memberships


🧠 Best Practices
Use group-based licensing wherever possible
Use dynamic groups for automation
Monitor license usage regularly
Avoid assigning licenses manually unless needed


💼 Real-Life Scenarios
Automatically license new employees
Assign department-based licenses
Remove licenses when users leave a team
Control app access via group membership


🔥 Interview Questions
Q1: Why use group-based licensing?

To automate license assignment and reduce admin effort

Q2: What happens when a user leaves a licensed group?

Their license is automatically removed

Q3: Can all group types be restored?

No, only Microsoft 365 Groups

Q4: Where do you manage group-based licensing?

Microsoft Entra Admin Center

Q5: Why should you assign permissions to groups instead of users?

To simplify management and improve scalability

🧠 Summary
Groups are essential for managing access and collaboration
Use proper group types for correct scenarios
Avoid assigning permissions directly to users
Use group-based licensing to automate processes
Plan group structure carefully to avoid issues
New-MgGroup -DisplayName "Test Group" `
-MailEnabled:$False `
-MailNickName "testgroup" `
-SecurityEnabled
