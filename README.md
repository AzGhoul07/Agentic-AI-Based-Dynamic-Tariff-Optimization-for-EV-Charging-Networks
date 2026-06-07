# AI-Driven Multi-Agent System for EV Dynamic Tariff Optimization

## Overview

This project presents an AI-powered multi-agent framework for intelligent Electric Vehicle (EV) charging management. The system integrates demand forecasting, dynamic tariff optimization, and continuous performance monitoring to improve charging infrastructure utilization and support data-driven pricing decisions.

Using real-world EV charging datasets, the framework predicts charging demand, dynamically adjusts tariffs based on utilization patterns, and evaluates system performance through a feedback-driven monitoring agent.

---

## Key Features

### Demand Prediction Agent

* Forecasts EV charging demand using machine learning models.
* Utilizes temporal, utilization, occupancy, and pricing features.
* Compares multiple regression models and selects the best-performing model for deployment.

### Dynamic Tariff Pricing Agent

* Adjusts charging prices based on predicted utilization levels.
* Applies discount pricing during low-demand periods.
* Applies surge pricing during congestion periods.
* Generates hourly tariff recommendations.

### Monitoring & Learning Agent

* Tracks utilization, revenue, and pricing efficiency metrics.
* Evaluates system performance across multiple episodes.
* Provides feedback for continuous improvement of tariff strategies.

### Executive Dashboard

* Interactive visualizations for demand patterns, utilization trends, revenue analysis, and agent performance.
* Consolidated view of all key system metrics.

---

## Datasets

### ACN-Data

* 14,999 EV charging sessions
* Includes charging duration, energy delivered, station information, and session timestamps

### UrbanEV

* 247 charging grids
* 8,640 temporal observations
* Includes charging volume, occupancy, utilization, and pricing information

---

## Methodology

### 1. Data Preprocessing

* Missing value handling
* Feature extraction
* Temporal indexing
* Data aggregation

### 2. Feature Engineering

Generated features include:

* Hour of day
* Day of week
* Weekend indicators
* Lag variables
* Rolling averages
* Utilization metrics
* Occupancy density
* Fast charger ratio
* Grid-level characteristics

### 3. Demand Forecasting

Models evaluated:

* Random Forest Regressor
* Gradient Boosting Regressor
* Ridge Regression

Selected Model:

* Random Forest Regressor

Performance:

* Demand Prediction R² = 0.9976
* Utilization Prediction R² = 0.9802
* MAPE = 0.86%

### 4. Dynamic Pricing Strategy

Pricing decisions are based on utilization thresholds:

| Utilization Level | Action           |
| ----------------- | ---------------- |
| < 30%             | Discount Pricing |
| 30% – 80%         | Baseline Pricing |
| > 80%             | Surge Pricing    |

### 5. Monitoring & Evaluation

Performance metrics include:

* Revenue Gain
* Charger Utilization
* Pricing Efficiency Score
* Customer Response Rate
* Congestion Indicators

---

## Results

### Demand Prediction Agent

* R² Score: 0.9976
* RMSE: 142.02
* MAE: 86.53
* MAPE: 0.86%

### Tariff Pricing Agent

* Charger utilization improved from 28.9% to 30.0%
* Dynamic pricing successfully shifted demand toward off-peak periods
* Generated adaptive hourly tariff recommendations

### Monitoring Agent

* Evaluated performance across multiple episodes
* Pricing Efficiency Score: 0.8888 yuan/kWh
* Enabled continuous feedback-driven evaluation

---

## Visualizations

The project includes:

* ACN charging session analysis
* UrbanEV temporal demand analysis
* Demand prediction performance
* Dynamic tariff outcomes
* Monitoring agent evaluation
* Executive dashboard

---

## Project Structure

```text
EV-Dynamic-Tariff-Optimization/
│
├── notebooks/
│   └── EV_Dynamic_Tariff_Optimization.ipynb
│
├── data/
│   ├── ACN_Data.csv
│   └── UrbanEV_Data.csv
│
├── outputs/
│   ├── acn_sessions_processed.csv
│   ├── urbanev_panel_predictions.csv
│   ├── episode_monitoring_results.csv
│   ├── dynamic_tariff_recommendations.csv
│   └── grid_classification.csv
│
├── visualizations/
│   ├── plot1_acn_demand.png
│   ├── plot2_urbanev_eda.png
│   ├── plot3_prediction.png
│   ├── plot4_tariff.png
│   ├── plot5_monitoring.png
│   └── plot6_dashboard.png
│
├── presentation/
│   └── Final_Presentation.pdf
│
├── README.md
└── requirements.txt
```

---

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-Learn
* Matplotlib
* Seaborn
* Jupyter Notebook

---

## Future Improvements

* Reinforcement Learning based pricing optimization
* Real-time streaming data integration
* Multi-objective revenue-utilization optimization
* User behavior modeling
* Deployment as a cloud-based decision support system

---

## Authors

Developed as part of a data analytics and intelligent systems project focused on AI-driven EV charging infrastructure optimization.
