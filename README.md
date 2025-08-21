# Insurance Cost Prediction Model

A machine learning project that predicts individual medical insurance costs using linear regression based on demographic and health factors.

## 🎯 Project Overview

This project analyzes the Medical Cost Dataset from Kaggle to build a predictive model for insurance charges. The model uses demographic information (age, sex, BMI, number of children, smoking status, and region) to estimate medical costs billed by health insurance companies.

## 📊 Dataset Information

- **Source**: Medical Cost Dataset from Kaggle
- **Size**: 1,338 observations with 7 features
- **Target Variable**: `charges` (individual medical costs)

### Features:
- `age`: Age of primary beneficiary (18-64)
- `sex`: Insurance contractor gender (male/female)
- `bmi`: Body Mass Index (kg/m²)
- `children`: Number of dependents covered
- `smoker`: Smoking status (yes/no)
- `region`: Residential area (northeast, southeast, southwest, northwest)
- `charges`: Individual medical costs (target variable)

## 🔍 Key Findings

### Correlation Analysis:
- **Smoking status**: Strongest predictor (correlation: 0.79)
- **Age**: Moderate correlation (correlation: 0.30)
- **BMI**: Weak correlation (correlation: 0.20)
- **Children**: Minimal correlation (correlation: 0.07)
- **Sex**: Negligible correlation (correlation: -0.06)

### Model Performance:
- **R² Score**: 0.75 (explains 75% of variance in test data)
- **RMSE**: $6,186.64
- **Selected Features**: Age and smoking status

## 🛠️ Technologies Used

- **Python 3.x**
- **Pandas** - Data manipulation and analysis
- **NumPy** - Numerical computing
- **Scikit-learn** - Machine learning library
- **Seaborn** - Statistical data visualization
- **Matplotlib** - Plotting library

## 📈 Model Development Process

### 1. Exploratory Data Analysis (EDA)
- Data quality assessment (no missing values found)
- Statistical summary and distribution analysis
- Correlation analysis between features and target variable

### 2. Feature Engineering
- Binary encoding for categorical variables (sex, smoker)
- Data type optimization (rounding BMI and charges to integers)
- Feature selection based on correlation analysis

### 3. Model Training
- Train-test split (80-20 ratio)
- Linear regression model implementation
- Model fitting on training data

### 4. Model Evaluation
- Performance metrics calculation (MSE, RMSE, R²)
- Residual analysis
- Test set evaluation

## 📊 Results

The linear regression model achieved:
- **Training R²**: 0.71
- **Test R²**: 0.75
- **Test RMSE**: $6,186.64

### Limitations Identified:
- Residual plots indicate non-linear relationships in the data
- Model may not capture complex interactions between features
- Limited feature set may not fully explain cost variations

## 🔮 Future Improvements

1. **Feature Engineering**: 
   - Create polynomial features to capture non-linear relationships
   - Explore interaction terms between variables

2. **Advanced Models**:
   - Random Forest or Gradient Boosting for better performance
   - Neural networks for complex pattern recognition

3. **Additional Features**:
   - Medical history information
   - Lifestyle factors
   - Geographic cost variations
