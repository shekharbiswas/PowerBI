# Task Sheet — Bridge Day: Capital Bikeshare Presentation and Week 4 Preview

**Dataskools | Power BI Programme**
Estimated Time: 6 Hours | Tools: Power BI + Canva | Data: Capital Bikeshare Visual Report (W3D4)

---

## How This Day Is Structured

| Block | Activity | Time |
|---|---|---|
| Block 1 | Presentation Planning and Story Spine | 45 Minutes |
| Block 2 | Power BI Final Pass and Canva Deck Build | 1 Hour 45 Minutes |
| Block 3 | Present and Reflect | 30 Minutes |
| Block 4 | Forecasting and AI Visuals Primer | 1.5 Hours |
| Block 5 | Extending the Capital Bikeshare Dashboard | 1.5 Hours |

> **Note on today:** This is the last day of the core Capital Bikeshare build and the first day of going deeper on the same dataset. The presentation today is shorter than a full presentation day on purpose — the goal is to close this phase cleanly, not to spend the whole day polishing it further. The second half of today exists so that Week 4 does not start cold. Week 4 stays on Capital Bikeshare — we are not switching datasets. Instead, we use forecasting and AI-powered visuals to ask new questions of data we already know well. You will leave today having closed one phase of this project and opened the next.

---

## Block 1 — Presentation Planning and Story Spine (45 Minutes)

### Context

We already have a finished, presentation-ready file from Day 4. This block is about deciding what to say, not building anything new.

---

### Step 1 — Define Your Audience (10 mins)

Write in your notes which of the following you are presenting to today:

- **Option A — Internal report consumer:** someone who will use this dashboard regularly
- **Option B — Programme stakeholder or assessor:** someone judging the quality of the week's work
- **Option C — General audience:** someone with no Power BI background

Record what they already know and the one thing they must leave understanding.

---

### Step 2 — Build a Short Story Spine (25 mins)

Write each of the following in two to three sentences maximum — this is a compressed spine for a compressed presentation.

**The situation:** what Capital Bikeshare is and what this week's report covers.

**The findings:** two or three specific things the dashboard shows.

**One design decision:** one choice from the week — colour consistency, the drillthrough instead of a tooltip, what was left off the dashboard — and why it was made.

**The close:** one sentence on what this dashboard is ready for next.

> Keep this tight. A five-minute presentation does not need a nine-slide arc — it needs four clear points said well.

---

### Step 3 — Plan the Demo and the Deck (10 mins)

Decide, in writing:

- Which one or two things you will show live in Power BI — not a full walkthrough, just the dashboard and one interaction
- How many slides the Canva deck will have — aim for five or six, not nine

---

## Block 2 — Power BI Final Pass and Canva Deck Build (1 Hour 45 Minutes)

### Step 1 — Power BI Readiness Check (20 mins)

Open `W3D4_PowerBI.pbix` from `/Documents/Dataskools/Week3_Day4/` and save as `W3D5_PowerBI.pbix` in `/Documents/Dataskools/Week3_Day5/`

Confirm the dashboard and the one or two pages you plan to demo are clean: slicers at default state, no leftover test filters, all titles and colours consistent.

Export two to three visuals as PNG to `/Documents/Dataskools/Week3_Day5/Exports/`, including a screenshot of the Capital Bikeshare Overview dashboard.

---

### Step 2 — Build a Short Canva Deck (1 Hour 15 mins)

Build five or six slides in 16:9 format:

| Slide | Content |
|---|---|
| 1 | Title — project name, your name, date |
| 2 | Context — Capital Bikeshare in two to three sentences |
| 3–4 | Findings — one or two key findings, each with an embedded visual and one interpretation sentence |
| 5 | One design decision and why it was made |
| 6 | Close — one sentence on what the dashboard is ready for next |

Apply the same typography and colour rules used all week: two fonts maximum, the same member versus casual colour pair as the Power BI report, no slide more than 40% text.

Export the deck as PDF — **Share > Download > PDF Standard** — and save to `/Documents/Dataskools/Week3_Day5/` as `W3D5_Presentation.pdf`

---

### Step 3 — One Quick Run-Through (10 mins)

Talk through the deck once, including the brief live demo moment, with a timer. Confirm it lands at five to seven minutes, not longer. Fix anything that felt unclear.

---

## Block 3 — Present and Reflect (30 Minutes)

### Step 1 — Deliver the Presentation (10 mins)

Present the short deck plus the brief live demo, either to yourself, a peer, or a mentor.

---

### Step 2 — Closing Reflection (20 mins)

Write a minimum of two to three sentences per answer.

**Q1 — Closing This Phase:**
Now that the core Capital Bikeshare build is finished, what is the one thing you are most confident you could do again on a new dataset without guidance, and what is the one thing you would still want to look up or double-check?

**Q2 — What Carries Forward:**
Of everything built across the four weeks of this project — ETL, staging, profiling, visuals, accessibility, interactivity, dashboards, performance tuning — name the single skill you expect to lean on the most as we extend the dashboard with forecasting and AI visuals, and why.

---

## Block 4 — Forecasting and AI Visuals Primer (1.5 Hours)

### Context

