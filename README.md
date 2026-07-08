# ⚡ Smart Electricity Consumption Prediction & Energy Optimization System
**TEYZIX CORE Internship - ML Task 3 (Advanced)**

---

## Project Overview
This project is an advanced, production-ready Machine Learning system designed to predict daily electricity consumption based on household demographics, weather conditions, and appliance usage. Beyond simple prediction, the system acts as an Energy Optimizer, providing users with peak hour alerts, estimated monthly bills, and actionable recommendations to reduce energy costs.

##  Dataset Generation Strategy
As per the strict requirement of the task, **NO public datasets (Kaggle, UCI, etc.) were used.** A highly realistic synthetic dataset of 1,500 records was generated from scratch using Python's `Faker` library. The dataset mathematically models real-world energy consumption behaviors, incorporating features like:
- Household Demographics (Family Members, Rooms, House Type)
- Appliance Usage (AC, Fans, Refrigerator, Washing Machine, Motor, Lighting)
- Environmental Factors (Outdoor Temperature, Season, Holidays)

## Machine Learning Pipeline
1. **Data Preprocessing:** Handled missing values, removed duplicates, and applied One-Hot Encoding.
2. **Feature Scaling:** Applied `StandardScaler` to normalize appliance hours and temperature.
3. **Model Selection:** Trained **Linear Regression, Random Forest, and XGBoost**. The system automatically selects and saves the model with the highest R² Score (Linear Regression demonstrated peak performance due to the linear relationships in the generated data).
4. **Deployment:** Built an interactive Web Interface using **Gradio** for real-time predictions and intelligent energy-saving recommendations.

## How to Run the Project
1. Clone the repository and navigate to the project folder.
2. Ensure you have Python installed. Install dependencies using:
   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn faker xgboost gradio joblib