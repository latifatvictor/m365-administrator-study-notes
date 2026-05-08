# Monitor Tenant Health Using Microsoft 365 Usage Analytics

---

# 📌 What is Microsoft 365 Usage Analytics?

Microsoft 365 Usage Analytics is a reporting and analytics solution that helps organizations:

- Monitor Microsoft 365 usage
- Analyze adoption trends
- Track collaboration patterns
- Visualize service usage
- Create custom reports
- Share insights across departments

It provides:
- Prebuilt dashboards
- Historical usage data
- Cross-product reporting
- Department-level insights
- User activity analytics

---

# 🎯 Main Purpose

Microsoft 365 Usage Analytics helps organizations:

- Understand Microsoft 365 adoption
- Measure product usage
- Improve productivity
- Identify underused services
- Analyze collaboration behavior
- Monitor tenant health
- Support decision-making

---

# 📊 Main Features

- Interactive dashboards
- 12-month reporting history
- Custom reporting
- Power BI integration
- Department filtering
- Regional filtering
- Licensing insights
- User activity analysis

---

# 📌 Data Sources

Usage Analytics pulls data from:
- Microsoft 365 Activity Reports
- Microsoft Entra ID
- Exchange Online
- SharePoint Online
- Teams
- OneDrive
- Yammer
- Skype
- Office Apps

---

# 📈 Reporting Platforms

## 1. Microsoft 365 Admin Center
Provides:
- Built-in activity reports
- 7/30/90/180-day reporting

---

## 2. Power BI Template App
Provides:
- Advanced analytics
- 12-month history
- Visual dashboards
- Custom reports
- Department slicing
- Location analysis

Requires:
- Power BI Pro License

---

# 📅 Data Retention & Refresh

## Microsoft 365 Admin Center
Shows:
- 7 days
- 30 days
- 90 days
- 180 days

---

## Power BI Template App
Shows:
- Up to 12 months

---

# 🔄 Data Refresh Frequency

## Back-end Microsoft Service
Refreshes:
- Daily

Data latency:
- 5 to 8 days behind real-time

---

## Power BI Template App
Refreshes:
- Weekly by default

Can be customized.

---

# 📌 Important Data Notes

- User-level details available only for latest complete month
- Tenant-level aggregates available after enabling analytics
- Content Date column shows data freshness

---

# ⚙️ How to Enable Microsoft 365 Usage Analytics

## Prerequisites

Must be:
- Global Administrator

---

# 🛠️ Steps to Enable Usage Analytics

1. Open Microsoft 365 Admin Center
2. Navigate to:
   Reports → Usage
3. Scroll to:
   Microsoft 365 Usage Analytics
4. Select:
   Get Started
5. Enable:
   "Make organizational usage data available to Microsoft 365 usage analytics for Power BI"
6. Select Save
7. Refresh the page

---

# ⏳ Important Notes

- Data collection may take up to 48 hours
- Time depends on tenant size

---

# 📊 Power BI Template App

The Power BI template app provides:
- Advanced visualizations
- Cross-service analytics
- Custom slicing/filtering
- Department-level analysis
- Organizational insights

---

# 🔐 Power BI License Requirement

Requires:
- Power BI Pro License

---

# 👤 Roles That Can Access Usage Analytics

- Global Administrator
- Reports Reader
- Exchange Administrator
- Skype for Business Administrator
- SharePoint Administrator

---

# ⚙️ Power BI Template App Setup

## High-Level Process

1. Enable Usage Analytics
2. Copy Tenant ID
3. Open Power BI
4. Install Microsoft 365 Usage Analytics app
5. Connect tenant data
6. Configure OAuth2 authentication
7. Allow automatic refresh

---

# 📌 Authentication Requirement

Must use:
- OAuth2 authentication

Other methods may fail.

---

# 📊 Available Reports

---

# 1. Executive Summary Dashboard

Provides:
- High-level adoption overview
- Usage trends
- Collaboration insights
- Mobility reports
- Storage analytics

Purpose:
- Executive-level reporting
- Leadership visibility

---

# 2. Microsoft 365 Overview Report

Contains multiple sections.

---

## Adoption Report

Shows:
- Enabled users
- Active users
- Returning users
- First-time users
- Month-over-month adoption

---

## Usage Report

Shows:
- Active user volumes
- Product usage trends
- Activity metrics

---

## Communication Report

Tracks:
- Teams usage
- Email usage
- Yammer activity
- Skype activity

