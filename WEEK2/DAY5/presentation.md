# Task Sheet — Presentation Day: Capital Bikeshare ETL Project

**Dataskools | Power BI Programme**
Estimated Time: 6 Hours | Tools: Power BI + Canva | Data: Capital Bikeshare Pipeline (W2D4)

---

## How This Day Is Structured

| Block | Activity | Time |
|---|---|---|
| Block 1 | Presentation Planning + Story Structure | 1 Hour |
| Block 2 | Power BI Report Build | 2 Hours |
| Block 3 | Canva Slide Deck Build | 2 Hours |
| Block 4 | Rehearsal, Review and Final Handoff | 1 Hour |

> **Note on today:** The ETL pipeline is done. Today the work becomes visible. A clean pipeline that cannot be communicated is not yet finished — the final deliverable is always what the audience understands, not what the file contains. Today you build two outputs: a Power BI report that lets someone explore the data, and a Canva slide deck that tells someone what the data means. These are different jobs. Keep them separate in your thinking throughout.

---

## Block 1 — Presentation Planning and Story Structure (1 Hour)

### Context

Before opening Power BI or Canva, plan what you are presenting and to whom. The most common mistake in data presentations is building visuals first and finding the story later. The story comes first. The visuals serve it.

---

### Step 1 — Define Your Audience (15 mins)

Write the following in your notes before anything else:

**Who is this presentation for?**

Choose one of the following audience profiles and write it at the top of your notes. Every decision today — which visuals to build, how much technical detail to include, what to put in the slide deck versus the Power BI report — flows from this choice.

- **Option A — Internal analyst handoff:** A data modeller or analyst who will work with the pipeline next week. They care about data structure, known limitations, and what is ready versus what is not.
- **Option B — Programme stakeholder:** A programme manager or course assessor who wants to understand what was built, why decisions were made, and what the data shows about Capital Bikeshare usage.
- **Option C — General audience:** Someone with no data background who wants to understand what the Capital Bikeshare data reveals about how people use the bike share system.

Record in your notes:

- Which audience you chose and why
- What they already know coming in
- What one thing they must leave understanding that they did not know before

---

### Step 2 — Build Your Story Spine (25 mins)

A data presentation has a spine — a sequence of points that build on each other. Write yours before touching any tool.

Complete each of the following in your notes in full sentences:

**The situation:**
What is Capital Bikeshare? What data exists and what does it cover? Why does it matter to look at this data?

**The pipeline:**
What was built across the week? What are the three sources? What does the pipeline do that raw data alone cannot? Keep this to two or three sentences — the audience cares about the output more than the process.

**The findings:**
What does the data actually show? Write three to five specific findings you expect the Power BI report to surface. These might include peak usage times, member vs casual rider patterns, station demand, trip duration distributions, or weather impact if you included a weather source. You do not need to have built the visuals yet — write what you expect to find based on what you already know about the data.

**The limitations:**
What does the data not show? What did the pipeline exclude, approximate, or leave unresolved? A presentation that acknowledges limitations is more credible than one that does not.

**The next step:**
What would a stakeholder or analyst do with this work next? Data modelling, deeper segmentation, a live dashboard, a policy recommendation — what is the logical continuation?

> The story spine is not the slide deck structure. It is the thinking underneath it. Once the spine is clear, the slides and visuals become decisions rather than guesses.

---

### Step 3 — Plan Both Outputs (20 mins)

You are building two things today. Plan them separately.

**Power BI report plan — write in your notes:**

- How many report pages will the report have?
- What is the purpose of each page — exploration, summary, detail, or comparison?
- Which visuals will appear on each page and what question does each visual answer?
- Which slicers or filters will the report include?
- What is the single most important visual in the report — the one that answers the central question?

**Canva slide deck plan — write in your notes:**

- How many slides will the deck have?
- What is the flow — title, context, pipeline overview, findings, limitations, next steps?
- Which Power BI visuals will be exported and embedded in the slides?
- What will be written text versus visual on each slide?
- What is the one slide that must land — the one the audience will remember?

> A report and a slide deck are not the same thing. A report lets someone explore. A slide deck argues a point. Design them with that difference in mind.

---

## Block 2 — Power BI Report Build (2 Hours)

### Context

Open `W2D4_PowerBI.pbix` from `/Documents/Dataskools/Week2_Day4/`

Save immediately as `W2D5_PowerBI.pbix` in `/Documents/Dataskools/Week2_Day5/`

Build the report against the plan written in Block 1. Every visual should answer a specific question. If you cannot state the question a visual answers, remove it.

---

### Step 1 — Set Up Report Pages (20 mins)

Create the pages planned in Block 1. Name each page clearly — not "Page 1" but the question or topic it addresses.

Suggested page structure for the Capital Bikeshare project:

| Page | Purpose | Example Title |
|---|---|---|
| Overview | High-level summary of the dataset | "Capital Bikeshare — Usage Overview" |
| Rider Patterns | Member vs casual comparison | "Who Is Riding?" |
| Station Demand | Top and bottom stations by trip volume | "Where Are People Going?" |
| Trip Duration | Distribution and outliers | "How Long Are Trips?" |
| Context Layer | Weather or date dimension findings | "When and Why?" |