Week 4 stays with Capital Bikeshare and introduces forecasting and AI-powered visuals on top of it. This block is a first exposure, not mastery — the goal is that none of this is unfamiliar going into the deeper build in Block 5.

---

### Step 1 — Watch and Read (30 mins)

Search Power BI's official documentation or Coursera resources for the following topics and spend roughly ten minutes on each:

- What forecasting in Power BI is and how the built-in line chart forecast feature works
- What the Key Influencers visual does and what kind of question it answers
- What the Decomposition Tree visual does and what kind of question it answers

Write a one-sentence plain-language definition of each in your notes.

---

### Step 2 — Try Forecasting on Familiar Data (30 mins)

Reopen `W3D5_PowerBI.pbix`. On the **Usage Over Time** page, select the monthly trend line chart.

Go to the **Analytics pane** and add a **Forecast**. Set a forecast length of a few months and apply it.

Observe the confidence interval shown around the forecast line. Write in your notes:

- Does the forecast look plausible given the trend you already know from this data?
- What does the confidence interval tell you about how certain Power BI is, and does that certainty seem to shrink or grow further into the forecast?

Leave the forecast in place for now — we will decide in Block 5 whether it becomes a permanent page in the dashboard.

---

### Step 3 — Try One AI Visual (30 mins)

On a blank area of any page, or a new temporary page, add a **Key Influencers** visual.

Set it to analyse what influences `member_casual` using the other fields available — for example time of day, day of week, or duration.

Read the output. Write in your notes: what does the visual claim is the strongest influence, and does that match what you already found through your own analysis earlier in the week?

If time allows, also try a **Decomposition Tree** visual breaking down total trips by `member_casual`, then station, then day of week. Write one sentence on what this visual makes easy to explore that a static bar chart does not.

Keep this page in the file for now — it feeds directly into Block 5, so there is no need to delete it today.

---

## Block 5 — Extending the Capital Bikeshare Dashboard (1.5 Hours)

### Context

This block is where Block 4's exploratory forecasting and AI visuals get turned into a proper, permanent extension of the Capital Bikeshare dashboard. We stay on the same dataset — the goal is depth, not breadth.

---

### Step 1 — Decide What Becomes Permanent (20 mins)

Review the forecast and AI visuals from Block 4. For each one, decide and write down:

- Does the forecast on the monthly trend line earn a permanent spot on the Usage Over Time page, or does it belong on a new dedicated **Forecast** page?
- Does the Key Influencers output say something worth keeping in front of a viewer, or was it more useful as your own exploratory step?
- Does the Decomposition Tree add something the existing dashboard pages do not already show?

---

### Step 2 — Build a Forecast Page (30 mins)

Create a new page named **Forecast** in `W3D5_PowerBI.pbix`.

Add the monthly trend line chart with the forecast applied, formatted to match the rest of the report — same fonts, same colour rules, clear title, a short text box explaining what the confidence interval means for a non-technical viewer.

If useful, add a second, smaller forecast broken down by `member_casual` to see whether member and casual usage are expected to trend differently.

---

### Step 3 — Build or Finalise an AI Insights Page (30 mins)

Create a new page named **AI Insights** (or add to an existing page if it fits better).

Place the Key Influencers visual here in its finished, formatted state — clear title, one sentence of interpretation as a text box.

If the Decomposition Tree earned its place in Step 1, add it here too, with the same drill order used in Block 4 (`member_casual` → station → day of week).

---

### Step 4 — Set Personal Goals for Going Deeper (10 mins)

Write a short personal goals note covering:

- One technical skill from Weeks 2 and 3 you specifically want to apply well as you extend this dashboard
- One thing about forecasting or AI visuals you want to get more confident with through deliberate repetition, rather than just having tried it once
- What "done well" would look like for you personally by the end of this extension, separate from the official completion checklist

---

## Completion Checklist

Before marking this session complete, confirm you have done each of the following:

- [ ] Written a short audience profile and compressed story spine
- [ ] Completed the Power BI readiness check and exported two to three visuals
- [ ] Built a five to six slide Canva deck and exported it as PDF
- [ ] Run through the short presentation and confirmed it lands at five to seven minutes
- [ ] Delivered the presentation and written both closing reflection answers
- [ ] Written plain-language definitions of forecasting, Key Influencers, and Decomposition Tree
- [ ] Applied a forecast to the monthly trend chart and recorded observations
- [ ] Tried at least one AI visual and recorded what it revealed
- [ ] Decided which Block 4 visuals become permanent additions to the dashboard
- [ ] Built a formatted Forecast page
- [ ] Built or finalised an AI Insights page
- [ ] Written personal goals for going deeper on Capital Bikeshare
- [ ] Saved all final files

---

## Files To Save

Save the following to `/Documents/Dataskools/Week3_Day5/`

| File | Description |
|---|---|
| `W3D5_PowerBI.pbix` | Capital Bikeshare report and dashboard, presentation-ready, extended with Forecast and AI Insights pages |
| `W3D5_Presentation.pdf` | Short Canva slide deck for the closing presentation |
| `W3D5_Notes.docx` | Story spine, closing reflection, forecasting and AI visual notes, and personal goals for going deeper on Capital Bikeshare |
| `Exports/` | Folder containing PNG visual exports used in the Canva deck |
