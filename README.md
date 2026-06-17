<h1 align="center">🏏 IPL Auction Intelligence System</h1>

<h3 align="center">
Data-Driven Player Valuation & Auction Price Estimation
</h3>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10+-blue?style=for-the-badge&logo=python" />
  <img src="https://img.shields.io/badge/Pandas-Data%20Analysis-green?style=for-the-badge&logo=pandas" />
  <img src="https://img.shields.io/badge/NumPy-Numerical%20Computing-orange?style=for-the-badge&logo=numpy" />
  <img src="https://img.shields.io/badge/Matplotlib-Visualization-red?style=for-the-badge" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Scikit--Learn-Feature%20Engineering-yellow?style=for-the-badge&logo=scikitlearn" />
  <img src="https://img.shields.io/badge/Jupyter-Notebook-orange?style=for-the-badge&logo=jupyter" />
</p>

<h3 align="center">
📊 IPL Player Analytics &nbsp; | &nbsp;
💰 Auction Valuation &nbsp; | &nbsp;
🏆 Cricket Intelligence
</h3>
</div>

---

# 📌 Project Overview

The **IPL Auction Intelligence System** is a Sports Analytics and Data Science project that evaluates IPL players and estimates their potential auction value using historical IPL performance data.

Instead of relying solely on reputation, popularity, or subjective judgment, this system uses a structured performance-based valuation framework to estimate player worth.

The project builds separate valuation models for:

* Specialist Batters
* Specialist Bowlers
* All-Rounders

and converts player performance into estimated IPL auction prices.

---

# 🎯 Business Problem

IPL franchises invest hundreds of crores during player auctions.

One of the biggest challenges is determining:

* Which players are worth investing in?
* Which players are overpriced?
* Which players are undervalued?
* How can franchises objectively compare players?

Traditional player valuation often depends on:

❌ Reputation

❌ Public perception

❌ Recent performances

❌ Subjective decision-making

This project introduces a data-driven player valuation system to support smarter auction decisions.

---

# 🚀 Project Objectives

* Analyze historical IPL player performance
* Create player-level batting and bowling datasets
* Develop separate valuation models for:

  * Batters
  * Bowlers
  * All-Rounders
* Generate performance scores
* Estimate realistic IPL auction values
* Support data-driven franchise decision making

---

# 📂 Dataset Description

The project uses ball-by-ball IPL match data containing:

### Match Information

* Match ID
* Season
* Venue
* City
* Toss Details
* Match Results

### Batting Information

* Batter
* Runs Scored
* Balls Faced
* Strike Rate

### Bowling Information

* Bowler
* Runs Conceded
* Wickets Taken
* Overs Bowled
* Economy Rate

### Team Information

* Batting Team
* Bowling Team
* Match Winner
* Player of the Match

---

# 🧹 Data Cleaning & Preprocessing

Extensive preprocessing was performed before model development.

### Cleaning Activities

✔ Removed duplicate team names

Examples:

* Delhi Daredevils → Delhi Capitals
* Kings XI Punjab → Punjab Kings
* Royal Challengers Bangalore → Royal Challengers Bengaluru

✔ Standardized city names

* Bangalore → Bengaluru

✔ Standardized venue names

✔ Removed inconsistent records

✔ Converted object columns into numerical format

✔ Handled missing values

✔ Created player-level aggregated datasets

✔ Feature engineering for batting and bowling metrics

---

# ⚙️ Feature Engineering

Several performance metrics were created from raw IPL data.

### Batting Metrics

* Total Runs
* Balls Faced
* Strike Rate
* Matches Played

### Bowling Metrics

* Total Wickets
* Runs Conceded
* Balls Bowled
* Overs Bowled
* Economy Rate
* Matches Played

### All-Rounder Metrics

* Batting Performance
* Bowling Performance
* Experience Metrics

---

# 📏 Why MinMax Scaling?

Different performance metrics exist on different numerical scales.

Example:

| Feature     | Range         |
| ----------- | ------------- |
| Runs        | Thousands     |
| Strike Rate | Hundreds      |
| Economy     | Single Digits |
| Wickets     | Hundreds      |

Without normalization, larger values would dominate the valuation process.

Therefore, **MinMax Scaling** was applied to transform all features into a common range between 0 and 1.

