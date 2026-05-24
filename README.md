# ⚽ Euro League Player Form Prediction

ML models forecasting player form scores across 7 European leagues using 100K+ match records from 2014–2023.

---

## 👥 Team Members
- **Nithin Kumar Hadhge Girish Kumar** (NK12131)
- **Resham Deepak Bahira** (Reshamm13)
- **Sudhanshu Gopalrao Pawar** (Psudhanshu)
- **Aaryan Wani** (aaryanwani)

---

## 📖 Introduction
This project develops a predictive model for **forecasting player form scores** in major European football leagues by analyzing historical performance data and incorporating contextual factors such as match location and weather conditions.

### Key Stakeholders
- **Team Managers & Coaches** lineup planning and training decisions
- **Sports Analysts** improved accuracy for predictive analysis and reporting
- **Fans & Enthusiasts** enhanced engagement through data-driven insights

---

## 📊 Data

**Source:** [Statbunker Football Statistics](https://data.world/cclayford/statbunker-football-statistics)

| Attribute | Details |
|-----------|---------|
| Seasons | 2014/15 – 2022/23 |
| Leagues | Premier League, Bundesliga, La Liga, Ligue 1, Serie A, Eredivisie, Scottish Premiership |
| Features | ~117 |
| Rows | 100,000+ |

---

## ⚙️ Methods

### 1. Data Preparation
- Consolidated 63 CSV files spanning multiple seasons
- Standardized key attributes (player IDs, team names)
- Applied systematic cleaning and validation procedures

### 2. Feature Engineering
- Integrated weather summaries for match context
- Developed position-specific form scores
- Created rolling statistical features:
  - Rolling mean (3-match window)
  - Rolling variance

### 3. Models

**Machine Learning**
- Random Forest Regressor
- XGBoost Regressor
- Linear Regression

**Time Series**
- SARIMA
- Facebook Prophet

---

## 📈 Results

| Model | CV R² | Test R² | Notes |
|-------|-------|---------|-------|
| Random Forest | 0.9239 ± 0.0176 | 0.8983 | Best generalization |
| XGBoost | 0.9945 ± 0.0065 | 0.9834 | Potential overfit risk |
| Linear Regression | ~1.0000 | ~1.0000 | Clear overfitting |

**Random Forest is the recommended model** — CV and test scores are closely aligned, indicating genuine generalization to unseen data.

### Weather Impact
Weather factors had negligible influence on form scores, with observed differences only at the fourth/fifth decimal place.

---

## ⚠️ Limitations
- Weather had minimal impact, contrary to initial expectations
- Time series models did not capture major career changes (injuries, transfers)
- Limited predictive power for inter-league transfers

---

## 🔮 Future Work
- Expand contextual features: injuries, team formations, player-club synergy, inter-player interactions
- Build an interactive dashboard with real-time predictions and visual insights for analysts and coaches