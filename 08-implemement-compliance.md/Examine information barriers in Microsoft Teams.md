## Information Barriers in Microsoft Teams – Summary

### Overview:
- Microsoft Purview Information Barriers (IB) control **who can communicate and collaborate** in Microsoft Teams
- Used to:
  - Prevent **conflicts of interest**
  - Restrict **sensitive data sharing**
  - Isolate specific business groups  

---

## Where IB Applies in Teams:
IB policies enforce restrictions across:

- ✅ Teams (channels and membership)
- ✅ 1:1 chats
- ✅ Group chats
- ✅ Meetings
- ✅ Calls
- ✅ File sharing
- ✅ User search (People picker)

---

## What IB Controls in Microsoft Teams:

### Prevents:
- Adding users to teams/channels  
- Starting chats (1:1 or group)  
- Inviting users to meetings  
- Joining meetings  
- Screen sharing  
- Voice/video calls  
- File sharing  
- Finding users (search/block discovery)

---

## Core Engine:
### Information Barrier Policy Evaluation Service (IBPES)
- Evaluates **every user action**
- Checks:
  - User policies  
  - Segment membership  
- Decides:
  - ✅ Allow  
  - ❌ Block  

---

## Key IB Triggers in Teams:

### 1. Adding Users to Teams
- IB checks compatibility with existing members  
- If conflict:
  - User **won’t appear in search**  
  - Cannot be added  

---

### 2. Starting Chats
- Evaluates all participants  
- If violation:
  - Chat is **blocked**  
- Applies to:
  - 1:1 chats  
  - Group chats  

---

### 3. Joining Meetings
- IB evaluates policies of:
  - Existing members  
  - Invited users  
- If conflict:
  - User **cannot join meeting**  

---

### 4. Screen Sharing
- Evaluated in real time  
- If violation:
  - Screen sharing **blocked**  

---

### 5. Voice Calls (VoIP)
- IB checks before call starts  
- If violation:
  - Call is **blocked**  

---

### 6. Guest Users
- IB policies apply to guests too  
- Guests must:
  - Be discoverable in address list  

---

## Impact of IB Policy Changes:

### 1. 1:1 Chats
- If newly blocked:
  - Chat becomes **read-only**
- Old messages visible  
- New messages blocked  

---

### 2. Group Chats
- Users violating policy:
  - ✅ Removed from group  
  - ❌ Cannot send messages  
- Can still view old messages  

---

### 3. Teams
- Conflicting users:
  - Removed from team  
  - Lose access to content  

---

## Information Barrier Modes in Teams:

### 1. Open Mode
- Default for old teams (before IB enabled)  
- ❌ No restrictions  

---

### 2. Implicit Mode
- Default for new teams (after IB enabled)  
- ✅ Allows only compatible users  

---

### 3. Owner Moderated Mode
- Team owner controls:
  - Adding users  
- ✅ Can allow exceptions based on policy  

---

### Example Command:
```powershell
Set-UnifiedGroup -InformationBarrierMode Implicit
``
