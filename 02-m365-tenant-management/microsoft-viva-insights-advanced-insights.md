File Name: microsoft-viva-insights-complete-guide.md

# Microsoft Viva Insights Complete Guide

# Overview

Microsoft Viva Insights is part of Microsoft Viva and helps organisations improve productivity, wellbeing, collaboration, and workplace culture using Microsoft 365 collaboration data and organisational data.

It provides four major insight areas:

- Personal insights
- Team insights
- Organization insights
- Advanced insights

Viva Insights integrates into:

- Microsoft Teams
- Outlook
- Microsoft 365
- Power BI

---

# Core Viva Insights Areas

| Area | Main Audience | Purpose |
|---|---|---|
| Personal insights | Individual users | Improve personal productivity and wellbeing |
| Team insights | Managers | Understand team habits and culture |
| Organization insights | Leaders | Analyse organisational wellbeing and productivity |
| Advanced insights | Analysts | Perform deep workplace analytics |

---

# Privacy and Data Protection

Viva Insights analyses Microsoft 365 collaboration metadata such as:

- Emails
- Meetings
- Teams chats
- Calls
- Calendar activity

It does NOT analyse:

- Email content for managers
- User surveillance
- Keystrokes
- Screen tracking

---

# Important Privacy Principles

- Only users can see their own Personal insights
- Managers cannot see individual employee behaviour
- Data is aggregated and de-identified
- Minimum group sizes protect privacy
- Viva Insights uses metadata, not message content
- No tracking software runs on user devices

---

# Viva Insights Roles

| Role | Purpose |
|---|---|
| Insights Administrator | Configures Viva Insights and uploads organisational data |
| Insights Business Leader | Views Organization insights |
| People Manager | Views Team insights |
| Analyst | Full Advanced insights access |
| Analyst (Limited Access) | Restricted Advanced insights access |
| Program Manager | Coordinates plans and programmes |

---

# Feature Access by Role

| Feature | Admin | Analyst | Business Leader | People Manager |
|---|---|---|---|---|
| Personal insights | Yes | Yes | Yes | Yes |
| Team insights | No | No | No | Yes |
| Organization insights | No | No | Yes | Yes (if enabled) |
| Advanced insights | Limited | Yes | Limited | No |
| Upload organisational data | Yes | No | No | No |

---

# Personal Insights

# What Are Personal Insights?

Personal insights help employees improve:

- Focus
- Productivity
- Wellbeing
- Work-life balance
- Relationships

Only the individual user can see their Personal insights.

---

# Personal Insights Features

| Feature | Description |
|---|---|
| Viva Insights app | Teams and web experience |
| Outlook add-in | Productivity insights in Outlook |
| Briefing emails | Daily email summaries |
| Digest emails | Work habit summaries |
| Inline suggestions | Smart meeting and email recommendations |

---

# What Personal Insights Shows

- Meeting hours
- Focus time
- Collaboration patterns
- Response times
- Relationships
- Work-life balance
- Outstanding commitments

---

# Data Used for Personal Insights

| Data Source | Examples |
|---|---|
| Email metadata | Sender, recipients, timestamps |
| Calendar data | Meetings, duration, attendees |
| Teams activity | Calls, chats, meetings |
| OneDrive and SharePoint | File collaboration counts |

---

# Important Privacy Point

Only you can see your Personal insights.

Managers and administrators cannot access your personal productivity data.

---

# Team Insights

# What Are Team Insights?

Team insights help managers understand:

- Team collaboration habits
- Meeting culture
- Workload balance
- Burnout risks
- Focus time patterns

---

# Team Insights Privacy

Managers cannot see individual employee behaviours.

All Team insights are aggregated.

---

# How Teams Are Built

Teams are created using:

- Microsoft Entra ID
- Uploaded HR organisational data

The team includes:

- Direct reports only

Managers cannot manually edit team membership.

---

# Team Insights Features

| Feature | Purpose |
|---|---|
| Productivity insights | Meeting behaviours |
| Shared plans | Team focus plans |
| No-meeting day plans | Reduce meeting overload |
| Wellbeing plans | Improve work-life balance |

