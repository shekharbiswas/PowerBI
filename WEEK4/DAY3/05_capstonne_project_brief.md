# 📊 Power BI Project: Ridership Trends and Station Insights

Imagine we've just joined Capital Bikeshare's analytics team.
Management wants a dashboard that shows how the system is performing — and we're in charge of building it. 🚲📊

This project simulates exactly that — with a twist that happens constantly in real analyst work: we're not starting from nothing. We already have a working model from earlier this week — daily ridership, weather, a date table, a forecast. What we don't have yet is trip-level detail: individual rides, stations, routes. Today we add that in, onto what already exists, and answer questions like:

- Which stations and routes are busiest?
- How does ridership split between members and casual riders?
- Is ridership increasing month by month?
- Which stations bring the most trips into the system?

We'll learn how to bring a new, more granular data source into an existing model without breaking what's already built. By the end, we'll have a one-page executive dashboard that looks professional and tells a clear story.
This is our capstone — the closest thing in this programme to a real, unguided client assignment.

<br>

## 🎯 Project Goal

Extend the existing Capital Bikeshare model with trip-level detail to cover:

- Ridership trends over time (already built — we'll reuse it)
- Busiest stations and routes (new)
- Member vs. casual rider mix (new)
- Key metrics like total rides, average ride duration, and member share (new)

<br>

## 🧰 Dataset

We already have Capital Bikeshare's daily ridership and weather data, joined and modelled, covering **2019 through June 2026**, in `W4D2_PowerBI.pbix`. Today we add a new source: individual trip records at the same date range, giving us the station- and route-level detail the daily aggregate never had.

📦 **Capital Bikeshare Trip History (CSV, by month) — new for today**
🔗 Source: Capital Bikeshare's public system data archive

Columns include:
- `ride_id`
- `rideable_type`
- `started_at`
- `ended_at`
- `start_station_name`
- `start_station_id`
- `end_station_name`
- `end_station_id`
- `start_lat`, `start_lng`
- `end_lat`, `end_lng`
- `member_casual`

<br>

## 🧩 Learning Objectives

By the end of this project, we will be able to:

✅ Import and clean real-world messy trip data
✅ Use Power Query to remove nulls, fix types, and create new columns
✅ Create a **date table** and build time intelligence
✅ Use measures (DAX) for Total Rides, Avg Ride Duration, Member Share
✅ Build visuals like bar charts, line charts, tables, slicers
✅ Publish and present a well-structured ridership dashboard

---

## ⏳ Time Breakdown (8 Hours)

| Step | Task | Tools | Time |
|------|------|-------|------|
| 1 | 🧼 Data Cleaning & Prep | Power Query | 2 hrs |
| 2 | 🧠 Data Modeling | Relationships, Date Table | 1 hrs |
| 3 | 📊 Measure Creation (DAX) | Rides, Duration, Member Share | 1 hr |
| 4 | 📈 Visualization | Charts, Filters, KPIs | 2 hrs |
| 5 | 🎤 Polishing + Story | Titles, tooltips, layout | 1 hr |
| 6 | 🌍 Export & Reflection | Save, publish, present insights | 1 hr |

> Please plan more hours as this is just an estimation

<br>

## 🔧 Step-by-Step Instructions

### 🔹 1. Load and Clean the New Trip-Level Data (1.5 hours)

- Open `W4D2_PowerBI.pbix` and import the monthly trip history CSVs as a new table alongside the existing daily ridership and weather tables
- Remove rows where `start_station_name`, `start_station_id`, or `ride_id` is null
- Filter out invalid trips: remove rows where ride duration is zero, negative, or implausibly short (likely a false start or system test ride)
- Change data types:
  - `started_at`, `ended_at` → Date/Time
  - `start_lat`, `start_lng`, `end_lat`, `end_lng` → Decimal number
- Create a new column in Power Query:
  `RideDurationMinutes = Duration.TotalMinutes([ended_at] - [started_at])`

<br>

### 🔹 2. Connect It to the Existing Date Table (0.5 hours)

- We already have a Date table from earlier this week — don't build a second one
- Add a whole-date column on the new Trips table (`started_at` truncated to a date, no time) so it can relate cleanly to the existing Date table
- Create relationship: Trips[date key] → Date[Date]
- Confirm the model diagram now shows **two fact tables** — daily ridership and Trips — both relating to the same Date table, rather than to each other directly

### 🔹 3. Create Key Measures (1 hour)

```DAX
Total Rides = COUNTROWS('Trips')
Avg Ride Duration = AVERAGE('Trips'[RideDurationMinutes])
Member Ride % = DIVIDE(CALCULATE([Total Rides], 'Trips'[member_casual] = "member"), [Total Rides])
```

Optional

```DAX
Top Station Rides =
      CALCULATE([Total Rides], FILTER(ALL('Trips'), 'Trips'[start_station_name] = "Union Station"))
```

<br>

### 🔹 4. Build Visuals (2 hrs)

On a single Power BI report page, include:

- 📈 **Line chart** → Monthly ridership trend
- 📊 **Bar chart** → Top 10 stations by rides
- 🌍 **Map** → Rides by station location, using `start_lat` / `start_lng`
- 🚲 **Table** → Top 10 start-to-end station routes by ride count
- 🔢 **Cards** → Total Rides, Avg Ride Duration, Member Ride %
- 🎛️ **Slicers** → Date, member_casual, rideable_type

<br>

### 🔹 5. Polish Dashboard (0.5 hr)

- Add clear report title
- Use consistent color scheme and layout
- Add tooltips and labels where helpful
- Include our name and date in footer
- *Optional*: use themes or custom fonts

---

### 🔹 6. Export & Reflect (0.5 hr)

- Export as PDF or publish to Power BI Service
- Take 2–3 screenshots of the final dashboard
- Answer these reflection prompts:

**🧠 Reflection**
- What was the most fun part?
- What part was hardest?
- What would we improve next time?

<br>

## 📁 Deliverables

- `.pbix` Power BI file
- Screenshots of final dashboard
- Written analysis report (5 - 8 slides in Google Slides — Canva is fine too)

🕔 **Submission Deadline**: Friday evening by midnight.

<br>

## 🏁 What We'll Practice

- End-to-end data cleaning and transformation on genuinely raw source files
- Operational metric creation using DAX
- Insightful and interactive dashboard design
- Project presentation and real-world thinking

<br>

## 🧠 Bonus Challenges (Optional)

- Add a Month-over-Month % change in ridership
- Rejoin the weather data from Week 4 Day 1 and add it as a slicer or influencer on this fresh build
- Build a tooltip report page
- Add slicer bookmarks for dynamic filtering
- Use KPIs or gauge visuals for performance metrics

<br>

Good luck — and have fun exploring the operational side of data with Power BI! 🚀