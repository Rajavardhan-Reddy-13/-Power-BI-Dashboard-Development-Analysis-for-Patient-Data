# 🏥 Power BI Dashboard: Patient Waiting List Analysis

This project demonstrates the **end-to-end development** of an interactive Power BI dashboard using real-world healthcare data focused on **patient waiting lists** from 2018–2021. It covers every stage from requirement gathering to publishing, following industry best practices in **data modeling, transformation, visualization**, and **dashboard deployment**.

---

## 📌 Project Objective

- Track and analyze the **current status** and **historical trends** of patient waiting lists in **Inpatient** and **Outpatient** categories.
- Provide insights by **Specialty** and **Age Profile**.
- Create an interactive, insightful, and visually appealing dashboard with **automated refresh capabilities**.

---

## 🧱 Step-by-Step Workflow

### 1. 📋 Requirement Gathering
- Identified **stakeholders** and their business objectives through meetings.
- Defined KPIs:
  - Average & Median Waiting List
  - Total Wait List by Category (Inpatient/Outpatient)
- Outlined scope, metrics, and deployment timeline.

### 2. 📁 Data Collection
- Source: Publicly available Excel files.
- Method: Imported data using **Folder Connector** in Power BI to enable **automated refresh**.
- Datasets:
  - Inpatient Data
  - Outpatient Data

### 3. 🧹 Data Transformation (Power Query)
Performed in Power BI's Power Query Editor:
- Renamed columns to match schemas.
- Reordered columns.
- Created custom columns (e.g., `Case_Type`).
- **Appended** Inpatient and Outpatient tables into a unified dataset.
- Cleaned values using `Replace` and `Trim`.
- Result: `All_Data` table.

### 4. 🔗 Data Modeling
- Disabled direct load of original tables (Inpatient & Outpatient).
- Created relationships using a **Specialty Mapping** table for grouping specialties.
- Used **Star Schema** modeling to optimize performance.
- Established one-to-many relationships for filtering and lookup.

### 5. 🧠 DAX Measures (Calculated Fields)
Defined DAX calculations for KPIs and interactivity:
- `Latest Month Wait List`
- `PY Latest Month Wait List`
- `Average Wait List`, `Median Wait List`
- `Avg/Med Wait List` (SWITCH based on user selection)
- `Dynamic Title`
- `NoDataLeft`, `NoDataRight` (handle blanks)

### 6. 🎨 Dashboard Layout & Visualization
Designed according to pre-approved **wireframe/blueprint**:
- **Summary Page**:
  - KPI cards
  - Doughnut & column charts
  - Line chart with Case_Type filter
  - Multi-row cards (Top 5 specialties)
- **Detailed Page**:
  - Matrix table for granular analysis (by Date, Age, Specialty, Time Band)
- **Tooltip Page**:
  - Specialty-based tooltip view activated on line chart hover
- **Interactive Slicers**:
  - Archive Date, Specialty, Case Type
  - Calculation Method switch (Average vs. Median)

### 7. ✨ Beautification
- Extracted color palette from reference dashboards using **Adobe Color**.
- Designed background in **PowerPoint/Canva**, saved as `.png`, applied to Power BI canvas.
- Ensured consistent layout using **gridlines and snap-to-grid**.

### 8. 🔁 Interactivity & Navigation
- Added navigation buttons for page switching.
- Enabled dynamic chart titles and tooltip behavior.
- Configured visual header tooltips and alt text for accessibility.

### 9. ✅ Testing & UAT
- Performed User Acceptance Testing (UAT) to identify data or design issues.
- Validated filter behavior, DAX calculations, and navigation.

### 10. ☁️ Sharing & Deployment
- Published to **Power BI Service**.
- Configured **Row-Level Security (RLS)** for stakeholder-specific access.
- Set up **automated monthly refresh** using the folder path.

---

## 📊 Tools & Technologies Used
- **Power BI Desktop**
- **Power Query Editor**
- **DAX (Data Analysis Expressions)**
- **Adobe Color / Canva / PowerPoint**
- **Power BI Service (for publishing & refresh)**

---

## Refereces
- **https://www.youtube.com/watch?v=G8ikAJele_s
- **https://pivotalstats.com/end-end-power-bi-dashboard-development/
