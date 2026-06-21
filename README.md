# Agricultural Yield : EDA & Machine Learning

Week 3 Assignment 1: Exploratory Data Analysis and a baseline Linear Regression model on an agricultural yield dataset.

## Files
- `Week3_Assignment1_Agricultural_Yield_EDA_ML.ipynb` — main notebook (pre-executed, all outputs included)
- `agriculture_yield_dataset.csv` — dataset (must sit in the same folder as the notebook)

## Dataset
1500 records, 8 columns, no missing values.

| Column | Type | Description |
|---|---|---|
| `rainfall_mm` | float | Rainfall in mm |
| `temperature_c` | float | Temperature in °C |
| `fertilizer_kg` | float | Fertilizer used (kg) |
| `irrigation_hours` | float | Irrigation hours |
| `soil_ph` | float | Soil pH |
| `crop_type` | categorical | Maize, Wheat, Cotton, Soybean, Rice |
| `soil_type` | categorical | Loamy, Sandy, Clay |
| `yield_ton_per_hectare` | float | **Target variable** |

## How to Run
```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
jupyter notebook Week3_Assignment1_Agricultural_Yield_EDA_ML.ipynb
```
Run All to reproduce, or just read the saved outputs.

## Structure
- **Part A — Dataset Overview:** shape, dtypes, missing values, descriptive stats
- **Part B — EDA:** distributions, crop/soil counts, yield distribution & outliers, scatter plots, correlation heatmap, group-wise average yield
- **Part C — Data Preparation:** one-hot encoding of categorical columns, feature/target split
- **Part D — Machine Learning:** 80/20 train-test split, Linear Regression, coefficients, RMSE/R²

## Key Results
- No missing values; `rainfall_mm` has the highest mean (754.05) and std (255.10)
- Most frequent crop: **Cotton** (311); most common soil: **Clay** (534)
- Only 3 outliers in yield (IQR method)
- Top 3 features correlated with yield: `rainfall_mm` (0.554), `irrigation_hours` (0.543), `fertilizer_kg` (0.278)
- Highest average yield: **Rice** crop (5.49 t/ha), **Loamy** soil (5.37 t/ha)
- Linear Regression test performance: **RMSE = 0.356**, **R² = 0.863**
- Strongest positive coefficient: `crop_type_Rice` (0.864)
