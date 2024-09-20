Refer https://github.com/jsathyan3245/PracticalApplicationAssignment111/blob/main/practical_application_II_starter_final/prompt_II_final.ipynb

# **Used Car Price Prediction Project**

## **Overview**
This project focuses on predicting used car prices using various regression models. By exploring and preprocessing a dataset of used cars, we aim to derive insights that can inform pricing strategies for used car dealers.

## **Steps Taken**

1. **Initial Data Inspection**
   - **Check Data Types:** Utilized `df.info()` to examine data types and missing values.
   - **Preview Data:** Displayed the first few rows using `df.head()` to understand dataset structure.

2. **Missing Data Exploration**
   - **Identify Missing Values:** Used `df.isnull().sum()` to check for missing data.
   - **Handling NaNs:** Decided on dropping or imputing missing values based on their extent.

3. **Distribution of Target and Features**
   - **Visualize Distributions:** Plotted histograms for numerical columns (price, year, odometer).
   - **Box Plots for Outliers:** Created box plots to inspect outliers in numerical features.
   - **Value Counts for Categorical Features:** Checked unique values and counts using `df[col].value_counts()`.

4. **Correlation Analysis**
   - **Correlation Matrix:** Calculated correlation matrix for numerical variables to identify relationships.

5. **Outlier Detection**
   - **IQR Method for Price:** Used interquartile range (IQR) to detect outliers in the price feature.

6. **Categorical Feature Encoding**
   - **One-Hot Encoding:** Converted categorical features into numerical format using One-Hot Encoding.

7. **Handling Duplicates**
   - **Check for Duplicates:** Used `df.duplicated()` to detect and drop duplicates.

8. **Irrelevant Columns**
   - **Remove Irrelevant Features:** Dropped columns with limited relevance (e.g., VIN, odometer, model, region).

9. **Feature Engineering**
   - **Map Categorical Features to Numerical Values:** Converted categorical features to meaningful numerical representations.

10. **Train-Test Split and Modeling**
    - **Train-Test Split:** Split data into training and test sets using `train_test_split()`.
    - **Model Pipelines:** Set up pipelines for each regression model (Linear, Lasso, Ridge, Random Forest) with integrated preprocessing.

## **Data Integrity Checks**
- **Final Check for Duplicates:** Confirmed no duplicate entries remain.
- **Final Check for Missing Values:** Ensured no columns contain missing values after imputation.

## **Feature Engineering**
- **New Feature Creation:** Considered creating features such as:
  - Age of the Vehicle
  - Odometer Value Normalization

## **Data Transformations**
- **Normalization and Scaling:** Applied standard scaling to numerical features and logarithmic transformation to the price if needed.

## **Final Data Preparation**
- **Define Features and Target:** Confirmed the correct definition of features (X) and target variable (y).
- **Pipeline Creation:** Ensured all preprocessing steps are encapsulated in a pipeline for consistency.

## **Model Training and Evaluation**
### **Selected Models:**
- Linear Regression
- Lasso Regression
- Ridge Regression
- Random Forest Regression

### **Performance Metrics:**
- Tracked metrics like Mean Squared Error (MSE) and R-squared for model comparison.

## **Conclusions**
1. **Model Performance Comparison:**
   - Random Forest: R² = 0.77, MSE = 33,530,825.06
   - Lasso & Ridge: R² ≈ 0.43, MSE ≈ 80,793,718.39
   - Linear Regression: R² = 0.45, MSE = 80,778,691.98

2. **Key Drivers of Price:**
   - Analyzed correlations, with notable influences from year and condition.

3. **Next Steps:**
   - Focus on Random Forest model and analyze feature importances.
   - Explore further data to enhance insights and model performance.

## **Reporting Findings**
This analysis provides actionable insights for used car dealers, emphasizing the importance of vehicle age and condition in pricing strategies.
