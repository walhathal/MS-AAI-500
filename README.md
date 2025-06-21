# Used Car Price Analysis 🚗📊

A Statistics science class project analyzing key factors that influence used car prices using a dataset of over 400,000 used car listings.

## 🎯 Project Overview

This project identifies the most significant factors affecting used car prices through data cleaning, exploratory data analysis, and visualization. The goal is to provide insights into what drives used car pricing.

## 📊 Dataset Description

The dataset contains **426,880 used car listings** with the following key features:

| Feature | Description |
|---------|-------------|
| `id` | Unique identifier for each listing |
| `region` | Region where the car is listed |
| `price` | Listing price in USD |
| `year` | Year of manufacture |
| `manufacturer` | Car manufacturer |
| `model` | Car model |
| `condition` | Condition of the vehicle |
| `cylinders` | Engine cylinders |
| `fuel` | Fuel type |
| `odometer` | Mileage |
| `title_status` | Status of the title |
| `transmission` | Type of transmission |
| `VIN` | Vehicle Identification Number |
| `drive` | Type of drive (FWD, RWD, AWD) |
| `size` | Size category |
| `type` | Vehicle type |
| `paint_color` | Exterior color |
| `state` | State where listed |

## 🛠️ Technologies Used

- **Python 3.x**
- **pandas** - Data manipulation
- **numpy** - Numerical computing
- **matplotlib & seaborn** - Data visualization
- **scikit-learn** - Machine learning models

## 📋 Requirements

```bash
pip install -r requirements.txt
```

Create a `requirements.txt` file with:
```
pandas>=1.3.0
numpy>=1.21.0
matplotlib>=3.4.0
seaborn>=0.11.0
plotly>=5.0.0
scikit-learn>=1.0.0
statsmodels>=0.12.0
shap>=0.40.0
joblib>=1.0.0
scipy>=1.7.0
```

## 🚀 Getting Started

1. **Clone or download** the project files
2. **Install required libraries**: `pip install pandas numpy matplotlib seaborn scikit-learn`
3. **Place the dataset** (`vehicles.csv.zip`) in the project folder
4. **Run the analysis** using Jupyter notebook or Python script

## 📁 Project Structure

```
used-car-price-analysis/
│
├── data/
│   └── vehicles.csv.zip          # Raw dataset
│
├── notebooks/
│   └── analysis.ipynb            # Jupyter notebook with analysis
│
├── src/
│   ├── data_cleaning.py          # Data preprocessing functions
│   ├── eda.py                    # Exploratory data analysis
│   ├── modeling.py               # Machine learning models
│   └── visualization.py          # Plotting functions
│
├── results/
│   ├── plots/                    # Generated visualizations
│   └── models/                   # Saved models and results
│
├── README.md
├── requirements.txt
└── used_car_analysis.py          # Main analysis script
```

## 🔍 Analysis Steps

### 1. Data Understanding
- **Dataset**: 426,880 used car listings with 18 features
- **Key variables**: price, year, manufacturer, model, condition, mileage, etc.

### 2. Data Cleaning
- Removed columns with >50% missing values
- Dropped rows with missing data
- Handled outliers using statistical methods
- Final clean dataset: 57,807 records

### 3. Feature Engineering
- Created `price_per_age` feature
- Cleaned categorical variables (e.g., extracted numbers from cylinders)
- Converted data types for analysis

### 4. Exploratory Data Analysis
- Distribution analysis of prices and other variables
- Correlation analysis between features
- Visualization of key relationships

## 📊 Key Findings

- **Data Quality**: Original dataset had significant missing values; final analysis used ~14% of original data
- **Price Distribution**: Median price of $13,950 with right-skewed distribution
- **Missing Data Impact**: Columns like 'size' had 71% missing values and were removed
- **Feature Relationships**: Analysis reveals correlations between price, year, mileage, and other factors

## 📈 Visualizations Created

- Price distribution histograms
- Correlation heatmap
- Categorical variable distributions
- Missing data analysis charts

## 🎓 Class Learning Objectives Met

- Data cleaning and preprocessing techniques
- Handling missing values and outliers
- Exploratory data analysis methods
- Data visualization best practices
- Feature engineering concepts