Adjust the pages to match your story spine and your chosen third source. You do not need five pages — three focused pages are better than five unfocused ones.

---

### Step 2 — Build Core Visuals (60 mins)

For each page, build the visuals planned in Block 1. Follow these standards throughout:

**Every visual must:**

- Have a clear, specific title that states what it shows — not "Trip Count" but "Total Trips by Month, Member vs Casual"
- Use consistent colour for the same categories across all pages — if member riders are blue on page two, they are blue everywhere
- Have axis labels that are readable without zooming
- Be sized so the most important visual on the page is the largest

**Suggested visuals by page:**

**Overview page:**
- Card visuals for total trips, total unique stations, date range covered, and average trip duration
- A bar or column chart showing trips by month
- A donut or bar chart showing member vs casual split

**Rider Patterns page:**
- A clustered bar chart comparing member vs casual by time of day or day of week
- A line chart showing trip volume over time split by member type
- A slicer for member type to allow filtered exploration

**Station Demand page:**
- A bar chart of top 10 start stations by trip volume
- A bar chart of top 10 end stations by trip volume
- A map visual if station latitude and longitude are available in the data

**Trip Duration page:**
- A histogram or binned bar chart of trip duration distribution
- A card showing average and median trip duration
- A scatter or bar chart comparing duration by member type

**Context Layer page:**
- If using a date dimension: trips by day of week, trips by month with a time intelligence comparison
- If using weather data: trips vs temperature or precipitation where available
- A slicer for the date or weather dimension

---

### Step 3 — Apply Report Formatting (25 mins)

Once all visuals are built, apply consistent formatting across the report.

**Canvas and theme:**

- Set a consistent background colour across all pages — light grey or white works cleanly for a professional report
- Apply a report theme that sets consistent font, colour palette, and visual style. Power BI Desktop includes built-in themes under **View > Themes**
- Ensure all text is readable at standard screen size without zooming

**Visual consistency check — go through every visual and confirm:**

- Font size is consistent across titles, axis labels, and data labels
- Colours match the plan — same category, same colour, every page
- No visual has a default "Sum of Column" title remaining
- No axis label is truncated or overlapping

**Interactivity check:**

- Click each slicer and confirm it filters all visuals on the page as expected
- Click a bar or segment in one visual and confirm cross-filtering updates other visuals correctly
- If any cross-filter behaviour is unintended, adjust interactions via **Format > Edit Interactions**

---

### Step 4 — Export Visuals For Canva (15 mins)

Before closing Power BI, export the visuals you plan to embed in the Canva slide deck.

To export a visual as an image:

- Right-click the visual
- Select **Export** then **Export to image** (PNG)
- Save each export to `/Documents/Dataskools/Week2_Day5/Exports/` with a clear name — `overview_trip_count.png`, `rider_patterns_member_casual.png`

Record in your notes which visuals you exported and which slide each one belongs to. Aim to export three to five visuals — enough to anchor the slide deck without making it a copy of the report.

---

## Block 3 — Canva Slide Deck Build (2 Hours)

### Context

Open Canva and create a new presentation. Use a 16:9 format. Do not start from a blank slide — choose a clean, professional template as the base and modify it rather than building from scratch.

The slide deck is not a replica of the Power BI report. It is a curated argument built from the data. Choose what to include based on what your audience needs to understand, not what you built.

---

### Step 1 — Set Up The Deck Structure (20 mins)

Create one slide for each section of your story spine. At minimum the deck should include:

| Slide | Content |
|---|---|
| 1 | Title slide — project name, your name, date |
| 2 | Context — what is Capital Bikeshare and what does this data cover |
| 3 | What was built — the pipeline in plain language, not technical detail |
| 4–6 | Findings — one key finding per slide, with a supporting visual |
| 7 | Limitations — what the data does not show |
| 8 | Next steps — what would follow from this work |
| 9 | Close — a single sentence summary or call to action |

Adjust the number of findings slides based on your story spine. Three findings slides with one strong visual each is better than six slides with weak ones.

---

### Step 2 — Build Each Slide (70 mins)

Work through each slide in sequence. Follow these standards:

**Title slide:**

- Project name: *Capital Bikeshare ETL Project — Week 2 Final*
- Your name and the programme name
- A simple, clean background — avoid stock photos on a data project title slide

**Context slide:**

- Two to three sentences maximum on what Capital Bikeshare is
- The date range and volume of the data — total trips, months covered, sources used
- No visuals needed here — this is orientation, not analysis

**Pipeline slide:**

- Describe the three sources in plain language
- Use a simple diagram or three-column layout — Source → Staging → Reporting
- One sentence on what the pipeline enables that raw data alone does not
- Avoid Power Query screenshots — the audience does not need to see the tool

**Findings slides — one per finding:**

- A headline at the top that states the finding as a sentence, not a label. Not "Trip Volume" but "Member riders account for 70% of all trips and are more consistent across the week"
- The exported Power BI visual embedded below the headline
- One to two sentences of interpretation beneath the visual — what does this mean, not just what does it show
- No more than one visual per slide

