# Create and Manage Contacts in Microsoft 365

---

## 🔑 Overview

Contacts are external people that an organisation wants users to find in the shared address book.

In Exchange Online, mail contacts are mail-enabled objects for people outside the organisation.

They appear in:

- Global Address List (GAL)
- Shared address books
- Other address lists

---

## 🧠 Mail Contacts vs Mail Users

| Type | Description |
|---|---|
| Mail Contact | External person with an email address outside the organisation |
| Mail User | External user object with an email address in the organisation’s domain |

👉 Key point:
A mail contact does not need a Microsoft 365 user account.

---

## 💼 Common Use Cases

Mail contacts are useful for:

- vendors
- customers
- partners
- external consultants
- suppliers
- frequently contacted external organisations

Example:
Create a contact for a vendor so everyone can find them in Outlook without creating a user account.

---

## 🔐 Required Permissions

To create mail contacts, you need one of these roles:

- Global Administrator
- Exchange Administrator
- Directory Writers

---

## ⚙️ Create a Contact in Microsoft 365 Admin Center

### Location

Microsoft 365 Admin Center → Users → Contacts

### Steps

1. Go to Microsoft 365 Admin Center
2. Select Users
3. Select Contacts
4. Click Add a contact
5. Enter required details
6. Choose whether to hide from the GAL
7. Select Add
8. Select Close

---

## 📋 Contact Fields

Required fields include:

- Display name
- Email address

Optional fields include:

- First name
- Last name
- Company
- Job title
- Phone number
- Website
- Address
- Mail tip

---

## 👁️ Hide from Global Address List

You can choose whether the contact appears in the organisation’s Global Address List.

If hidden:

- users cannot easily find the contact in Outlook
- admins can still manage the contact

---

## ⏳ Propagation Time

After creating a contact, allow up to 30 minutes for changes to take effect.

---

## 🗑️ Remove a Contact in Microsoft 365 Admin Center

### Steps

1. Go to Microsoft 365 Admin Center
2. Select Users
3. Select Contacts
4. Select the contact
5. Click Delete contact
6. Confirm deletion

---

## ⚠️ Bulk Management Limitation

The Microsoft 365 Admin Center does not currently support bulk editing or bulk removal of mail contacts.

For bulk operations, use:

- Exchange Admin Center
- Exchange Online PowerShell

---

## 💻 Create Mail Contact with Exchange Online PowerShell

```powershell
New-MailContact -Name "Debra Garcia" -ExternalEmailAddress dgarcia@tailspintoys.com -Alias dgarcia


💻 Modify Mail Contact Details

Use:

Get-Contact
Set-Contact
Get-MailContact
Set-MailContact

Example: Update contact profile
Set-Contact "Allan Deyoung" -Title Consultant -Department "Public Relations" -Company Fabrikam -Manager "Alex Wilber"


💻 Hide All Mail Contacts from Address Lists
$Contacts = Get-MailContact -Resultsize unlimited
$Contacts | foreach {Set-MailContact -Identity $_ -CustomAttribute1 PartTime -HiddenFromAddressListsEnabled $true}


💻 Set Custom Attribute for Contacts in a Department
$PR = Get-Contact -ResultSize unlimited -Filter "Department -eq 'Public Relations'"
$PR | foreach {Set-MailContact -Identity $_ -CustomAttribute15 TemporaryEmployee}


💻 Remove Mail Contact with PowerShell
Remove-MailContact -Identity "Nestor Wilke"


💼 Real-Life IT Tasks
Creating contacts for vendors
Adding partner contacts to GAL
Hiding temporary contacts from address lists
Updating company or department details
Removing old external contacts
Managing contacts in bulk with PowerShell



⚠️ Common Mistakes
Creating a guest user when only a contact is needed
Forgetting that contacts do not provide login access
Using internal domains for mail contacts
Not allowing time for GAL updates
Trying to bulk edit contacts in the Microsoft 365 Admin Center



🔥 Interview Questions
Q1: What is a mail contact?

A mail contact is a mail-enabled object for an external person that appears in the organisation’s address book.

Q2: Does a mail contact have access to Microsoft 365?

No. A mail contact does not have sign-in access or a mailbox in the organisation.

Q3: What is the difference between a mail contact and a guest user?

A mail contact is used for address book visibility, while a guest user is used for external collaboration and access to resources.

Q4: Where can you manage mail contacts?

You can manage mail contacts in the Microsoft 365 Admin Center, Exchange Admin Center, or Exchange Online PowerShell.

Q5: Which PowerShell cmdlet creates a mail contact?

New-MailContact




🧠 Summary
Mail contacts represent external people
They appear in the GAL
They do not provide login access
They are useful for vendors, partners, and customers
PowerShell is best for bulk contact management

👉 Use contacts when users need to email external people regularly, but those people do not need access to company resources.
