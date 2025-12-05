# AI & ML Minor Project – Stock_Price_Trend_Analysis_and_Prediction

This repository contains my AI & ML minor project created during the **Skill Ladder Training and Internship Program**.  
The project demonstrates the complete workflow of a beginner–friendly machine learning pipeline:
data loading, cleaning, exploratory data analysis (EDA), feature engineering, model building,
evaluation, and visualization.

---

## Datasets Used

1. **Superstore Excel File**
   - Sheets:
     - `Orders` – detailed sales and order information
     - `People` – regional managers and their regions
     - `Returns` – returned orders by `Order ID`
   - Used to analyze:
     - Sales by region / category
     - Returns by region and manager
     - Overall business performance

2. **US_Stock_Data.csv**
   - Columns include:
     - `Date`
     - `Netflix_Price` (or similar)
     - `Crude_oil_Price`
     - `Natural_Gas_Price`
     - `Natural_Gas_Vol.`
   - Used for:
     - Time series analysis and visualization
     - Relationship between energy prices and stock price
     - Example plots: line plots, bar plots, histograms, pie charts

3. **Advertising.csv**
   - Columns:
     - `TV`, `Radio`, `Newspaper` (advertising budget)
     - `Sales` (units sold)
   - Used for:
     - Building a **Linear Regression** model
     - Predicting `Sales` based on advertising spend

---

##  Project Components

### 1. Data Loading and Cleaning

- Loaded Excel file with three sheets: `Orders`, `People`, `Returns`
- Created three DataFrames:
  - `df_orders`
  - `df_people`
  - `df_returns`
- Loaded `US_Stock_Data.csv` into a DataFrame
- Dropped unnecessary columns (e.g., `Unnamed: 0`)
- Handled missing values in numerical columns using **mean imputation**
- Converted the `Date` column to `datetime` and created:
  - `Year`
  - `Month`
  - `Day`

---

### 2. Exploratory Data Analysis (EDA)

####  Superstore Data (Sales & Returns)

- Basic summaries: total sales, average sales, number of orders
- Grouped analysis:
  - Sales by **Region**, **Category**, and **Sub-Category**
  - Returns joined with orders to analyze:
    - Returns by **Region**
    - Returns by **Manager**
- Example visualizations:
  - Bar charts for sales by region
  - Bar charts for count of returns by region/manager

#### US Stock & Energy Data

- Average **Netflix** price by **year** and **month**
- Time series plots for:
  - `Crude_oil_Price` over time
  - `Natural_Gas_Price` over time
- Visualizations for `Natural_Gas_Vol.`:
  - Bar plots
  - Scatter plot over time
- Combined line plot:
  - `Natural_Gas_Price` and `Crude_oil_Price` on the same graph
- Examples of:
  - Bar charts
  - Horizontal bar charts (`barh`)
  - Histograms
  - Pie charts

---

### 3. Predictive Analytics with Linear Regression

Using **Advertising.csv**:

1. **Introduction to Predictive Analytics and Linear Regression**
   - Concept of predictive analytics
   - Idea of fitting a line to data (simple linear regression)

2. **Sample Data and Initial Model**
   - Created a small synthetic dataset
   - Fitted a basic linear regression model
   - Visualized how the line fits the data

3. **Train–Test Split**
   - Split data into:
     - Training set
     - Testing set
   - Explained why testing on unseen data is important

4. **Model Training**
   - Features (`X`): `TV`, `Radio`, `Newspaper`
   - Target (`y`): `Sales`
   - Trained a `LinearRegression` model from `sklearn`

5. **Model Evaluation**
   - Predictions on the test set
   - Evaluation metrics:
     - **MAE** – Mean Absolute Error
     - **MSE** – Mean Squared Error
     - **RMSE** – Root Mean Squared Error
     - **R²** – Coefficient of Determination

6. **Visualization**
   - Actual vs Predicted Sales scatter plot
   - Residual plot to check error distribution

---

## Possible Extensions (Future Work)

- Try other models:
  - **Ridge** or **Lasso Regression**
  - **Random Forest Regressor**
- Add a **correlation heatmap** for all numerical features
- Create **monthly sales trends** using the `Orders` dataset
- Build a simple **dashboard-style notebook** with key charts at the top

---

## How to Run This Project in Google Colab

1. Open **Google Colab**:  
   `https://colab.research.google.com/`

2. Upload the notebook:
   - Go to **File → Upload Notebook**
   - Select `Stock Price Trend Analysis and Prediction.ipynb` (from this repo if downloaded)

3. Upload datasets:
   - Either:
     - Upload via Colab (**Files** panel → upload), or
     - Mount Google Drive and read files from there

4. Install any required libraries (if needed), for example:
   ```python
   !pip install pandas matplotlib seaborn scikit-learn