**Limitations slide:**

- Three to five bullet points maximum
- Each limitation stated plainly — what the data does not cover, what was approximated, what is known to be incomplete
- Do not apologise for limitations. State them as information, not failure.

**Next steps slide:**

- Two to three concrete next steps — data modelling, deeper segmentation, a live dashboard, a policy use case
- Each written as an action, not a vague direction. Not "further analysis" but "build a date intelligence model to compare month-on-month growth by rider type"

**Close slide:**

- One sentence that captures the value of the work
- Your contact or the Dataskools programme name
- Keep it simple

---

### Step 3 — Apply Design Standards (30 mins)

Once all slides are built, apply consistent design across the deck.

**Typography:**

- Use a maximum of two fonts — one for headings, one for body text
- Heading size: 28–36pt. Body text: 16–20pt. Caption or label text: 12–14pt
- Do not use more than three font sizes across the deck

**Colour:**

- Choose a palette of three colours — one primary, one accent, one neutral
- Use the primary colour for headings and key data points
- Use the accent colour sparingly — for one highlight per slide at most
- The neutral is for body text and backgrounds

**Consistency check — go through every slide and confirm:**

- All headings are the same font, size, and colour
- All body text is the same font and size
- All embedded visuals are the same width and aligned to the same grid
- No slide has more than three distinct elements competing for attention
- No slide is more than 40% text

**Export:**

- Download the final deck as PDF from Canva — **Share > Download > PDF Standard**
- Save to `/Documents/Dataskools/Week2_Day5/` as `W2D5_Presentation.pdf`

---

## Block 4 — Rehearsal, Review and Final Handoff (1 Hour)

### Context

A presentation that has not been rehearsed is a draft. This block is for making it finished.

---

### Step 1 — Talk Through The Deck (20 mins)

Open the PDF export of the slide deck and present it out loud — to yourself, to a timer, or to someone else if available.

For each slide, say out loud:

- What this slide shows
- Why it matters to the audience
- What the next slide will cover

Record in your notes:

- Which slides felt unclear when spoken — where did you hesitate or over-explain?
- Which slides had too much on them — where did you run out of things to say before you ran out of slide?
- Which transition between slides felt abrupt — where did the story skip rather than flow?

Go back and fix the top two issues before moving on.

---

### Step 2 — Report Review (20 mins)

Open `W2D5_PowerBI.pbix` and review the report against the following:

**Navigation:**

- Can someone who has never seen the report find what they are looking for within 30 seconds?
- Is the page order logical — does overview come before detail?
- Are the page names descriptive enough to navigate without reading every visual?

**Accuracy check:**

- Open the row count validation table from `W2D4_Notes.docx`
- Confirm the totals shown in the report card visuals match the validated row counts from Day 4
- If any number does not match — investigate before signing off

**Slicer check:**

- Set every slicer to its default state
- Confirm no slicer is left in a filtered state that would confuse the first person to open the report

---

### Step 3 — Reflection Questions (20 mins)

Write minimum two to three sentences per answer.

**Q1 — Story vs Data:**
The slide deck tells a story and the Power BI report shows the data. Describe one moment today where you had to choose what to leave out. What did you cut and why?

**Q2 — Audience Impact:**
Looking at the finished slide deck with your chosen audience in mind — what would they understand after seeing it that they did not know before? What is still unclear or missing for that audience specifically?

**Q3 — The Gap Between Building and Presenting:**
The ETL pipeline took four days to build. The presentation took one. Describe the difference in the type of thinking required. Which was harder and why?

---

## Completion Checklist

Before marking this session complete, confirm you have done each of the following:

- [ ] Written audience profile and story spine in notes before opening any tool
- [ ] Planned both outputs — Power BI report pages and Canva slide structure — before building
- [ ] Created and named all report pages in Power BI
- [ ] Built all planned visuals with correct titles, consistent colours, and readable formatting
- [ ] Applied a consistent theme and formatting pass across the full report
- [ ] Confirmed slicer and cross-filter interactivity works correctly
- [ ] Exported three to five visuals as PNG for Canva embedding
- [ ] Built all slides in Canva following the story spine
- [ ] Each findings slide has a headline stating the finding, an embedded visual, and an interpretation sentence
- [ ] Applied consistent typography and colour across the full deck
- [ ] Exported the deck as PDF and saved to the correct location
- [ ] Talked through the deck out loud and fixed the top two issues identified
- [ ] Confirmed Power BI report totals match the W2D4 validated row counts
- [ ] Written full answers to all three reflection questions
- [ ] Saved all final files

---

## Files To Save

Save the following to `/Documents/Dataskools/Week2_Day5/`

| File | Description |
|---|---|
| `W2D5_PowerBI.pbix` | Completed Power BI report with all pages, visuals, slicers, and consistent formatting |
| `W2D5_Presentation.pdf` | Canva slide deck exported as PDF — full story from context through findings to next steps |
| `W2D5_Notes.docx` | Audience profile, story spine, presentation plan, rehearsal notes, and all three reflection answers |
| `Exports/` | Folder containing all PNG visual exports from Power BI used in the Canva deck |