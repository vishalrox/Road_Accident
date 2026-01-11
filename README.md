# Regulatory Affairs of Road Accident Data 2020 India (ML Project)

This repository contains an **EDA + Machine Learning regression project** on Road Accident Data (India, 2020) for **50 million-plus cities**.  
The project analyzes accident causes and outcomes, and builds **tree-based regression models** to predict accident counts.

---

## 📌 Project Overview
Road accidents are a critical public safety issue. This project explores:
- Accident distribution across Indian million-plus cities
- Major accident cause categories and subcategories
- Relationship between causes and incident outcomes
- Machine Learning prediction for total accident counts
- Feature importance for model interpretability

---

## 🎯 Objectives
- Analyze and visualize accident patterns across cities.
- Study **cause category** and **cause subcategory** contributions.
- Visualize **Cause Category vs Outcome** relationships.
- Compute **Fatality Ratio (Deaths / Total Accidents)** to understand severity.
- Build and compare **Decision Tree** and **Random Forest** regression models to predict accident counts.

---

## 🧾 Dataset Information
- **Dataset Name:** Road Accidents in India (2020)
- **Source:** Government of India Open Data Portal  
  https://data.gov.in/catalog/road-accidents-india-2020

### Dataset Columns
| Column | Description |
|--------|-------------|
| Million Plus Cities | Name of the cities |
| Cause category | Primary classification of accident cause |
| Cause Subcategory | Detailed breakdown of the accident cause |
| Outcome of Incident | Accident outcome (accidents, deaths, injuries) |
| Count | Number of recorded incidents |

> **Note:** The dataset is aggregated (statistical records), not event-level accident logs.

---

## 🧠 Key EDA Insights
- Accident patterns vary significantly across cities and cause types.
- Certain junction types like **T-junction** and **Y-junction** appear as subcategories under junction causes.
- Cause category vs outcome visualization helps identify which cause types contribute more to injuries/deaths/accidents.
- Fatality Ratio highlights cities with more severe outcomes.

---

## 🤖 Machine Learning Approach

### ML Task
**Regression:** Predict accident `Count` using categorical features.

### Target Variable
- `Count`

### Features Used
- `Million Plus Cities`
- `Cause category`
- `Cause Subcategory`

### ML Dataset Restriction
For meaningful prediction, ML modeling is restricted to:
- **Outcome of Incident = "Total number of Accidents"**

### Models Used
1. **Decision Tree Regressor**
2. **Random Forest Regressor**

### Evaluation Metrics
- MAE (Mean Absolute Error)
- RMSE (Root Mean Squared Error)
- R² Score

### Interpretability
- Feature importance is extracted from **Random Forest** to identify the most influential city/cause factors.

---

## Project

### Dataset Preview

### Top 15 Accident-Prone Cities (Total Accidents)

### Cause Category vs Outcome (Stacked Bar)

### ML Model Results (Decision Tree vs Random Forest)

### Feature Importance (Random Forest)

> Note: All outputs (EDA charts, evaluation metrics, feature importance) are available inside the notebook.

---

## 📁 Project Structure
```
Road_Accident/
│
├── Road_accident_2020.ipynb
├── data/
│ └── Regulatory Affairs of Road Accident Data 2020 India.csv
├── README.md
└── requirements.txt
```

---

## ⚙️ How to Run the Project

### 1) Clone the Repository
```
git clone <https://github.com/vishalrox/Road_Accident>
cd Road_Accident
```
### 2) Install Dependencies
``` 
pip install -r requirements.txt
```

### 3) Run Notebook

Open in VS Code / Jupyter:

jupyter notebook

Then run:
```
Road_accident_2020.ipynb
```

## Results Summary

Decision Tree and Random Forest models were trained and evaluated.

Random Forest generally provides more stable predictions due to ensemble learning.

Feature importance highlights key contributing cities and subcategories affecting accident counts.

## Limitations

Dataset is aggregated and categorical (not raw accident logs).

No time-based features (hour/day/month), traffic density, road length, or population indicators.

"Others" cause subcategory dominates some segments, reducing fine-grained causality.

## 🚀 Future Work

Add external factors like population and vehicle density.

Try advanced ensemble methods (Gradient Boosting, XGBoost, LightGBM).

Convert the task into classification (High vs Low accident zones).

Combine multiple years of accident datasets for stronger generalization.

## 👤 Author

Vishal Mehta

## Topics

machine-learning · data-analysis · eda · regression · random-forest · decision-tree · python · scikit-learn · data-visualization · road-safety · india
