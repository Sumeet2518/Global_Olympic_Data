# 🏅 Global Olympic Sports Performance Analysis (1992–2026)

[![Tableau Public](https://img.shields.io/badge/Tableau_Public-Live_Dashboard-E97627?style=for-the-badge&logo=tableau&logoColor=white)](https://public.tableau.com/views/GlobalOlympicSportsPerformanceAnalysis_17931934959440/Dashboard1-OlympicOverview?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)
[![Project Status](https://img.shields.io/badge/Status-Completed-22c55e?style=for-the-badge)]()
[![Data Source](https://img.shields.io/badge/Datasets-4_Relational_CSVs-3b82f6?style=for-the-badge)]()

An end-to-end data analytics and visualization project built in **Tableau Public** that explores historical Olympic trends, country-level dominance, medal breakdowns, athlete participation patterns, host country advantages, and sport-level efficiency from **1992 to 2026**.

---

## 📂 Repository Folder Structure

This repository is organized systematically across all project lifecycle phases:

```text
📦 Global-Olympic-Sports-Performance-Analysis
 ┣ 📂 1. Ideation Phase               # Problem statement, empathy map & brainstorming docs
 ┣ 📂 2. Requirement Analysis         # Functional/non-functional requirements & data specs
 ┣ 📂 3. Project Design Phase         # Data architecture, ER/schema design & dashboard wireframes
 ┣ 📂 4. Project Planning Phase       # Project charter, milestone schedule & sprint planning
 ┣ 📂 5. Project Development Phase    # Tableau worksheets, calculated fields & dashboard builds
 ┣ 📂 6. Performance Testing          # Data validation, composite relationship checks & QA reports
 ┣ 📂 7.Project Documentation         # Comprehensive project report & technical guides
 ┣ 📂 8.Project Demonstration         # Walkthrough presentation, screenshots & demo assets
 ┣ 📂 Dataset                         # Raw CSV datasets (rankings, medals, athletes, games summary)
 ┣ 📄 Global Olympic Sports Performance.url  # Direct shortcut to the live Tableau Public project
 ┗ 📄 README.md                       # Repository overview and documentation
```

---

## 🔗 Live Interactive Project Links

* **📊 Live Tableau Public Workbook:** [Global Olympic Sports Performance Analysis on Tableau Public](https://public.tableau.com/views/GlobalOlympicSportsPerformanceAnalysis_17931934959440/Dashboard1-OlympicOverview?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)
* **🔗 Quick Shortcut File:** Click on `Global Olympic Sports Performance.url` in the root directory to launch the visualization directly.

---

## 🗄️ Datasets & Relational Data Model (`/Dataset`)

The project integrates **4 relational CSV datasets** located in the `Dataset` folder using Tableau's Logical Relationship Layer:

| Dataset File | Description | Key Fields |
| :--- | :--- | :--- |
| **`alltime_country_rankings.csv`** | Aggregated country standings across Olympic history | `Country`, `Noc Code`, `Total Medals`, `Total Gold`, `Total Silver`, `Total Bronze`, `Avg Efficiency Pct` |
| **`medal_results.csv`** | Event-level and cycle-level medal results & host info | `Year`, `Season`, `Host City`, `Host Country`, `Country`, `Noc Code`, `Total Medals`, `Medal Efficiency Pct` |
| **`athletes.csv`** | Participant demographics, sports & individual metrics | `Athlete Id`, `Name`, `Gender`, `Sport`, `Sport Category`, `Noc Code`, `Age At Peak`, `Training Hours` |
| **`games_summary.csv`** | Macro metadata for each Summer and Winter Olympic cycle | `Year`, `Season`, `Participating Nations`, `Total Athletes`, `Total Medals Awarded` |

### **Validated Data Relationships**
1. `alltime_country_rankings.csv` ↔ `medal_results.csv` joined on **`Country = Country`**
2. `medal_results.csv` ↔ `athletes.csv` joined on **`Noc Code = Noc Code`**
3. `medal_results.csv` ↔ `games_summary.csv` joined via a **composite multi-field relationship**:
   * **`Year = Year (Games Summary.Csv)`**
   * **`Season = Season (Games Summary.Csv)`**

---

## 📈 Core Visualizations (8 Validated Worksheets)

1. **Medals Performance Over Time** (`Line Chart`): Tracks total medals awarded across Olympic cycles from 1992 to 2026 (peaking at **363** in 2020 and **358** in 2016).
2. **Top Countries by Total Medals** (`Horizontal Bar Chart`): Ranks dominant nations led by **United States (735)**, **China (696)**, **Russia (429)**, and **Great Britain (401)**.
3. **Medal Breakdown by Type** (`Side-by-Side Bar Chart`): Compares Gold, Silver, and Bronze distributions across leading nations (**USA: 250G / 208S / 277B**, **China: 230G / 230S / 236B**).
4. **Athlete Participation Trends** (`Line Chart`): Visualizes athlete participation across alternating Summer and Winter cycles, peaking at **8,000** athletes in 2020.
5. **Top Sports by Medals** (`Horizontal Bar Chart`): Identifies the highest medal-awarding sports led by **Skateboarding (6,025)**, **Gymnastics (6,025)**, **Fencing (6,025)**, and **Volleyball (5,984)**.
6. **Host Country Performance** (`Horizontal Bar Chart`): Evaluates host nation performance counts led by **Japan (105)**, **United States (100)**, **China (98)**, and **Italy (93)**.
7. **Medal Efficiency by Country** (`Horizontal Bar Chart`): Ranks countries by cumulative Medal Efficiency Percentage led by **Iran (1,032.1)**, **Latvia (1,015.0)**, and **Poland (986.3)**.
8. **Top Sports by Gold Medals** (`Horizontal Bar Chart`): Highlights sports awarding the highest number of Gold medals (**Skateboarding, Gymnastics & Fencing at 1,959 Golds each**).

---

## 🖥️ Dashboards & Story Presentation

* **Dashboard 1 - Olympic Overview**: Consolidates Sheets 1–4 into an automatic-sizing 2×2 executive grid covering historical medal trends, top countries, medal type breakdowns, and athlete turnout.
* **Dashboard 2 - Sports & Country Insights**: Consolidates Sheets 5–8 into an automatic-sizing 2×2 analytical grid covering top sports by total/gold medals, host country performance, and national medal efficiency.
* **Olympic Performance Story**: A step-by-step interactive narrative built around individual worksheets and dashboards for granular stakeholder presentations.

---

## 🚀 How to Run Locally

1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/your-repo-name.git
   ```
2. Open the **`Dataset`** folder to inspect the raw CSV files, or open `index.html` in any browser to launch the interactive web portfolio.
3. Double-click **`Global Olympic Sports Performance.url`** (or visit the [Tableau Public Link](https://public.tableau.com/views/GlobalOlympicSportsPerformanceAnalysis_17931934959440/Dashboard1-OlympicOverview?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)) to interact with the live cloud workbook.