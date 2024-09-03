# Financial Data Analysis and Forecasting using Clustering, Classification, and ARIMA Models

## Project Overview

This project focuses on analyzing financial data, performing clustering and classification on lenders, and forecasting future financial trends. The dataset used contains information on lenders, including `amount_to_repay`, `amount_paid`, `payment_date`, `loan_status`, and `loan_due_date`. The tasks undertaken include data cleaning, exploratory data analysis (EDA), feature engineering, clustering, classification, and time series forecasting using the ARIMA model. The results are intended to provide insights into lender behavior and predict future payment patterns.

## Project Objectives

1. **Data Cleaning and Preprocessing:** 
   - Handle missing values, normalize numerical features, and encode categorical variables.
   - Prepare the dataset for further analysis and modeling.

2. **Exploratory Data Analysis (EDA) and Feature Engineering:** 
   - Perform EDA to uncover patterns and insights in the data.
   - Engineer relevant features to improve model performance.

3. **Clustering and Classification:**
   - Perform clustering using K-means and DBSCAN algorithms to group similar lenders.
   - Evaluate clustering models using metrics like Silhouette Score, Davies-Bouldin Score, and Within-Cluster Sum of Squares (WCSS).
   - Apply supervised machine learning models (Decision Tree, Logistic Regression, Random Forest) to classify lenders based on their activity.

4. **Time Series Forecasting:**
   - Use the ARIMA model to forecast the `amount_to_repay` and `payment_date` for lenders.
   - Evaluate the model's performance using statistical metrics.

## Datasets

The dataset includes the following key features:
- `amount_to_repay`: The total amount that needs to be repaid by the lender.
- `amount_paid`: The amount that has already been paid by the lender.
- `payment_date`: The date of payment.
- `loan_status`: The current status of the loan.
- `loan_due_date`: The due date for the loan repayment.

## Methodology

1. **Data Cleaning and EDA:**
   - Clean the dataset by handling missing data and outliers.
   - Perform EDA to identify trends, correlations, and distributions.
   - Engineer features to improve the performance of clustering and classification models.

2. **Clustering:**
   - Implement K-means and DBSCAN clustering algorithms to group lenders based on their behavior.
   - Evaluate the clusters using metrics like Silhouette Score, Davies-Bouldin Score, and WCSS.
   - **Results:** 
     - K-means provided better-defined clusters with a higher Silhouette Score (0.996027) and a lower Davies-Bouldin Score (0.377538), although it had a higher WCSS (15689.602098) compared to DBSCAN.

3. **Classification:**
   - Apply Decision Tree, Logistic Regression, and Random Forest models to classify lenders.
   - **Results:**
     - **Decision Tree:** Achieved 96.98% accuracy, with a precision of 85.22% and a recall of 78.30% for active lenders.
     - **Random Forest:** Achieved 97.04% accuracy, with a precision of 85.37% and a recall of 79.21% for active lenders.
     - **Logistic Regression:** Achieved 95.31% accuracy but struggled to predict inactive lenders, with a precision of 0.60 and a recall of 0.01.

4. **Time Series Forecasting:**
   - Implement the ARIMA model for forecasting `amount_to_repay`.
   - **Results:**
     - The SARIMAX model was applied with an ARIMA(5, 1, 0) configuration, achieving a log likelihood of -182125.620 and an AIC of 364263.241. The model's residuals indicated a good fit, although the Jarque-Bera test suggested a departure from normality.

## Tools and Technologies

- **Programming Language:** Python
- **Data Manipulation and Analysis:** Pandas, NumPy
- **Visualization:** Matplotlib, Seaborn
- **Clustering:** scikit-learn (K-means, DBSCAN)
- **Classification:** scikit-learn (Decision Tree, Logistic Regression, Random Forest)
- **Time Series Forecasting:** statsmodels (ARIMA)

## Conclusion

The project successfully applied clustering, classification, and time series forecasting techniques to financial data, providing valuable insights into lender behavior and predicting future payment trends. The K-means clustering model and Random Forest classification model performed the best in their respective tasks. The ARIMA model effectively forecasted the amount to be repaid, although further refinement could improve its accuracy.

## Future Work

- **Model Improvement:** Explore more advanced clustering and classification algorithms to improve model performance.
- **Real-Time Forecasting:** Implement real-time forecasting to dynamically predict lender payments.
- **Expansion to Other Datasets:** Test the models on different financial datasets to validate their generalizability.

## How to Use

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/yourusername/Finance-Data-Analysis-Forecasting.git