# 🏏 Moneyball Sri Lanka: T20 Player Impact Modeling & All-Time Team Optimization

An end-to-end sports quantitative analytics and operations research project built in Python. Utilizing complete ball-by-ball international records from Cricsheet (52,400+ deliveries across 225 T20Is from 2006 to 2026), this project evaluates phase-specific player performances and solves a Binary Integer Linear Programming (BILP) model to determine the statistically optimal All-Time Sri Lanka Men's T20 XI.

---

## 📌 Project Objectives
1. Phase-Wise Bowling Evaluation: Quantify death-over efficiency (overs 16–20) combining Economy Rate, Wicket Strike Rate, and Dot Ball percentage.
2. Batting Acceleration Modeling: Evaluate boundary intent and strike rate differentials between the Powerplay (overs 1–6) and Death phase.
3. Mathematical Team Optimization: Formulate and solve an Integer Linear Program to select an 11-player squad that maximizes composite player impact subject to realistic composition constraints (wicketkeeper, pace/spin balance, minimum 20 overs capacity).

---

## 🛠️ Tech Stack & Methodologies
* Language: Python 3
* Optimization Engine: scipy.optimize.milp (HiGHS Simplex & Branch-and-Bound solver)
* Data Science & Visualization: pandas, numpy, plotly, matplotlib, seaborn
* Mathematical Modeling: Binary Integer Linear Programming (BILP)
* Data Source: Official Cricsheet ball-by-ball T20 International archive

---

## 📊 Phase-Specific Key Findings

### 1. The Death Bowling Matrix (Overs 16–20)
* Mystery Spin Anomaly: Wanindu Hasaranga and Ajantha Mendis recorded sub-7.5 death economies and ~36% dot ball frequencies, proving that spin variations severely disrupt aggressive death hitting.
* Volume Benchmark: Lasith Malinga maintained an elite 8.3 economy over hundreds of death deliveries across a 15-year career.
* Strike Wicket-Taking: Matheesha Pathirana demonstrated the fastest wicket strike rate at the death (< 10 balls per wicket).

### 2. Batting Acceleration & Intent
* Top-Order Anchors: Pathum Nissanka and Tillakaratne Dilshan demonstrated masterclass pacing, maintaining ~120 Powerplay strike rates while accelerating to 180+ at the death.
* Designated Finisher: Dasun Shanaka demonstrated specialized death hitting with a career death strike rate of ~160.

---

## 🏆 The Mathematically Optimal All-Time Sri Lanka T20 XI

Solved via Binary Integer Linear Programming to maximize overall team impact under official composition constraints:

| # | Player | Role | Career Runs | Wickets | Total Impact Score |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | Pathum Nissanka | Batter | 2,606 | 0 | 3,330.7 |
| 2 | Kusal Mendis | Wicketkeeper / Batter | 2,510 | 0 | 3,257.5 |
| 3 | Kusal Janith Perera | Wicketkeeper / Batter | 2,307 | 0 | 3,064.0 |
| 4 | Tillakaratne Dilshan | Batter / Off-spin | 1,747 | 9 | 2,353.6 |
| 5 | Dasun Shanaka | Pace All-Rounder / Finisher | 2,008 | 42 | 3,602.7 |
| 6 | Angelo Mathews | All-Rounder | 1,343 | 41 | 2,779.0 |
| 7 | Thisara Perera | Pace All-Rounder | 1,042 | 42 | 2,364.4 |
| 8 | Wanindu Hasaranga | Leg-spin All-Rounder | 742 | 155 | 5,022.2 |
| 9 | Lasith Malinga | Pace Spearhead | 136 | 108 | 2,986.9 |
| 10 | Dushmantha Chameera | Express Pace | 125 | 98 | 2,495.2 |
| 11 | Maheesh Theekshana | Mystery Spin | 114 | 83 | 2,429.9 |

* Total Team Impact Score: 33,686.1 points
* Solver Status: Optimal solution found (HiGHS Status 7)
* Team Balance: Deep batting down to #8, 7 bowling options (5 pace, 2 spin).

---

## 🚀 How to Run
1. Clone the repository:
   git clone https://github.com/rasindupramith-oss/sri-lanka-cricket-analytics-moneyball.git
2. Open and run Sri_Lanka_Cricket_Analytics.ipynb in Google Colab or Jupyter Notebook.

---
Author: Rasindu Pramith — Undergraduate in Applied Statistics, Faculty of Science, University of Colombo
