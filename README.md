# 🌾 Seasonal Agriculture Performance Analysis

A data analytics project analyzing how agricultural performance — yield, profit, resource usage, and risk — varies across seasons, using a dataset of 4,000 farm records across India.



---

## 📖 Project Description

Agricultural activities are shaped by seasonal variations in environmental conditions, farming practices, resource availability, and market conditions — yet raw agricultural data on its own doesn't reveal *how* performance changes across seasons or what patterns drive those changes.

This project analyzes a seasonal agriculture performance dataset to identify meaningful patterns, trends, relationships, and differences in agricultural outcomes across **Kharif, Rabi, and Zaid** seasons. It combines data cleaning, exploratory data analysis (EDA), statistical testing, and custom-designed analytical questions to produce evidence-based insights and recommendations for seasonal agricultural planning.

---

## 📂 Dataset

**File:** `seasonal_agriculture_performance_dataset.csv`
**Size:** 4,000 rows × 28 columns

| Category | Columns |
|---|---|
| Identifiers & Location | `Farm_ID`, `State`, `District` |
| Farming Context | `Crop`, `Season`, `Farm_Area_Hectares`, `Irrigation_Method` |
| Environmental Conditions | `Rainfall_mm`, `Avg_Temperature_C`, `Humidity_pct`, `Sunlight_Hours_Day`, `Soil_pH`, `Soil_Moisture_pct` |
| Inputs / Resources | `Nitrogen_kg_ha`, `Phosphorus_kg_ha`, `Potassium_kg_ha`, `Fertilizer_kg_ha`, `Pesticide_Litre_ha`, `Seed_Quality_Score`, `Water_Used_m3` |
| Outcomes | `Yield_Tonnes_Ha`, `Production_Tonnes`, `Water_Efficiency_t_per_1000m3`, `Disease_Pest_Risk_pct` |
| Economics | `Market_Price_INR_Tonne`, `Total_Cost_INR`, `Revenue_INR`, `Profit_INR` |

Covers **8 states**, **10 districts**, **8 crops**, and **4 irrigation methods**.

---

## 🎯 Objectives

- Explore and clean the seasonal agriculture dataset
- Examine how yield, profit, and resource usage vary across seasons
- Identify significant patterns, relationships, and outliers
- Statistically validate seasonal differences
- Design original analytical questions beyond standard comparisons
- Produce evidence-based insights and actionable recommendations

---

## 🛠️ Methodology

1. **Data Cleaning & Preparation** — missing value imputation (Season + Crop median), duplicate checks, text standardization, validity checks
2. **Descriptive Statistics** — central tendency, spread, and distribution shape for all numeric variables
3. **Outlier Investigation** — IQR method + boxplots, with a documented decision on retaining legitimate high-yield outliers (Sugarcane)
4. **Univariate Analysis** — distribution of environmental, financial, and categorical variables
5. **Bivariate Analysis** — season vs. yield/profit, rainfall vs. yield, crop vs. yield, irrigation vs. water efficiency
6. **Multivariate Analysis** — Season × Crop and Season × Irrigation heatmaps, faceted state-season comparisons
7. **Correlation Analysis** — full correlation heatmap, top drivers of profit and yield
8. **Seasonal Comparison** — summary tables, multi-panel charts, and a one-way ANOVA significance test
9. **Custom Analyses** — water-use profitability, disease/pest risk vs. reward, regional consistency of seasonal patterns

---

## 🔑 Key Insights

- **Kharif is the strongest season** — highest average yield and profit of the three seasons
- **Zaid is the riskiest season financially** — the majority of Zaid-season farms operate at a loss
- **Season significantly affects yield** — confirmed via one-way ANOVA (p < 0.05)
- **Irrigation method matters more than season for water efficiency** — Rainfed and Drip outperform Flood irrigation
- **Revenue and water efficiency are the strongest profit drivers**, while input intensity (fertilizer, pesticide) shows little correlation with profit
- **Regional patterns broadly follow the national seasonal trend**, with a few states diverging — flagged for further investigation

*(Full list of 10 insights, recommendations, and limitations are documented in the notebook.)*

---

## 🧰 Tech Stack

- **Language:** Python 3
- **Environment:** Google Colab / Jupyter Notebook
- **Libraries:** `pandas`, `numpy`, `matplotlib`, `seaborn`

---

## 🚀 How to Run

1. Clone this repository or download the notebook
2. Open `Seasonal_Agriculture_Performance_Analysis.ipynb` in [Google Colab](https://colab.research.google.com/)
3. Run the cells in order — you'll be prompted to upload `seasonal_agriculture_performance_dataset.csv`
4. All cleaning, analysis, and visualizations run automatically

```bash
# Or run locally with Jupyter
pip install pandas numpy matplotlib seaborn scipy jupyter
jupyter notebook Seasonal_Agriculture_Performance_Analysis.ipynb
```

---