Formula:

Scaled Value =

(Value − Minimum Value)

/

(Maximum Value − Minimum Value)

This ensures fair contribution from every feature.

---

# 🏏 Batter Valuation Model

## Objective

Estimate auction value for specialist batters.

### Features Used

| Feature        | Weight |
| -------------- | ------ |
| Total Runs     | 60%    |
| Strike Rate    | 25%    |
| Matches Played | 15%    |

### Batter Score Formula

Batter Score =

(Runs Score × 60%)

*

(Strike Rate Score × 25%)

*

(Match Score × 15%)

### Auction Price Formula

Estimated Price (Cr) =

0.20 + (Batter Score / 100) × 24.80

---

# 🎯 Bowler Valuation Model

## Objective

Estimate auction value for specialist bowlers.

### Features Used

| Feature        | Weight |
| -------------- | ------ |
| Wickets        | 50%    |
| Economy Rate   | 30%    |
| Matches Played | 20%    |

### Economy Rate Calculation

Economy Rate =

Runs Conceded

/

Overs Bowled

Where:

Overs Bowled = Balls Bowled / 6

### Bowler Score Formula

Bowler Score =

(Wicket Score × 50%)

*

(Economy Score × 30%)

*

(Match Score × 20%)

### Auction Price Formula

Estimated Price (Cr) =

0.20 + (Bowler Score / 100) × 24.80

---

# ⭐ All-Rounder Valuation Model

## Objective

Estimate auction value for players contributing in both batting and bowling.

### Features Used

| Feature        | Weight |
| -------------- | ------ |
| Runs           | 30%    |
| Strike Rate    | 15%    |
| Wickets        | 30%    |
| Economy Rate   | 15%    |
| Matches Played | 10%    |

### All-Rounder Score Formula

All-Rounder Score =

(Runs Score × 30%)

*

(Strike Rate Score × 15%)

*

(Wicket Score × 30%)

*

(Economy Score × 15%)

*

(Match Score × 10%)

### Auction Price Formula

Estimated Price (Cr) =

0.20 + (All-Rounder Score / 100) × 24.80

---

# 📊 Visual Analytics

The project includes multiple visualizations:

### Batter Analysis

* Top Valued Batters
* Runs vs Auction Value

### Bowler Analysis

* Top Valued Bowlers
* Wickets vs Auction Value

### All-Rounder Analysis

* Top Valued All-Rounders

### Comparative Analysis

* Average Auction Value by Category
* Auction Price Distribution Comparison

---

# 💡 Key Business Insights

### Batters

Players with:

* High run accumulation
* Strong strike rates
* Extensive IPL experience

receive higher valuations.

### Bowlers

Players with:

* High wicket-taking ability
* Low economy rates
* Long-term consistency

receive higher valuations.

### All-Rounders

Players contributing in both departments generate the highest overall value because they provide dual utility to franchises.

---

# 🛠️ Technology Stack

| Technology       | Purpose                  |
| ---------------- | ------------------------ |
| Python           | Core Development         |
| Pandas           | Data Cleaning & Analysis |
| NumPy            | Numerical Computation    |
| Matplotlib       | Visualization            |
| Scikit-Learn     | MinMax Scaling           |
| Jupyter Notebook | Development Environment  |

---

# 📈 Business Impact

This framework helps franchises:

✅ Reduce auction investment risk

✅ Evaluate players objectively

✅ Compare players fairly

✅ Identify undervalued talent

✅ Optimize auction budgets

✅ Improve decision-making

---

# 🔮 Future Scope

* Machine Learning Based Price Prediction
* Season Performance Forecasting
* Team Recommendation Engine
* Interactive Dashboard
* Real-Time Auction Analytics
* AI-Based Player Comparison System

---

# 🏆 Conclusion

The IPL Auction Intelligence System demonstrates how Data Science and Sports Analytics can be combined to create objective player valuation frameworks.

Using historical IPL data, the system successfully converts player performance into estimated auction values through dedicated valuation models for batters, bowlers, and all-rounders.

This approach provides franchises with a structured and data-driven methodology for making smarter auction decisions.

---

<div align="center">

### ⭐ Star this repository if you found it useful!

**Built with ❤️ using Python, Data Science and Cricket Analytics**

</div>
