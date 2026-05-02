# 🏏 IPL Match Insights & Win Predictor

An end-to-end data science project analyzing **16 years of IPL data** to uncover insights and predict match outcomes using interpretable machine learning.

---

## 📊 Project Overview

This project answers a real-world question: *"Given a first innings score, how likely is the chasing team to win?"*

Built to simulate how data scientists present insights to decision-makers in sports analytics — combining EDA, feature engineering, and ML modelling in a single end-to-end pipeline.

---

## 📁 Dataset

- 16 years of IPL match data (2008–2023)
- Match-level data: teams, venue, toss, scores, results
- Sourced from publicly available IPL datasets

---

## 🧹 Data Cleaning

- Removed incomplete and rain-affected matches
- Standardised team names across seasons (franchise renames handled)
- Filtered out matches with missing target or result data

---

## 📈 Exploratory Data Analysis

Key findings from EDA:

- **Mumbai Indians and Chennai Super Kings** dominate IPL history in wins
- **Toss has minimal impact** on match outcome (~50% win rate regardless)
- **Venue plays a significant role** in chase success rates
- **IPL scores have increased over time** — average first innings scores rising season by season

![Average First Inning Score by Season](https://github.com/Appy0413/IPL-Win-Predictor/raw/main/average%20first%20inning%20score%20by%20seasons.png)
![Top Teams Wins](https://github.com/Appy0413/IPL-Win-Predictor/raw/main/top%20teams%20wins.png)
![Toss Winner vs Match Winner](https://github.com/Appy0413/IPL-Win-Predictor/raw/main/toss%20winner%20vs%20match%20winner.png)

---

## ⚙️ Feature Engineering

Features selected based on domain knowledge of T20 cricket:

| Feature | Reasoning |
|---|---|
| Target score | Primary driver of chase difficulty |
| Team win rates | Historical strength of each team |
| Venue chase % | Some grounds favour chasing more |
| Toss decision | Bat/field choice context |
| Season normalisation | Accounts for rule changes over years |
| Recent form (last 5) | Current momentum of team |

---

## 🤖 Model Building

Chose **Logistic Regression** over more complex models because:
- T20 cricket has high inherent randomness — complex models overfit
- Interpretability matters: stakeholders can understand probability outputs
- Probabilities are more useful than binary win/loss predictions

---

## 📉 Model Performance

| Metric | Score |
|---|---|
| Accuracy | ~60% |
| ROC-AUC | ~0.62 |

> 💡 Context: A random coin flip gives 50% accuracy. Our model's 60% reflects meaningful signal extracted from noisy T20 data. The high uncertainty is a property of the sport, not a model weakness.

![Predicted Probability](https://github.com/Appy0413/IPL-Win-Predictor/raw/main/predicted%20probability.png)

---

## 💡 Key Learnings

- Feature engineering is more important than model complexity
- T20 cricket is inherently unpredictable — probabilistic outputs beat binary predictions
- Domain knowledge (cricket context) significantly improves feature selection

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| Python | Core language |
| Pandas | Data cleaning & manipulation |
| Matplotlib / Seaborn | Visualisations |
| Scikit-learn | Model building & evaluation |
| Jupyter Notebook | Analysis & presentation |

---

## 🚀 Future Improvements

- Player-level data (top batsman, bowler form)
- Ball-by-ball live prediction
- Streamlit web app for interactive predictions
- XGBoost / Random Forest comparison

---

## ⚙️ Setup Instructions

```bash
git clone https://github.com/Appy0413/IPL-Win-Predictor.git
cd IPL-Win-Predictor
pip install -r requirements.txt
```
Open `notebook/` folder and run the Jupyter notebook.

---

## 📌 Author

**Aprajita Singh** — Aspiring AI/ML Engineer  
[GitHub](https://github.com/Appy0413)
