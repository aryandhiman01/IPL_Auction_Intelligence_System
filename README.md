<div align="center">

# 🏏 IPL Auction Intelligence System
### Data-Driven Player Valuation & Auction Price Prediction

<img src="https://img.shields.io/badge/Python-3.10+-blue?style=for-the-badge&logo=python" />
<img src="https://img.shields.io/badge/Pandas-Data%20Analysis-green?style=for-the-badge&logo=pandas" />
<img src="https://img.shields.io/badge/Scikit--Learn-Machine%20Learning-orange?style=for-the-badge&logo=scikitlearn" />
<img src="https://img.shields.io/badge/Jupyter-Notebook-red?style=for-the-badge&logo=jupyter" />

### 📊 IPL Player Analytics | 💰 Auction Valuation | 🏆 Performance Intelligence

</div>

---

# 📌 Project Overview

The **IPL Auction Intelligence System** is a Data Science project designed to evaluate IPL players and estimate their potential auction value using historical performance data.

Traditional player selection often depends on reputation, recent form, or subjective judgment. This project introduces a **data-driven valuation framework** that converts player performance into estimated auction prices.

The system analyzes:

- Batting Performance
- Bowling Performance
- All-Rounder Performance
- Player Experience
- Match Impact
- Auction Value Estimation

---

# 🎯 Business Problem

IPL franchises invest hundreds of crores during player auctions.

However, determining a player's fair market value is a major challenge.

### Common Problems:

❌ Overpaying for underperforming players

❌ Ignoring consistent performers

❌ Lack of objective valuation methods

❌ Reliance on intuition and reputation

This project addresses these challenges by creating a structured player valuation framework based on historical IPL statistics.

---

# 🚀 Project Objectives

- Analyze historical IPL player performance.
- Build separate valuation models for:
  - Batters
  - Bowlers
  - All-Rounders
- Generate player performance scores.
- Estimate realistic IPL auction values.
- Support data-driven franchise decision making.

---

# 📂 Dataset Information

The dataset contains ball-by-ball IPL match data including:

- Match Information
- Player Statistics
- Batting Records
- Bowling Records
- Team Information
- Venue Details
- Match Outcomes

### Key Features

```text
match_id
batting_team
bowling_team
batter
bowler
runs_batter
balls_faced
runs_bowler
bowler_wicket
venue
season
match_won_by
player_of_match
```

---

# 🧹 Data Cleaning & Preprocessing

The dataset was cleaned before model development.

### Cleaning Steps

✔ Removed duplicate team names

Example:

```text
Delhi Daredevils → Delhi Capitals
Kings XI Punjab → Punjab Kings
Royal Challengers Bangalore → Royal Challengers Bengaluru
```

✔ Standardized city names

```text
Bangalore → Bengaluru
```

✔ Standardized venue names

✔ Converted mixed datatype columns

✔ Removed invalid values

✔ Handled missing values

✔ Created player-level datasets

---

# 🏏 Batter Valuation Model

## Objective

Estimate the auction value of specialist batters.

### Features Used

| Feature | Weight |
|----------|----------|
| Total Runs | 60% |
| Strike Rate | 25% |
| Matches Played | 15% |

### Batter Score Formula

```text
Batter Score =
(Runs Score × 60%)
+
(Strike Rate Score × 25%)
+
(Match Score × 15%)
```

### Auction Price Formula

```text
Estimated Price =
0.20 + (Batter Score / 100) × 24.80
```

### Price Range

```text
Minimum Price = ₹20 Lakh
Maximum Price = ₹25 Crore
```

---

# 🎯 Bowler Valuation Model

## Objective

Estimate the auction value of specialist bowlers.

### Features Used

| Feature | Weight |
|----------|----------|
| Wickets | 50% |
| Economy Rate | 30% |
| Matches Played | 20% |

### Economy Calculation

```text
Economy Rate =
Runs Conceded / Overs Bowled
```

### Bowler Score Formula

```text
Bowler Score =
(Wicket Score × 50%)
+
(Economy Score × 30%)
+
(Match Score × 20%)
```

### Auction Price Formula

```text
Estimated Price =
0.20 + (Bowler Score / 100) × 24.80
```

---

# ⭐ All-Rounder Valuation Model

## Objective

Estimate the auction value of players contributing in both batting and bowling.

### Features Used

| Feature | Weight |
|----------|----------|
| Runs | 30% |
| Strike Rate | 15% |
| Wickets | 30% |
| Economy Rate | 15% |
| Matches Played | 10% |

### All-Rounder Score Formula

```text
All-Rounder Score =
(Runs Score × 30%)
+
(Strike Rate Score × 15%)
+
(Wicket Score × 30%)
+
(Economy Score × 15%)
+
(Match Score × 10%)
```

### Auction Price Formula

```text
Estimated Price =
0.20 + (All-Rounder Score / 100) × 24.80
```

---

# ⚙️ Technologies Used

<table>
<tr>
<td><b>Python</b></td>
<td>Core Programming</td>
</tr>

<tr>
<td><b>Pandas</b></td>
<td>Data Cleaning & Analysis</td>
</tr>

<tr>
<td><b>NumPy</b></td>
<td>Numerical Computation</td>
</tr>

<tr>
<td><b>Matplotlib</b></td>
<td>Visualization</td>
</tr>

<tr>
<td><b>Scikit-Learn</b></td>
<td>MinMax Scaling</td>
</tr>

<tr>
<td><b>Jupyter Notebook</b></td>
<td>Development Environment</td>
</tr>
</table>

---

# 📈 Key Insights

### Top Valued Batters

- Virat Kohli
- Rohit Sharma
- David Warner
- Shikhar Dhawan
- MS Dhoni

### Top Valued Bowlers

- Jasprit Bumrah
- Yuzvendra Chahal
- Bhuvneshwar Kumar
- Ravichandran Ashwin
- Sunil Narine

### Top Valued All-Rounders

- Ravindra Jadeja
- Hardik Pandya
- Andre Russell
- Sunil Narine
- Shane Watson

---

# 💡 Business Value

This system helps IPL franchises:

✅ Evaluate players objectively

✅ Reduce auction investment risk

✅ Identify undervalued talent

✅ Compare players fairly

✅ Optimize auction budgets

✅ Make data-driven decisions

---

# 🔮 Future Enhancements

- Machine Learning Based Price Prediction
- Season-wise Performance Forecasting
- Team Recommendation Engine
- Player Performance Dashboard
- Real-Time Auction Analytics
- AI-Powered Player Comparison System

---

# 📊 Project Outcome

The IPL Auction Intelligence System successfully converts historical player performance into realistic auction value estimates using separate valuation models for batters, bowlers, and all-rounders.

The project demonstrates how Data Science can support strategic decision-making in professional sports analytics.

---

<div align="center">

### ⭐ If you found this project useful, don't forget to star the repository!

**Made with ❤️ using Data Science & Cricket Analytics**

</div>
