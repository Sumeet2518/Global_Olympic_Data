# Olympic Sports Performance Analysis (1992–2026)

A comprehensive data analysis and visualization project built in Tableau, exploring historical Olympic trends, country dominance, medal distributions, athlete participation, and sport-specific insights.

---

## 📋 Table of Contents
1. [Project Overview](#-project-overview)
2. [Datasets Used & Data Architecture](#-datasets-used--data-architecture)
3. [Key Performance Indicators & Visualizations](#-key-performance-indicators--visualizations)
4. [Dashboard Architecture](#-dashboard-architecture)
5. [Story Presentation Flow](#-story-presentation-flow)
6. [Key Insights & Findings](#-key-insights--findings)
7. [How to View and Use This Project](#-how-to-view-and-use-this-project)

---

## 🎯 Project Overview
The **Olympic Sports Performance Analysis** project provides a deep dive into modern Olympic history spanning from 1992 to 2026. The objective is to uncover patterns in athletic participation, country-level medal efficiency, sport popularity, and the performance impact of host nations. 

Built entirely using Tableau Public, the project incorporates advanced data relationships, custom calculations, and multi-sheet interactive dashboards structured into a cohesive presentation story.

---

## 🗄️ Datasets Used & Data Architecture
The project integrates four primary relational datasets connected seamlessly inside Tableau:

1. **`alltime_country_rankings.csv`**: Aggregated country statistics including total gold, silver, bronze, overall points, and efficiency percentages.
2. **`medal_results.csv`**: Event-level medal breakdowns containing host details, sport categories, and year information.
3. **`athletes.csv`**: Participant-level demographics including gender, age at peak, training hours, and athlete counts.
4. **`games_summary.csv`**: Historical metadata for Olympic games categorized by year and season.

### **Data Relationships (Model Structure)**
- `alltime_country_rankings.csv` linked to `medal_results.csv` via **`Country`**.
- `medal_results.csv` linked to `athletes.csv` via **`Noc Code`**.
- `medal_results.csv` linked to `games_summary.csv` via composite keys: **`Year`** and **`Season`**.

---

## 📊 Key Performance Indicators & Visualizations
The analysis comprises 8 core worksheets structured into analytical categories:

1. **Medals Performance Over Time (Line Chart)**: Tracks total medals awarded across Olympic cycles from 1992 to 2026.
2. **Top Countries by Total Medals (Bar Chart)**: Highlights dominant nations sorted in descending order of total medal counts.
3. **Medal Breakdown by Type (Grouped Bar Chart)**: Compares Gold, Silver, and Bronze distributions across leading nations.
4. **Athlete Participation Trends (Line Chart)**: Visualizes the growth and fluctuation of participating athletes over the years.
5. **Top Sports by Medals (Horizontal Bar Chart)**: Identifies which sports award the highest volume of total medals.
6. **Host Country Performance (Bar Chart)**: Evaluates the "host nation advantage" in terms of medals won when hosting the games.
7. **Medal Efficiency by Country (Bar Chart)**: Analyzes efficiency metrics to measure conversion rates of participation into podium finishes.
8. **Top Sports by Gold Medals (Horizontal Bar Chart)**: Pinpoints sports leading in elite gold medal distribution.

---

## 🖥️ Dashboard Architecture
The worksheets are consolidated into two interactive executive dashboards:

- **Dashboard 1 - Olympic Overview**: Focuses on macro trends, timeline progression, country rankings, medal composition, and athlete participation metrics.
- **Dashboard 2 - Sports & Country Insights**: Highlights sport popularity, gold medal distribution, host country performance advantages, and national medal efficiency rankings.

---

## 📖 Story Presentation Flow
An interactive presentation story titled **"Olympic Performance Story"** guides stakeholders through the findings:
- **Slide 1**: Overview of historical Olympic trends and macro performance indicators.
- **Slide 2**: Deep dive into country domination, sport rankings, efficiency metrics, and host advantages.

---

## 💡 Key Insights & Findings
- **Country Dominance**: Traditional powerhouse nations consistently secure the highest volume of total medals, led heavily by consistent performances in core sports like Gymnastics and Track & Field.
- **Host Nation Advantage**: Host countries experience a statistically significant surge in medal counts during the years they host the Olympic games.
- **Participation Growth**: Athlete turnout scales progressively with each quadrennial cycle, reflecting the expansion of global sports categories and inclusion events.

---

## 🚀 How to View and Use This Project
1. **Tableau Public Link**: Access the live interactive dashboard online via [Tableau Public Profile Link].
2. **Local Execution**: Download the `.twbx` packaging file and open it using Tableau Desktop or Tableau Reader.