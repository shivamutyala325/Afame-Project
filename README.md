"# Afame-Project" 

"Sales Prediction with Python"


This project builds a **regression-based machine learning system** to predict the **sales of a product** based on advertising expenditure in **TV, Radio, and Newspaper**. It uses both **Linear Regression** and **Random Forest Regressor**, comparing their performance to identify the best model.

---

## Project Overview

### Objective
To predict the number of units sold based on:
- TV advertising budget
- Radio advertising budget
- Newspaper advertising budget

---

## Flow of project

### 1. **Dataset**
- File: `Sales.csv`
- Columns:
  - `TV`: Advertising spend on TV (in thousands)
  - `Radio`: Advertising spend on Radio (in thousands)
  - `Newspaper`: Advertising spend on Newspaper (in thousands)
  - `Sales`: Units sold (target variable)

### 2. **Workflow**
- Load the dataset
- Clean the data (check for missing values)
- Analyze feature correlations
- Split the data into training and testing sets
- Train two regression models:
  - Linear Regression
  - Random Forest Regressor
- Evaluate both models using:
  - Mean Absolute Error (MAE)
  - Root Mean Squared Error (RMSE)
  - R² Score
- Predict sales on new/unseen data

---

## Example Prediction

added a sample data point to verify the prediction:

```python
new_data = pd.DataFrame({
    'TV': [200],
    'Radio': [25],
    'Newspaper': [30]
})

predicted_sales = rf_model.predict(new_data)
print(f"Predicted Sales: {predicted_sales[0]:.2f}")

