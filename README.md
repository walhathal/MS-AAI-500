# MS-AAI-500

# What-Drives-The-Price-of-a-Car-


## 📌 Introduction

This repository contains the Jupyter Notebook for **Application Assignment 11.1**, which explores a dataset of used car listings sourced from Kaggle. The goal of this project is to build a machine learning model that evaluates whether vehicle attributes such as **fuel type, condition, size, body type, color**, and others can be used to accurately predict used car prices.

The dataset (`vehicles.csv`) is located in the `data/` folder of this repository.

By analyzing these features, the project aims to provide insights that will help car dealerships and sales teams optimize their inventory—focusing on the types of vehicles that align with consumer preferences and drive higher sales.

## 🛠️ Key Tasks

- Data cleaning and preprocessing
- Exploratory data analysis and visualizations
- Feature selection and transformation
- Regression modeling and evaluation
- Insights and recommendations for dealership strategy

## 💼 Business Understanding

The primary business objective of this project is to identify the key features that influence used car prices. By understanding these factors, car dealerships and their sales teams can make more informed decisions about which vehicles to stock in their inventory, ultimately aiming to increase sales and meet consumer demand more effectively.

This machine learning application follows a typical pipeline that includes:
- Data collection
- Cleaning and preprocessing
- Feature engineering
- Model training and testing
- Evaluation of prediction accuracy

To ensure continued model improvement, it is recommended that dealerships integrate updated sales data on an ongoing basis. This will help refine the model and improve its ability to accurately predict what consumers value in used cars.

## 📊 Data Understanding

The initial review of the dataset revealed several data quality issues. Many records contained missing or unrealistic values for key attributes. For example, some vehicles had an **odometer reading of 0 or single-digit values**, and others had a **price of $0**, which are not plausible in the context of used car listings.

These inconsistencies highlighted the need for thorough cleaning and filtering before any modeling could be performed.

---

## 🧹 Data Preparation

A number of preprocessing steps were taken to clean and prepare the data for modeling:

- Removed records with **$0 prices** and **odometer values of 0 or less**.
- Dropped rows where critical features were missing or null.
- Removed non-predictive columns such as `VIN`, `id`, and `region`, which do not contribute to price determination.
- Evaluated and dropped additional features like `state`, `paint_color`, `manufacturer`, and `transmission` where they showed little to no correlation with car price.
- Filtered the dataset to include only cars manufactured **from 1990 onward**, since vehicles older than that were rare and not representative.

These steps helped ensure a cleaner dataset for building more reliable and interpretable machine learning models.

## 🤖 Regression Models

To evaluate the factors influencing used car prices, we developed and tested seven different regression models. These models were built using both the full feature set and various filtered subsets of the dataset—based on correlations, thresholds (e.g., price > $5000, odometer > 5000), and manufacture year (> 1990).

Most models resulted in accuracy scores below 50%, with the exception of **Model6** and **Model7**, which demonstrated the most consistent and realistic predictions.

While accuracy remains modest, these models provide valuable insights into which features contribute most to used car pricing.

---

## 🧠 Key Findings

During model testing, we observed the following:

- Some models, like the baseline model using all features, returned **unrealistic predictions**, including negative prices.
- **Simpler models** using only odometer or year performed poorly, with very low or even negative R² scores.
- The **top-performing models**—Model6 and Model7—delivered **more realistic and consistent price predictions** for various test scenarios.

---

### ✅ Recommended Models

Based on performance and interpretability, the following models are recommended:

- **Model6**: Built using odometer, year, diesel fuel, 4WD, and full-size vehicle classification.
- **Model7**: Includes the same features as Model6, with additional filtering for cars manufactured after 1990.

These models achieved the **highest accuracy scores** among those tested and aligned closely with the strongest correlations observed in the dataset.

---

### 🔍 Feature Importance (Ranked)

- **Model6**: Diesel Fuel, Odometer, Four-Wheel Drive, Full-Size, Year  
- **Model7**: Diesel Fuel, Year, Odometer, Four-Wheel Drive, Full-Size

These features consistently showed the strongest influence on price prediction and are central to improving model accuracy moving forward.

---
## 🚀 Next Steps and Recommendations

The dataset used in this analysis contains several data quality issues, including missing, null, zero, and unrealistic values. To improve model performance, further filtering is recommended—for example, limiting records to vehicles manufactured from the year **2000 onward**. This will allow the model to focus on newer vehicles that are more representative of current market trends.

Filtering the dataset in this way will also emphasize features such as **model, number of cylinders, drivetrain, and size**, which tend to have a stronger influence on used car prices—especially when paired with lower odometer readings. This refinement may lead to improved model accuracy, potentially exceeding **50%**.

### 📈 Recommendations for Data Collection and Enhancement

- Incorporate additional, high-quality data from **used car datasets on Kaggle** or dealership records.
- Focus on vehicles from the **last 10–15 years**, which are more relevant for today's market.
- Capture modern vehicle features that influence price, such as:
  - Advanced Driver Assistance Systems (ADAS)
  - Infotainment and touch screen systems
  - Backup and 360° cameras
  - Remote start capabilities
  - Real-time fuel efficiency and mileage tracking

Additionally, consider converting categorical features like `paint_color` and `state` into broader classifications or fewer categories to reduce model complexity and improve generalization.

---

### ✅ Recommended Models

Based on performance, the following models are recommended for deployment and further tuning:

- **Model6**: Trained on filtered data (price > $5000), using the following features:  
  `Odometer`, `Year`, `fuel_diesel`, `drive_4wd`, and `size_full-size`

- **Model7**: Similar to Model6 but with an additional filter for `Year > 1990`

### 🔍 Key Features Driving Model Predictions

- **Model6**: Diesel Fuel, Odometer, Four-Wheel Drive, Full-Size, Year  
- **Model7**: Diesel Fuel, Year, Odometer, Four-Wheel Drive, Full-Size

---

### 📌 Final Recommendation

While **Model6** and **Model7** offer a strong starting point, we recommend continuing to refine these models by integrating more recent and complete vehicle data. With higher-quality inputs and more advanced features, future models could reach an accuracy level of **75% or higher**, providing actionable insights that dealerships can use to optimize inventory and meet evolving consumer preferences.

## Link to Jupyter Notebook
