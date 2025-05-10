# 📊 Power BI Project: Sales  Trends and Customer Insights

Imagine you've just joined a fast-growing e-commerce company.  
Your manager wants a dashboard that shows how the business is doing — and you're in charge of building it. 💼📊

This project simulates exactly that. You'll clean messy real-world data, spot trends, and build visuals that answer important questions like:

- What are our best-selling products?  
- Which customers spend the most?  
- Are sales increasing month by month?  
- Which countries bring the most revenue?

You’ll learn how to turn raw data into business insights that your team can actually use.  
By the end, you'll have a one-page executive dashboard that looks professional and tells a clear story.  
This is your first step toward thinking (and working) like a real Power BI analyst.


<br>


## 🎯 Project Goal

Build a dynamic Power BI dashboard for a fictional online retail company to analyze:

- Sales trends over time  
- Top products and customers  
- Regional performance  
- Key metrics like revenue, order count, and average order value

<br>

## 🧰 Dataset

We’ll use a UK based online retail store data from the UCI Machine Learning [Repository](https://archive.ics.uci.edu/dataset/352/online+retail):

📦 **Online Retail Dataset (Excel)**  
🔗 [Download here](https://archive.ics.uci.edu/ml/machine-learning-databases/00352/Online%20Retail.xlsx)

Columns include:
- `InvoiceNo`  
- `StockCode`  
- `Description`  
- `Quantity`  
- `InvoiceDate`  
- `UnitPrice`  
- `CustomerID`  
- `Country`

<br>

## 🧩 Learning Objectives

By the end of this project, you will be able to:

✅ Import and clean real-world messy data  
✅ Use Power Query to remove nulls, fix types, and create new columns  
✅ Create a **date table** and build time intelligence  
✅ Use measures (DAX) for Total Sales, Total Orders, Avg Order Value  
✅ Build visuals like bar charts, line charts, tables, slicers  
✅ Publish and present a well-structured sales dashboard

---

## ⏳ Time Breakdown (8 Hours)

| Step | Task | Tools | Time |
|------|------|-------|------|
| 1 | 🧼 Data Cleaning & Prep | Power Query | 1.5 hrs |
| 2 | 🧠 Data Modeling | Relationships, Date Table | 1 hrs |
| 3 | 📊 Measure Creation (DAX) | Revenue, AOV, Orders | 1 hr |
| 4 | 📈 Visualization | Charts, Filters, KPIs | 2 hrs |
| 5 | 🎤 Polishing + Story | Titles, tooltips, layout | 1 hr |
| 6 | 🌍 Export & Reflection | Save, publish, present insights | 1 hr |

> Please plan more hours as this is just an estimation

<br>

## 🔧 Step-by-Step Instructions

### 🔹 1. Load and Clean Data (1.5 hours)

- Import the Excel file into Power BI  
- Remove rows where `CustomerID`, `InvoiceNo`, or `Description` is null  
- Filter out cancelled transactions: remove rows where `InvoiceNo` starts with “C”  
- Change data types:  
  - `InvoiceDate` → Date/Time  
  - `Quantity`, `UnitPrice` → Whole/Decimal number  
- Create a new column in Power Query:  
  `TotalPrice = Quantity * UnitPrice`

---

### 🔹 2. Create Relationships and Date Table (0.5 hours)

- Add a **Date Table**:
  Use DAX formula:  
  ```DAX
  Date = CALENDAR(MIN('Sales'[InvoiceDate]), MAX('Sales'[InvoiceDate]))
 ```

- Add columns: Year, Month, Month Name (you can use FORMAT or YEAR(), MONTH() functions)
- Create relationship: Sales[InvoiceDate] → Date[Date]
- Mark as official Date Table: Modeling → Mark as Date Table

###🔹 3. Create Key Measures (1 hour)

```
Total Sales = SUM('Sales'[TotalPrice])
Order Count = DISTINCTCOUNT('Sales'[InvoiceNo])
Avg Order Value = [Total Sales] / [Order Count]
```

Optional

```
Top Country Sales = 
      CALCULATE([Total Sales], FILTER(ALL('Sales'), 'Sales'[Country] = "United Kingdom"))
```


### 🔹 4. Build Visuals (2 hrs)

On a single Power BI report page, include:

- 📈 **Line chart** → Monthly sales trend  
- 📊 **Bar chart** → Top 10 products by sales  
- 🌍 **Map or column chart** → Sales by country  
- 👤 **Table** → Top 10 customers by spend  
- 🔢 **Cards** → Total Revenue, Order Count, AOV  
- 🎛️ **Slicers** → Date, Country, Product Name

<br>

### 🔹 5. Polish Dashboard (0.5 hr)

- Add clear report title  
- Use consistent color scheme and layout  
- Add tooltips and labels where helpful  
- Include your name and date in footer  
- *Optional*: use themes or custom fonts

---

### 🔹 6. Export & Reflect (0.5 hr)

- Export as PDF or publish to Power BI Service  
- Take 2–3 screenshots of your dashboard  
- Answer these reflection prompts:

**🧠 Reflection**  
- What was the most fun part?  
- What part was hardest?  
- What would you improve next time?

<br>

## 📁 Deliverables

- `.pbix` Power BI file  
- Screenshots of final dashboard  
- Written reflection (3–5 bullet points)

<br>

## 🏁 What You’ll Practice

- End-to-end data cleaning and transformation  
- Business metric creation using DAX  
- Insightful and interactive dashboard design  
- Project presentation and real-world thinking

<br>

## 🧠 Bonus Challenges (Optional)

- Add a Month-over-Month % change  
- Build a tooltip report page  
- Add slicer bookmarks for dynamic filtering  
- Use KPIs or gauge visuals for performance metrics

<br>

Good luck — and have fun exploring the business side of data with Power BI! 🚀
