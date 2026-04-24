# Recover Deleted User Accounts in Microsoft 365

---

## 🔑 Key Concepts

When a user leaves an organisation, their Microsoft 365 account should be removed or disabled to prevent unauthorised access.

When a user account is deleted:

- The account is removed from Active Users
- The user can no longer sign in
- The assigned licence becomes available for reuse
- The account is soft-deleted for 30 days before permanent deletion

---

## 🧠 Soft Delete vs Permanent Delete

### Soft Delete

- Default behaviour when a user is deleted
- User appears under Deleted Users
- Account can be restored within 30 days

### Permanent Delete

- Happens after the 30-day recovery period
- Account can no longer be restored
- Associated data may be permanently lost

---

## ⚙️ Delete a User in Microsoft 365 Admin Center

1. Go to Microsoft 365 Admin Center
2. Select Users
3. Select Active Users
4. Select the user
5. Click Delete user
6. Confirm deletion

---

## 💻 Delete a User with Microsoft Graph PowerShell

```powershell
Remove-MgUser -UserId "<UserId>"


🔄 Restore a Deleted User in Microsoft 365 Admin Center
Go to Microsoft 365 Admin Center
Select Users
Select Deleted Users
Select the deleted user
Click Restore user
Set or assign a password
Confirm restore


💻 Restore a Deleted User with Microsoft Graph PowerShell
Restore-MgDirectoryDeletedItem -DirectoryObjectId "<UserId>"


⚠️ Important Notes
Deleted users can be restored for up to 30 days
After 30 days, the user is permanently deleted
Restoring a deleted user reactivates the account
The user may need a licence reassigned after restore
Security groups cannot be recovered after deletion


💼 Real-Life IT Tasks
Delete accounts for leavers
Restore accidentally deleted users
Reassign released licences
Investigate missing user accounts
Support Joiner, Mover, Leaver processes



⚠️ Common Mistakes
Waiting longer than 30 days to restore a user
Forgetting to reassign a licence after restore
Deleting the wrong account
Assuming all deleted data is always recoverable
Not checking retention and recovery policies



🔥 Interview Questions
Q1: What happens when you delete a user in Microsoft 365?

A deleted user is soft-deleted, removed from Active Users, blocked from signing in, and the assigned licence becomes available for reuse.

Q2: How long can a deleted user be restored?

A deleted user can be restored within 30 days.

Q3: What happens after 30 days?

After 30 days, the user is permanently deleted and can no longer be restored.

Q4: Where can you restore a deleted user?

A deleted user can be restored from Microsoft 365 Admin Center under Users > Deleted Users.

Q5: What happens to the user’s licence after deletion?

The licence becomes available and can be reassigned to another user.

🧠 Summary
Deleted users are soft-deleted first
Microsoft 365 keeps deleted users for 30 days
Users can be restored during the 30-day recovery window
Licences are released when users are deleted
After 30 days, recovery is no longer possible
