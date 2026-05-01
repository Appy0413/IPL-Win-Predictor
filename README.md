# 🏏 IPL Match Insights & Win Predictor

## Overview
This project analyzes 16 years of IPL data (2008–2024) to uncover insights and predict whether a chasing team will win a match.

## Key Insights
- Mumbai Indians and Chennai Super Kings dominate IPL history
- Toss has minimal impact on match outcomes (~50%)
- Venue plays a significant role in chase success
- IPL scores have increased over time

## Features Used
- Target score
- Team win rates
- Venue chase percentage
- Toss decision
- Season normalization
- Recent form (last 5 matches)

## Model
- Logistic Regression (chosen for interpretability)

## Performance
- Accuracy: ~60%
- ROC-AUC: ~0.62

## Key Learnings
- Feature engineering is more important than model complexity
- T20 cricket is inherently unpredictable
- Probabilities are more useful than binary predictions

## Future Improvements
- Player-level data
- Ball-by-ball live prediction
- Streamlit web app

## Tech Stack
- Python
- Pandas
- Matplotlib / Seaborn
- Scikit-learn
