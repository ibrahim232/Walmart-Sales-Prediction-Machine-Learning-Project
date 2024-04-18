<h1 style="text-align:center;">Walmart Sales Prediction Machine Learning Project</h1>
<p align="center">
  <img src="https://s.yimg.com/ny/api/res/1.2/rXENBrYvTBAH53uub8.dvg--/YXBwaWQ9aGlnaGxhbmRlcjt3PTY0MDtoPTQyNw--/https://media.zenfs.com/en/fortune_175/392698f693225d44aa0a6e78b21dd53c" width="500" height="300">
</p>


1. [Data Overview](#data-overview)
2. [Importing Libraries](#importing-libraries)
3. [Data Cleaning & Preprocessing](#data-cleaning-and-preprocessing)
4. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
    - [Univariate Analysis](#univariate-analysis)
    - [Bivariate Analysis](#bivariate-analysis)
    - [Multivariate Analysis](#multivariate-analysis)
5. [Data Encoding](#data-encoding)
6. [Data Scaling](#data-scaling)
7. [Data Modeling](#data-modeling)
8. [Model Evaluation](#model-evaluation)
9. [Pipeline](#pipeline)
10. [Deployment](#deployment)


## Problem Statement
Predict the sales of Walmart stores.


## Tasks

### Hypothesis based EDA:
1. **Share of sales and profit by product category (top 5)**
   - Analyze the top 5 product categories for their sales and profit contributions.
2. **Share of profit by region**
   - Uncover the profit distribution across different regions.
3. **Share of sales and profit by product name (top 5)**
   - Determine the sales and profit shares of the top 5 product names.
4. **Plot the trend of sales and profit over time as a line chart**
   - Visualize how sales and profit have evolved over time.

### Create new features:
1. **Create average sales per category and average sales by region features and drop the category and region column**
2. **One-hot encode all the other categorical variables.**
3. **Standardize the numerical variables**

### Build Models and compare the results:
1. **Build a Linear Regression and Random Forest on the above data**
2. **Set the date as index and use only sales column to build ARIMA and SARIMA model**
3. **Use Facebook Prophet and build the model**

## FAQs

**Q1. How can I analyze the sales and profit distribution by product category?**
- Perform hypothesis-based EDA to identify the top 5 product categories' sales and profit shares.

**Q2. How can I determine the profit distribution by region?**
- Conduct an analysis to uncover the share of profit attributed to different regions.

**Q3. Which models can I build for sales prediction?**
- Use Linear Regression, Random Forest, ARIMA, SARIMA, and Facebook Prophet models to predict Walmart store sales.
  
By the end we got the following:
## Model Evaluation Results

We evaluated our predictive model using an `ExtraTreesRegressor`, which is part of a comprehensive pipeline that includes preprocessing and model fitting stages. Below, we discuss the key metrics used to quantify the model's performance on the test set.

### Mean Absolute Error (MAE): 39.5045

- **Description**: The Mean Absolute Error (MAE) represents the average absolute difference between the actual values (`y_test`) and the predictions (`y_pred`).
- **Interpretation**: A lower MAE suggests better model accuracy. Here, the average error the model makes in predicting the output variable is approximately 39.5 units. The acceptability of this score largely depends on the scale and context of the target variable.

### Mean Squared Error (MSE): 4827.7339

- **Description**: The Mean Squared Error (MSE) is the average of the squares of the errors—that is, the average squared difference between the actual values and the predicted values. MSE emphasizes larger errors more significantly due to squaring.
- **Interpretation**: With an MSE of about 4827.7, indicating the presence of some large errors. This suggests that when the model is inaccurate, it can be significantly so, which might be crucial if large errors are particularly undesirable in our application.

### Root Mean Squared Error (RMSE): 69.4819

- **Description**: The Root Mean Squared Error (RMSE) is the square root of the MSE and provides a measure of the magnitude of error in the same units as the target variable.
- **Interpretation**: With an RMSE of approximately 69.5, this value indicates how widely your predictions deviate from the actual values on average. Like the MAE, the acceptability of this number depends on the context.

### R-squared (R²): 0.8465

- **Description**: R², or the coefficient of determination, is a statistical measure of how well the regression predictions approximate the real data points.
- **Interpretation**: An R² of 0.8465 means that approximately 84.65% of the variation in the dependent variable is explained by the independent variables in the model. This is generally considered a good R² value, suggesting that your model explains a large portion of the variability in the target variable.

### Conclusion

Overall, the model is performing reasonably well, particularly in terms of R². However, the relatively high values of MSE and RMSE compared to the MAE suggest that there are some predictions where the error is quite large. This could potentially be addressed by further tuning the model's parameters, exploring different preprocessing techniques, or examining outliers in this dataset.
