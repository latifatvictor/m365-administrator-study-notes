# Configure Tenant-Level Settings for Microsoft Teams

---

## 🔑 Key Concepts (Must Know)

### What are tenant-level Teams settings?

Tenant-level settings are organization-wide controls configured in the **Microsoft Teams admin center**.

They determine how users and guests can:

- access Teams
- use meetings, chat, and calling
- use apps
- interact as guests
- transition from Skype for Business

👉 Key idea:
These settings apply broadly across the organisation unless more specific policies are assigned.

---

## ⚙️ Main Teams Tenant-Level Settings

### 1. Guest Access

Controls whether external users can participate in Teams.

Guests can take part in:

- chats
- calls
- meetings
- channels

But they have limited access compared to internal users.

#### What admins can control
- whether guest access is enabled
- which domains can be allowed or blocked
- which Teams features guests can use

👉 Real-world:
Useful when working with clients, vendors, or partners

---

### 2. Teams Upgrade

Controls how an organisation transitions from **Skype for Business** to **Teams**.

#### Common coexistence / upgrade modes
- **Islands**
- **Teams Only**
- **Skype for Business Only**
- other coexistence modes

#### Why it matters
This determines which app is used for:

- chat
- meetings
- calling

👉 Real-world:
During migration, users may still use Skype while others use Teams

---

### 3. Teams Settings

This is the broadest area and controls major user experiences in Teams.

Includes settings for:

- app setup policies
- meeting policies
- messaging policies
- live event policies
- voice settings
- device settings

👉 Interview Tip:
If asked which setting customises many aspects of Teams, the answer is **Teams settings**

---

### 4. Teams Apps

Controls which apps users can access in Teams.

Admins can:

- approve apps
- block apps
- upload apps
- uninstall apps
- create app permission policies
- create app setup policies

#### App permission policies
Define which apps are allowed or blocked

#### App setup policies
Define which apps are:
- pinned to the app bar
- installed by default

👉 Real-world:
Useful for controlling third-party apps and standardising user experience

---

### 5. Teams Analytics and Reports

Used to monitor adoption, usage, and performance.

Examples include:

- Teams user activity report
- device usage report
- live event usage report
- call quality dashboard

👉 Real-world:
Helps identify adoption gaps, device trends, and meeting/call issues

---

## 🎥 Teams Meeting Policy Settings

Meeting policies define how users can schedule and run meetings.

Policies can be assigned to:

- individual users
- groups
- the entire organisation

### Common meeting policy settings

#### Allow scheduling private meetings
Controls whether users can create private meetings with specific invitees

#### Allow Meet now in channels
Controls instant meetings in channels

#### Allow channel meeting scheduling
Controls scheduled meetings published to channels

#### Allow IP video
Controls whether users can use camera/video in meetings

#### Allow screen sharing
Controls whether users can share their screen or apps

#### Allow transcription
Controls whether live meeting transcription is available

#### Allow cloud recording
Controls whether meetings can be recorded and stored in the cloud

#### Allow live captions
Controls live captions during meetings

#### Media bit rate
Controls maximum media bandwidth for meetings

#### Allow live events
Controls whether users can host large-scale live events

👉 Real-world:
Meeting policies are often adjusted for compliance, bandwidth, or user experience reasons

---

## 🧩 Meeting Configuration Settings

These apply to all meetings in the organisation.

Configured in:

**Teams admin center → Meetings → Meeting settings**

### Common configuration settings

#### Designated presenter role mode
Defines who can present in meetings

Options include:
- everyone
- only people in the organisation
- organiser only

#### Who can bypass the lobby
Defines who joins directly without waiting

#### Announce when callers join or leave
Controls join/leave audio alerts

#### Allow dial-in users to bypass the lobby
Controls whether phone users wait in lobby

#### Automatically admit people
Defines who is automatically admitted

#### Allow anonymous users to join
Controls whether unsigned-in users can join meetings

#### Allow users to chat privately
Controls private chat during meetings

#### Allow users to send reactions
Controls emoji reactions

#### Allow users to view shared notes
Controls access to shared meeting notes

👉 Real-world:
Lobby settings and anonymous access are very common security discussion points

---

## 💼 Real-Life IT Tasks

- enabling or disabling guest access
- managing Teams apps and blocking risky third-party apps
- configuring meeting recording permissions
- restricting anonymous meeting join
- changing lobby bypass settings
- reviewing call quality reports
- supporting Teams-only migration from Skype for Business

---

## ⚠️ Common Mistakes

- enabling guest access without reviewing domain or security settings
- allowing anonymous join when meetings are sensitive
- allowing too many apps without governance
- applying one meeting policy to all users without considering role differences
- ignoring bandwidth impact of video and screen sharing settings

---

## 🔥 Interview Questions

### Q1: Where do you configure tenant-level Teams settings?

👉 Answer:
In the Microsoft Teams admin center.

---

### Q2: What setting controls meeting recording and transcription?

👉 Answer:
Meeting policy settings.

---

### Q3: What is the difference between app permission policies and app setup policies?

👉 Answer:
App permission policies control which apps are allowed or blocked, while app setup policies control which apps are pinned or installed by default.

---

### Q4: What does Teams Only mode mean?

👉 Answer:
It means Teams is the primary app for chat, calling, and meetings, replacing Skype for Business for those users.

---

### Q5: Why would an organisation restrict anonymous meeting join?

👉 Answer:
To reduce security risk and ensure only authenticated users can access meetings.

---

### Q6: Which tenant-level setting lets admins customise app setup, meetings, messaging, live events, voice, and devices?

👉 Answer:
Teams settings.

---

## 🧠 Summary

- Teams tenant settings control organisation-wide collaboration experience
- key areas include:
  - guest access
  - upgrade mode
  - apps
  - analytics
  - meetings
- meeting policies control user experience
- meeting configuration controls organisation-wide defaults

👉 Teams administration is not just about chat — it’s governance, collaboration, security, and user experience combined