Purpose:
- Understand communication preferences

---

## Collaboration Report

Tracks:
- OneDrive usage
- SharePoint collaboration
- Internal sharing
- External sharing

---

## Storage Report

Tracks:
- Mailbox storage
- OneDrive storage
- SharePoint storage

---

## Mobility Report

Tracks:
- Device types
- Client apps
- Mobile access patterns

---

# 3. Activation & Licensing Report

Tracks:
- Office activations
- Device installations
- License assignments
- License utilization

---

# 📌 Activation Definition

A plan counts as activated when:
- User installs app
AND
- Signs in successfully

---

# 4. Product Usage Reports

Separate reports for:
- Exchange
- OneDrive
- Teams
- SharePoint
- Yammer
- Skype
- Microsoft 365 Groups

---

# 5. User Activity Reports

Provides:
- User-level activity
- AD attribute filtering
- Department reporting

---

# ⚠️ Important Restriction

Users with:
- Global Reader
- Usage Summary Reports Reader

Cannot view:
- User Activity Reports

---

# 🔍 Power BI Advantages

Power BI allows:
- Advanced filtering
- Department slicing
- Location analysis
- Custom visualizations
- Shared dashboards
- Executive reporting

---

# 📈 Real Work Example

IT notices:
- Low Teams adoption in Marketing department

Using Usage Analytics:
- Filter by department
- Review activity trends
- Compare against benchmarks

Action:
- Provide Teams training
- Promote collaboration tools

Result:
- Improved productivity
- Better adoption metrics

---

# 🧠 Interview Questions

## Q1: What is Microsoft 365 Usage Analytics?
A reporting solution that visualizes Microsoft 365 adoption and usage data.

---

## Q2: What license is required for Power BI Usage Analytics?
Power BI Pro License.

---

## Q3: How much historical data is available in Power BI?
Up to 12 months.

---

## Q4: How often is backend data refreshed?
Daily.

---

## Q5: What is the data latency?
5 to 8 days.

---

## Q6: What authentication method should be used in Power BI?
OAuth2.

---

## Q7: Which services are included?
- Exchange
- Teams
- SharePoint
- OneDrive
- Yammer
- Skype

---

# 🔐 Privacy & Identifiable User Information

Microsoft hides identifiable user information by default.

Organizations can:
- Keep reports anonymous
OR
- Show user identities

---

# ⚙️ How to Show Identifiable User Information

1. Open Microsoft 365 Admin Center
2. Navigate to:
   Settings → Org Settings
3. Select:
   Reports
4. Disable:
   "Display concealed user, group, and site names in all reports"
5. Save

---

# 📌 Important Notes

- Changes take several minutes
- Action is logged in Microsoft Purview Audit Logs

---

# 🔒 Privacy Best Practices

- Limit access to reports
- Use role-based access
- Protect user activity data
- Follow local privacy laws
- Audit report access regularly

---

# 📌 Key Differences: Adoption Score vs Usage Analytics

| Feature | Adoption Score | Usage Analytics |
|---|---|---|
| Focus | Digital transformation | Usage reporting |
| Dashboard | Built-in | Power BI |
| Benchmarks | Yes | Limited |
| Custom reports | Limited | Extensive |
| Historical data | 180 days | 12 months |
| User activity detail | Limited | Detailed |
| Power BI required | No | Yes |

---

# 🛠️ Automation & Reporting

Scripts and automation can be used for:
- Exporting reports
- Dashboard generation
- Scheduled analytics
- Department comparisons
- Usage monitoring
- Power BI integrations

(Commonly done using Microsoft Graph APIs and Power BI)

---

# 🔥 Key Exam Points

- Usage Analytics provides 12-month reporting
- Requires Power BI Pro for template app
- Backend data refreshes daily
- Data latency is 5–8 days
- OAuth2 required for authentication
- Supports custom Power BI reporting
- Can filter by department/location
- User information hidden by default
- Uses Microsoft Entra ID attributes

---

# 🚀 Summary

Microsoft 365 Usage Analytics is a powerful reporting and monitoring solution that helps organizations:

- Monitor tenant health
- Measure Microsoft 365 adoption
- Track collaboration trends
- Improve productivity
- Analyze user behavior
- Create executive dashboards
- Support digital transformation initiatives

It is widely used by:
- Microsoft 365 Administrators
- IT Managers
- Adoption Specialists
- Security Teams
- Leadership Teams

---
