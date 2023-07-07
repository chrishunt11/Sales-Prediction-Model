# Production Sales and Insights
## Analyzing Product Sales 

**Author**: Christopher Hunt

### Business problem:

A problem retailers often run into is how to increase their sales. Within this problem there are subproblems they need to focus on. One being able to figure out which products are worth selling. Another being able to figure out which Outlets play a crucial role in increasing sales. There are many factors that come into play when deciding what to sell and where to sell it.

### Data Source:

Big Mart Sales Prediction: https://datahack.analyticsvidhya.com/contest/practice-problem-big-mart-sales-iii/

For this dataset there were 8523 rows and 12 columns

### Data Dictionary
<p align = "center"> 
  <img width="429" alt="Data Dictionary" src="https://github.com/chrishunt11/Prediction-of-Product-Sales/assets/123383359/06c0f6b5-b1be-4a6d-8712-6cff3262a07c">
</p>

### To prepare this data, the data was cleaned, and the following processes were performed:

#### Exploratory Data Analysis

- During the exploratory data analysis, a histogram and a boxplot was visualized for Outlet Sales, MRP, Visibility, Outlet Type, and Outlet Location.
- Also, countplots were visualized for the Outlet location and Type.
- This gave good baseline for all the Sales of the Products and the count for the Location and Type.

![Visibilitypng](https://github.com/chrishunt11/Prediction-of-Product-Sales/assets/123383359/74f27d5c-bcf8-4361-b380-8a585a00707d)

This visual shows that the majority of the products have a visibility percentage of about 3 percent.

#### Explanitory Data Analysis

- During the Explanitory data analysis, a boxplot and histogram was visualized for each numeric datatype column.
- Also, a countplot was visualized for each categorical column.
- This gave a good baseline for all of the numeric and caegorical columns for univariate and multivarite EDA.


![OutletType](https://github.com/chrishunt11/Prediction-of-Product-Sales/assets/123383359/b4e7c2ae-caaf-4417-af36-e41f3b23f410)


This visual shows that majority of the stores are SuperMarket Type 1.

 ### Maching Learning Using the Following Models:
    - Linear Regression Model
    - Random Forest Regressor Model
    - Tuned Random Forest Regressor Model

## Models Evaluated & Results

- Linear Regression Model (Testing Set):
  - R^2 = 0.570
  - MAE = 802.048
  - MSE = 1,186,964.271
  - RMSE = 1,089.479

- Random Forest Model (Testing Set):
  - R^2 = 0.554
  - MAE = 773.627
  - MSE = 1,229,857.716
  - RMSE = 1,108.990

- Tuned Random Forest Model (Testing Set):
  - R^2 = 0.595
  - MAE = 736.676
  - MSE = 1,116,454.429
  - RMSE = 1,056.624

- The Final Model Chosen was a 'Random Forest Regressor Model' with the n_estimators tuned to 150.
- For the testing model '59.5%' of the variance in y was explained by X.
- The Mean Absolute Error was off by about '$736.68'
- The Mean Squared Error was '$1,116,454.43'.
- The Root Mean Squared Error had a calculation of '$1,056.62'

Using this model 

Refer to the metrics to describe how well the model would solve the business problem

## Recommendations:

More of your own text here


## Limitations & Next Steps

More of your own text here


### For further information


For any additional questions, please contact **email**
