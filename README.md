# road-safety-accident-prediction
“Phase-2 Project – Enhancing Road Safety with AI-driven Accident Severity Prediction”
# Enhancing Road Safety with AI-driven Traffic Accident Analysis and Prediction

**Student Name**: Monisha.S  
**Register Number**: 412723205031  
**Institution**: Tagore Engineering College  
**Department**: Information Technology  
**Date of Submission**: 1st May 2025  
**GitHub Repository Link**: [Update the project source code to your GitHub Repository]

## 1. Problem Statement

Road accidents cause immense loss of life and property every year. Traditional methods of accident analysis are often reactive rather than preventive. This project aims to leverage AI to proactively analyze patterns in historical traffic accident data and predict the likelihood and severity of accidents under various conditions. This is a classification problem, where the goal is to predict accident severity (e.g., minor, serious, fatal) or the occurrence of an accident based on input features like weather, lighting, time, and road type. The solution can guide urban planners, traffic departments, and emergency services in making informed safety interventions.

## 2. Project Objectives
- Build machine learning models to predict accident severity or probability.
- Identify the key contributing factors (e.g., weather, road condition, time of day).
- Improve road safety by enabling data-driven decision-making.
- Ensure accuracy, interpretability, and real-world usability of the model.
- Incorporate insights from EDA to refine and optimize model features.

## 3. Flowchart of the Project Workflow

Data Acquisition → Preprocessing → Exploratory Data Analysis → Feature Engineering → Model Training → Model Evaluation → Interpretation → Reporting

## 4. Data Description
- **Dataset Name and Origin**: UK Road Safety Data (Kaggle)
- **Type of Data**: Structured tabular data
- **Number of Records and Features**: Over 1.5 million rows (2015–2020), 30+ features
- **Static or Dynamic Dataset**: Static dataset
- **Target Variable**: `Accident_Severity` (1 = Fatal, 2 = Serious, 3 = Slight)

## 5. Data Preprocessing
- **Merging**: Combined Accidents, Vehicles, and Casualties using `Accident_Index`.
- **Missing Values**: Handled using mode for categorical and median for numerical; removed rows with excessive missing data.
- **Encoding**: Used one-hot encoding for `Road_Type`, `Weather_Conditions`, etc.
- **Outlier Treatment**: Removed speed values outside the 1st–99th percentiles.
- **Type Conversion**: Converted date/time strings into datetime objects.
- **Normalization**: Scaled numeric features using `StandardScaler`.

## 6. Exploratory Data Analysis (EDA)
### Univariate Analysis
- Most accidents are classified as "Slight".
- Peak hours are between 4 PM–7 PM.

### Bivariate/Multivariate Analysis
- Fatal accidents increase under dark and wet conditions.
- Young drivers are involved in more accidents during late-night hours.
- Correlation between weather, lighting, and severity.

### Key Insights
- Poor lighting and adverse weather significantly increase accident severity.
- Road types like dual carriageways are safer than single carriageways.

## 7. Feature Engineering
- Extracted `Hour`, `Day`, `Weekday`, and `Month` from timestamp.
- Created interaction terms such as `Lighting × Weather`.
- Binned speed limits into Low, Medium, High categories.
- Removed features with high multicollinearity.
- Used PCA to reduce dimensionality (kept 95% variance).

## 8. Model Building
### Algorithms Used:
- Logistic Regression (baseline)
- Random Forest Classifier
- XGBoost Classifier

### Data Split:
- 80% Train, 20% Test (Stratified by severity)

### Metrics Used:
- Accuracy
- Precision, Recall, F1-Score
- ROC-AUC Score
- Confusion Matrix

## 9. Visualization of Results & Model Insights
- **Confusion Matrix**: To assess classification accuracy and errors.
- **ROC Curves**: XGBoost had the highest AUC score (~0.88).
- **Feature Importance**:
  - Top factors: Road surface, light conditions, speed limit, hour of the day
- **SHAP Values**: Used for understanding prediction logic for individual samples.

## 10. Tools and Technologies Used
- **Programming Language**: Python
- **IDE/Notebook**: Google Colab, Jupyter Notebook
- **Libraries**: pandas, numpy, seaborn, matplotlib, scikit-learn, XGBoost, etc.
- **Visualization Tools**: Pyplot, matplotlib.

## 11. Team Members and Contributions
- **Data cleaning** - Shrilekha.S
- **EDA** - Rachel.R
- **Feature Engineering** - Soumya.P
- **Model Development** - Logasri.J
- **Documentation and Reporting** - Monisha.S
