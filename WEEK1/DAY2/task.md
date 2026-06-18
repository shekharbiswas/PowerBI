# 🔌 Connectors, Triggers & Automation
### Dataskools | Power BI Programme
**Estimated Time: 1.5 Hours** | Data Source: Capital Bikeshare

---

## 🗂️ How This Session Is Structured

| Block | Activity | Time |
|---|---|---|
| Block 1 | Coursera Videos + Readings | 30 mins |
| Block 2 | Connector Mapping Exercise | 30 mins |
| Block 3 | Trigger Scenario Task + Reflection | 30 mins |

---

## 📘 Block 1 — Coursera (30 Minutes)

Complete the following in **Module 1** on Coursera before moving to the tasks:

- ✅ What are connectors? (video)
- ✅ Triggers and actions (video)
- ✅ Exercise: Implementing triggers (reading)
- ✅ Self-review: Implementing triggers
- ✅ Exemplar: Implementing triggers
- ✅ Discussion: How can stakeholders benefit from triggers and actions?

**Before moving to Block 2 — write one sentence answering this:**
> *"The difference between a connector and a trigger in Power BI is..."*

---

## 🚲 Block 2 — Connector Mapping Exercise (30 Minutes)

### Context
Capital Bikeshare data is currently published as static monthly CSV files. But imagine you are the data analyst for a modern bike sharing company that uses cloud tools across every department. Your job is to map where the data lives and how Power BI could connect to it.

---

### Step 1 — Read The Business Scenario (5 mins)

Your company runs a bike sharing service across three cities. The following systems are used daily across the business:

| Department | Tool Used | Data Generated |
|---|---|---|
| Operations | Google Sheets | Daily bike availability by station |
| Finance | Excel (SharePoint) | Weekly revenue and refund records |
| Marketing | Salesforce | Customer acquisition campaigns |
| Engineering | SQL Server | Live trip and sensor data |
| Customer Support | Zendesk | Support tickets and complaint logs |
| HR | SharePoint Lists | Staff rosters and shift schedules |

---

### Step 2 — Connector Classification Task (15 mins)

For each department above, complete the following table in your notes:

| Department | Power BI Connector To Use | Data Refresh Frequency Needed | Import or DirectQuery? | Reason For Your Choice |
|---|---|---|---|---|
| Operations | | | | |
| Finance | | | | |
| Marketing | | | | |
| Engineering | | | | |
| Customer Support | | | | |
| HR | | | | |

> **Tip:** Think about how often the data changes and how critical it is that the report shows current data. That determines your connector and storage mode choice together.

---

### Step 3 — Connector Research Task (10 mins)

Go to **https://learn.microsoft.com/en-us/power-bi/connect-data/power-bi-data-sources** and find the official list of Power BI data connectors.

Answer the following in your notes:

- How many connector categories does Microsoft list?
- Name two connectors you had never heard of before today
- Which connector category would Capital Bikeshare's CSV files fall under?
- If Capital Bikeshare published their data via a live API instead of CSV — which connector category would you use?

---

## 🧠 Block 3 — Trigger Scenario Task + Reflection (30 Minutes)

### Step 1 — Trigger Design Exercise (15 mins)

A trigger is an event that automatically starts an action. Read each situation below and design a simple trigger and action pair for each one. Write your answers in your notes.

**Situation 1:**
The Capital Bikeshare operations team updates a Google Sheet every morning at 7am with the previous day's station availability data. The Head of Operations wants the Power BI dashboard to always show yesterday's data without anyone manually refreshing it.

> **Your trigger:** *(what event starts the automation?)*
> **Your action:** *(what does Power BI do when the trigger fires?)*
> **Who benefits and how?**

---

**Situation 2:**
The finance team uploads a new monthly revenue Excel file to SharePoint on the first working day of every month. The CFO wants an email notification sent automatically when the Power BI report has been updated with the new data.

> **Your trigger:**
> **Your action:**
> **Who benefits and how?**

---

**Situation 3:**
The engineering team's SQL Server records a new entry every time a bike trip is completed. Leadership wants a live operations dashboard that always shows trips completed in the last 60 minutes.

> **Your trigger:**
> **Your action:**
> **Who benefits and how?**

---

**Situation 4:**
A data quality rule states that if any station in the Google Sheet shows zero bikes available for more than two consecutive hours, the operations manager should be alerted immediately.

> **Your trigger:**
> **Your action:**
> **Who benefits and how?**

---

### Step 2 — Reflection Questions (15 mins)

Write minimum 2–3 sentences per answer in your learning journal.

**Q1 — Real World Connection:**
Think about the Capital Bikeshare CSV files you downloaded on Day 1. These are published monthly by a human manually. Design a simple automated workflow that would replace this manual process using connectors and triggers. What would need to change on Capital Bikeshare's side for this to be possible?

**Q2 — Automation vs Control:**
Some analysts worry that automating data refreshes means errors get pushed into reports without anyone noticing. Do you agree with this concern? What safeguards would you build into an automated Power BI workflow to catch bad data before it reaches a dashboard?

**Q3 — Stakeholder Impact:**
The Coursera discussion asked how stakeholders benefit from triggers and actions. Write your own answer here before or after posting in Coursera. Name a specific stakeholder role (CFO, Operations Manager, Marketing Lead) and explain concretely how one automation saves them time or improves their decisions.

---

## ✅ Session Completion Checklist

Before marking this session complete confirm you have:

- [ ] Completed all six Coursera items listed in Block 1
- [ ] Written your one sentence summary of connectors vs triggers
- [ ] Completed the Connector Classification table for all six departments
- [ ] Answered the four connector research questions from the Microsoft docs page
- [ ] Designed trigger and action pairs for all four situations
- [ ] Written full answers to all three reflection questions

---

## 📁 Files To Update After This Session

Add the following to your `/Documents/Dataskools/Day1/` folder:

| File | What To Add |
|---|---|
| `Day1_Notes.docx` | Connector classification table, trigger designs, reflection answers |