---

# Common Team Insights Metrics

- Meeting hours
- Multitasking in meetings
- Focus time
- After-hours work
- Collaboration habits

---

# Organization Insights

# What Are Organization Insights?

Organization insights help leaders understand:

- Organisational productivity
- Employee wellbeing
- Team culture
- Collaboration behaviours

---

# Requirements for Organization Insights

Users must:

- Have a Viva Insights premium licence
- Be assigned the Insights Business Leader role or group manager role
- Meet minimum reporting hierarchy size

---

# Organization Insights Tabs

| Tab | Purpose |
|---|---|
| Home | Overall organisation metrics |
| Wellbeing | Focus and work-life balance |
| Productivity | Meeting effectiveness |
| Teamwork | Collaboration networks |

---

# Organization Insights Metrics

| Metric | Meaning |
|---|---|
| After-hours collaboration | Work outside business hours |
| Uninterrupted focus hours | Time without meetings or chats |
| Daily connected hours | Active collaboration time |
| Collaboration hours | Total collaboration time |
| Meeting hours | Time spent in meetings |
| Join on time rate | Percentage of meetings joined on time |
| Multitasking hours | Overlapping meeting and email activity |
| Manager 1:1 meeting hours | Time with direct manager |
| Internal network size | Number of workplace connections |

---

# Organization Insights Features

| Feature | Purpose |
|---|---|
| Scope selector | Switch between company or reporting group |
| Indicators | Compare trends over time |
| Show details | View deeper analytics |
| Share button | Share insights via Teams or links |
| Set up plan | Launch wellbeing or productivity plans |

---

# Example Organization Insight Use Case

A company discovers:

- High meeting overload
- Increased after-hours work
- Reduced focus time

Leaders then:

- Introduce no-meeting days
- Encourage focus plans
- Reduce recurring meetings

---

# Advanced Insights

# What Are Advanced Insights?

Advanced insights provides deep workplace analytics using:

- Microsoft 365 collaboration data
- Organisational data
- Power BI reporting
- Custom queries

---

# Main Goals of Advanced Insights

Analyse:

- Work-life balance
- Hybrid work
- Collaboration culture
- Manager effectiveness
- Meeting culture
- Employee wellbeing

---

# Advanced Insights Tools

| Tool | Purpose |
|---|---|
| Organisational data upload | Add HR data |
| Query designer | Create custom analysis |
| Power BI templates | Visualise workplace trends |
| Analyst settings | Configure analysis rules |
| Data sources | Validate uploaded data |

---

# Organisational Data

Organisational data includes:

- Department
- Job role
- Location
- Region
- Level
- Manager
- Cost centre
- Direct reports

---

# Organisational Data Sources

Viva Insights gets data from:

1. Microsoft Entra ID
2. Uploaded CSV file

---

# CSV File Requirements

The CSV file must:

- Be UTF-8 encoded
- Be properly structured
- Contain required attributes
- Use alphanumeric file names only

Example:

```text
FileName2.csv
```

---

# Power BI Templates

# Main Templates

| Template | Purpose |
|---|---|
| Business resilience | Measure resilience and wellbeing |
| Hybrid workforce experience | Analyse hybrid work |
| Manager effectiveness | Measure management behaviours |
| Meeting effectiveness | Assess meeting quality |
| Ways of working | Analyse collaboration culture |
| Wellbeing balance and flexibility | Analyse focus and work-life balance |

---

# Hybrid Workforce Experience Report

Analyses:

- Remote workers
- Hybrid workers
- Onsite workers

Key areas:

- Collaboration
- Connectivity
- Work-life balance
- Onboarding
- Manager relationships

---

# Manager Effectiveness Report

Measures:

- Coaching
- Empowerment
- Manager capacity
- Team connection
- Leadership behaviours

---

# Meeting Effectiveness Report

Measures:

- Meeting load
- Recurring meetings
- Long meetings
- Large meetings
- Meeting engagement

---

# Custom Queries

There are two major query types:

1. Custom person queries
2. Custom meeting queries

---

# Custom Person Queries

Used to analyse:

