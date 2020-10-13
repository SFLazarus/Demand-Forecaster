# Demand-Forecaster
Built a few forecasting models to determine the demand for a particular product.


# Problem Statement
### World Wide Products Inc. - Shipping and delivering to a place near you
1. Set up a data science project structure in a new git repository in your GitHub account
2. Download the product demand data set from
https://www.kaggle.com/felixzhao/productdemandforecasting
3. Load the data set into panda data frames
4. Formulate one or two ideas on how feature engineering would help the data set to establish additional value using exploratory data analysis
5. Build one or more forecasting models to determine the demand for a particular product using the other columns as features
6. Document your process and results
7. Commit your notebook, source code, visualizations and other supporting files to the git repository in GitHub

---

# Data Description
- Product_Code : The product name encoded
- Warehouse: Warehouse name encoded
- Product_Category: Product Category for each Product_Code encoded
- Date: The date customer needs the product
- Order_Demand:single order qty

## What are we doing?
- Train Time series models to forecast product demand

## Analysis:

#### Count of samples for warehouses 
![](https://github.com/SFLazarus/Demand-Forecaster/blob/main/reports/warehouse-count.png)

#### Product 1359's throughout demand:

![](https://github.com/SFLazarus/Demand-Forecaster/blob/main/reports/demand-of-product1359.png)

# Results:

## Linear Regression based Forecasting model:
### Performance on testing data:

![](https://github.com/SFLazarus/Demand-Forecaster/blob/main/reports/LR-predictions-testing-data.png)

-It performed worst on test data

### Performance on complete data:

![](https://github.com/SFLazarus/Demand-Forecaster/blob/main/reports/LR-predictions-complete-data.png)

- Even on training data didn't perform well

### R2 score:
- Training R2 score 0.00798308424338956
- Testing R2 score -0.001335919802511798

## Gradient Boosting based Forecasting model:
### Performance on testing data:

![](https://github.com/SFLazarus/Demand-Forecaster/blob/main/reports/GB-predictions-testing-data.png)

- Pretty good performance compared to LR based model

### Performance on complete data:

![](https://github.com/SFLazarus/Demand-Forecaster/blob/main/reports/GB-predictions-complete-data.png)

### R2 score:
- Training R2 score 0.852648878481129
- Testing R2 score -0.6673676260758077

## Conclusions and Further Developments:
- Linear Regression model performed worst
- Gradient Boosting model was good
- To further improve we can make use of recurrent neural networks(RNN) which I am sure would perform best in such scenarios.

---

# Project Structure:
### Readme.md
- Project description
### Data
- Contains link to dataset
### Notebooks
- Jupyter Notebook for Exploratory data analysis, Visualization, Feature Engineering and Forecasting Demand.
### Reports
- plot- warehouse sample count 
- Plot- Demand of Product 1359
- Plot- Linear Regression model predictions on testing data
- plot- Linear Regression model predictions on complete data
- Plot- Gradient boosting model predictions on testing data
- Plot- Gradient boosting model predictions on complete data
### Requirements.txt
- Info about Tools, frameworks and libraries required to reproduce the work flow
