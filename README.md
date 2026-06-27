# 🏏 Cricket Best 11 — T20 World Cup 2022 | Power BI Dashboard

A data analytics project that scrapes real cricket statistics from **ESPN Cricinfo** for the **ICC T20 World Cup 2022** and uses **Power BI** to analyze player performance and select the **Best Playing 11** based on data-driven insights.

---

## 📌 Project Overview

Selecting the best cricket team is often based on opinions and gut feeling. This project takes a **data-driven approach** — scraping real match statistics from ESPN Cricinfo, cleaning and transforming the data, and building an interactive Power BI dashboard that evaluates every player's performance to recommend the optimal Best 11 for the T20 World Cup 2022.

---

## 🏆 Dashboard Pages

The Power BI report is divided into **9 interactive pages**, each focused on a specific player role:

| Page | Role | Purpose |
|---|---|---|
| **Power Hitters** | Openers | Analyze aggressive top-order batters with high strike rates |
| **Anchors / Middle Order** | Middle Order | Evaluate consistent run-scorers who stabilize the innings |
| **Finisher / Lower Order Anchor** | Finishers | Find players who accelerate at the death overs |
| **All Rounders / Lower Middle Order** | All Rounders | Assess players contributing in both batting and bowling |
| **Specialist Fast Bowlers / Tail End** | Bowlers | Rank bowlers by economy, wickets, and dot ball percentage |
| **Final 12** | Best XI Selection | Final recommended team based on all role analyses |
| **Batters — Player Details by Match** | Deep Dive | Match-by-match batting breakdown for selected players |
| **All Rounder / Low** | Deep Dive | Detailed all-rounder stats per match |
| **Bowler — Player Details by Match** | Deep Dive | Match-by-match bowling breakdown for selected players |

---

## 📊 Key Metrics Analyzed

### Batting Metrics
| Metric | Description |
|---|---|
| **Batting Average** | Runs scored per dismissal |
| **Strike Rate** | Runs scored per 100 balls faced |
| **Boundary %** | Percentage of runs scored in fours and sixes |
| **Batting Position** | Order at which the player bats |
| **Innings Batted** | Total innings played |

### Bowling Metrics
| Metric | Description |
|---|---|
| **Bowling Economy** | Runs conceded per over |
| **Bowling Strike Rate** | Balls bowled per wicket taken |
| **Dot Ball %** | Percentage of dot balls bowled |
| **Wickets Taken** | Total wickets in the tournament |
| **Bowling Average** | Runs conceded per wicket |

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| **ESPN Cricinfo** | Data source — T20 WC 2022 match scorecards |
| **Python** | Web scraping the match data from ESPN |
| **pandas** | Data cleaning and transformation |
| **Power BI Desktop** | Dashboard building and visualizations |
| **Power Query** | Data loading and preprocessing inside Power BI |
| **DAX** | Custom measures and calculated columns |
| **Custom Visuals** | Image viewer (player photos), InfoRiver, Bar Chart with Top N |

---

## 🔍 Player Role Selection Criteria

### Power Hitters (Openers)
- Batting Average > 30
- Strike Rate > 140
- Innings Batted > 3
- Boundary % > 50%
- Batting Position < 4

### Anchors / Middle Order
- Batting Average > 40
- Strike Rate > 125
- Innings Batted > 3
- Avg. Balls Faced > 20
- Batting Position > 2

### Finishers / Lower Order Anchors
- Batting Average > 25
- Strike Rate > 130
- Innings Batted > 3
- Avg. Balls Faced > 12
- Batting Position > 4

### All Rounders
- Batting Average > 15
- Strike Rate > 140
- Innings Batted > 2
- Wickets > 2
- Bowling Economy < 7
- Bowling Strike Rate < 20

### Specialist Fast Bowlers
- Innings Bowled > 4
- Dot Ball % > 40%
- Bowling Economy < 7
- Bowling Average < 16
- Bowling Strike Rate < 16

---

## 📁 Project Structure

```
cricket-best-11-t20wc-2022/
│
├── Cricket_Best_11.pbix        # Main Power BI dashboard file
├── data/
│   ├── batting_summary.csv     # Scraped batting statistics
│   ├── bowling_summary.csv     # Scraped bowling statistics
│   ├── match_results.csv       # T20 WC 2022 match results
│   └── players_info.csv        # Player metadata (country, role, image)
├── scraping/
│   └── espn_scraper.py         # Python script to scrape ESPN Cricinfo
└── README.md
```

---

## ⚙️ How to Run

### Step 1 — Scrape the Data
```bash
pip install pandas requests beautifulsoup4
python scraping/espn_scraper.py
```
This generates the CSV files in the `data/` folder.

### Step 2 — Open Power BI
- Open `Cricket_Best_11.pbix` in **Power BI Desktop**
- If prompted, update the data source path to your local `data/` folder
- Click **Refresh** to reload the data

### Step 3 — Explore the Dashboard
- Use the **role buttons** on each page to navigate between player categories
- Click on any player in the table to see their **match-by-match breakdown**
- Check the **Final 12** page for the recommended Best XI

---

## 📈 Visuals Used in Dashboard

| Visual Type | Used For |
|---|---|
| **Card** | KPI metrics (avg, strike rate, economy) |
| **Area Chart** | Performance trends across matches |
| **Scatter Chart** | Strike Rate vs Batting Average comparison |
| **Table** | Player stats with sortable columns |
| **Slicer** | Filter by team/country |
| **Image Visual** | Player photos |
| **Bar Chart with Top N** | Top performers ranking |
| **Action Buttons** | Page navigation between role categories |

---

## 🏅 Final Best 11 Selection

The **Final 12** page of the dashboard displays the recommended playing XI selected purely based on the statistical criteria above across all five roles:

- 2 Power Hitters (Openers)
- 3 Anchors / Middle Order
- 1 Finisher
- 2 All Rounders
- 3 Specialist Fast Bowlers

---

## 👤 Author

**Muhammad Usman**  
BS Computer Science — University of Karachi  
IBM Data Analyst Certified  
[GitHub](https://github.com/UsmanAdil18) • [LinkedIn](https://www.linkedin.com/in/muhammad-usman-72a03241a/)

---

## 📄 Data Source

All cricket statistics are sourced from **[ESPN Cricinfo](https://www.espncricinfo.com/)** — ICC Men's T20 World Cup 2022 scorecards and player profiles.