- Work habits
- Collaboration
- Productivity
- Workload balance
- Focus time
- Team dynamics

---

# Common Person Query Use Cases

| Use Case | Purpose |
|---|---|
| Performance analysis | Understand work patterns |
| Collaboration analysis | Measure teamwork |
| Workload analysis | Identify overload |
| Diversity analysis | Examine cross-team collaboration |
| Benchmarking | Compare against goals |

---

# Custom Meeting Queries

Used to analyse:

- Meeting culture
- Attendee patterns
- Meeting effectiveness
- Recurring meetings
- Collaboration behaviour

---

# Common Meeting Query Use Cases

| Use Case | Purpose |
|---|---|
| Meeting type analysis | Compare meeting categories |
| Attendee analysis | Review participation |
| Effectiveness analysis | Measure outcomes |
| Trend analysis | Detect meeting overload |

---

# Real Workplace Example

A company notices:

- Remote workers feel disconnected
- Meeting overload is increasing
- New hires struggle to integrate

Using Advanced insights, analysts discover:

- Smaller internal networks for remote workers
- Reduced manager 1:1 time
- Excessive recurring meetings

The company responds by:

- Creating onboarding programmes
- Increasing manager check-ins
- Introducing no-meeting days
- Launching focus plans

---

# Best Practices

- Define business questions first
- Keep organisational data updated
- Protect employee privacy
- Use pilot groups
- Use Power BI templates as a starting point
- Use custom queries for deeper analysis
- Convert insights into action plans

---

# Common Mistakes

- Ignoring privacy protections
- Uploading poor HR data
- Over-monitoring employees
- Using outdated organisational data
- Failing to act on insights
- Overloading users with dashboards

---

# Viva Insights vs Traditional Monitoring

| Viva Insights | Employee Monitoring |
|---|---|
| Privacy-focused | Surveillance-focused |
| Aggregated insights | Individual tracking |
| Productivity improvement | Behaviour monitoring |
| Metadata analysis | Device tracking |
| Employee wellbeing | Employee surveillance |

---

# Important Viva Insights Concepts

| Concept | Meaning |
|---|---|
| Collaboration data | Metadata from Microsoft 365 |
| Organisational data | HR employee attributes |
| Focus time | Uninterrupted work blocks |
| After-hours work | Work outside configured hours |
| Network size | Workplace collaboration connections |
| Shared plans | Team productivity programmes |

---

# Key Exam Points

- Viva Insights is part of Microsoft Viva
- Personal insights are private to the user
- Team insights are aggregated for managers
- Organization insights help leaders analyse productivity and wellbeing
- Advanced insights supports deep analytics
- Organisational data provides context
- Analysts require the Insights Analyst role
- Power BI templates support workplace analytics
- Custom queries provide tailored analysis
- Privacy and minimum group sizes are critical

---

# Interview Questions

## Q1: What is Microsoft Viva Insights?

A workplace analytics platform that helps organisations improve productivity, wellbeing, and collaboration using Microsoft 365 data.

---

## Q2: What are the four main Viva Insights areas?

- Personal insights
- Team insights
- Organization insights
- Advanced insights

---

## Q3: Who can see Personal insights?

Only the individual user.

---

## Q4: What role is required for Advanced insights?

Insights Analyst.

---

## Q5: What is organisational data?

Employee descriptive information such as department, role, manager, and location.

---

## Q6: What are custom queries used for?

To perform tailored workplace analytics beyond standard reports.

---

## Q7: What is the purpose of Power BI templates?

To visually analyse workplace collaboration and productivity patterns.

---

# Summary

Microsoft Viva Insights helps organisations understand and improve:

- Productivity
- Collaboration
- Employee wellbeing
- Meeting culture
- Hybrid work
- Focus time
- Manager effectiveness

It uses Microsoft 365 collaboration metadata together with organisational data to provide actionable workplace insights.

The four main components are:

- Personal insights
- Team insights
- Organization insights
- Advanced insights

The platform strongly prioritises:

- Privacy
- Data protection
- Ethical analytics
- Aggregated reporting

Viva Insights enables organisations to make data-driven decisions that improve both employee experience and business outcomes.
