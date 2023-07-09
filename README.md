![produce-stand](https://github.com/chrishunt11/Prediction-of-Product-Sales/assets/123383359/5f2fbe30-7e71-4c91-9223-8656b9eabed5)


# Production Sales and Insights
## Analyzing Product Sales 

**Author**: Christopher Hunt

### Business problem:

A challenge retailers often run into is how to continually increase their sales. Within this problem there are subproblems they need to focus on. One is to figure out which products are worth selling; another is to figure out which outlets play a crucial role in increasing sales. There are many factors that come into play when deciding what to sell and where to sell it.

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
- Also, a numerous barplots are visualized to get a better understanding of which outlet type and size have the most sales.
- This gave a good baseline for all of the numeric and categorical columns for univariate and multivarite EDA.


![Mrp-OutletSales](https://github.com/chrishunt11/Prediction-of-Product-Sales/assets/123383359/94e0aeef-f97a-4c0e-8ce0-5dd8bee14070)


This visual shows that the greater the MRP price the greater the Outlet Sales.


![tot-sale-item](https://github.com/chrishunt11/Prediction-of-Product-Sales/assets/123383359/bd5decf4-f20b-4582-92f2-1f8cf5c3d2a9)


The top five highest earning sales per item type are as follows:
- Fruits and Vegetables:    `$2,820,059.82`
- Snack Foods:              `$2,732,786.09`
- Household:                `$2,055,493.71`
- Frozen Foods:             `$1,825,734.79`
- Dairy:                    `$1,522,594.05`

The bottom five highest earning sales per item types are as follows:
- Hard Drinks:               `$457,793.43`
- Starchy Foods:             `$351,401.25`
- Others:                    `$325,517.61`
- Breakfast:                 `$232,298.95`
- Seafood:                   `$148,868.22`

![sales-outlet-size](https://github.com/chrishunt11/Prediction-of-Product-Sales/assets/123383359/329fe0f0-8673-4557-977f-ae904d28268f)

This barplot shows that the most sales were at Medium sized stores.


In order, the outlet sales per outlet size are as follows:
- Medium:          `$7,489,718.69`
- Small:           `$4,566,212.20`
- High:            `$2,142,663.58`


![sales-outlet-type](https://github.com/chrishunt11/Prediction-of-Product-Sales/assets/123383359/0fc0cdc9-532c-40ba-99ff-bd9c765730b2)


This barplot shows that majority of the outlet sales were at Supermarket type 1.


In order, the outlet sales per outlet type are as follows:
- Supermarket Type 1:	    `$12,917,342.26`
- Supermarket Type 3:	    `$3,453,926.05`
- Supermarket Type 2:	    `$1,851,822.83`
- Grocery Store:	        `$368,034.27`


After viewing which type of outlet has the most sales, it is also important to take a look at how many of each outlet types there are to gain more knowledge.


![tot-outlet-type](https://github.com/chrishunt11/Prediction-of-Product-Sales/assets/123383359/1e59cc89-c3a0-452f-acb9-ac87c609688f)


In order, the count of the Outlet Type are as follows:
- Supermarket Type 1:       `5,577`
- Grocery Store:            `1,083`
- Supermarket Type 3:       `935`
- Supermarket Type 2:       `928`

After viewing the countplot we can see that there are over five times the amount of Supermarket Type 1 stores than any other store.


After seeing Supermarket Type1 has over five times the amount of stores, I looked into the average Sales per Store to see if Supermarket Type 1 had the greatest average sales as well.

![avg-sale-type](https://github.com/chrishunt11/Prediction-of-Product-Sales/assets/123383359/710e51bb-f5bf-4d45-8609-89822ca8d400)

In order, the average Sales per Outlet Type are as follows:
- Supermarket Type3        `$3,694.04`
- Supermarket Type1        `$2,316.18`
- Supermarket Type2        `$1,995.50`
- Grocery Store            `$339.83`

This barplot shows that Supermarket Type 3 has the highest average per store despite having the second least amount of stores.

 ### Maching Learning Using the Following Models:
    - Linear Regression Model
    - Bagged Tree Regressor Model
    - Tuned Bagged Tree Regressor Model
    - Random Forest Regressor Model
    - Tuned Random Forest Regressor Model

## Models Evaluated & Results

- Linear Regression Model (Testing Set):
  - R^2 = 0.570
  - MAE = 802.048
  - MSE = 1,186,964.271
  - RMSE = 1,089.479

- Bagged Tree Regressor Model (Testing Set):
  - R^2 = 0.526
  - MAE = 795.198
  - MSE = 1,306,771.261
  - RMSE = 1,143.141

- Tuned Bagged Tree Regressor Model (Testing Set):
  - R^2 = 0.578
  - MAE = 756.837
  - MSE = 1,163,912.604
  - RMSE = 1,078.848 

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

Using this model to make predictions about what Products to sell at which Outlet Location and Type would not be very reliable. After reviewing the regression metrics on how well the model performed, there is a disparity between the R^2 score.

## Recommendations:

- There appears to be a moderate correlation between Item MRP and Item Sales. If a retailor were to look to increase their Sales, one thing they could try doing is increase the Item MRP.
- After visualizing the average sales per Outlet Type, Supermarket Type 3 had the greatest average sale. A retailor might want to look into this and could look to sell products in more Supermarket Type 3 stores.

Model Performace 
- Overall, the best model is definitely the tuned Random Forest Regressor Model. The model is a moderatetly over fit, but it by far it outperformed the Linear Regression Model and the Bagged Tree Regressor Model.


## Limitations & Next Steps

- From here, a student could use the insights from the visuals on how to increase the Sales and could look for more correlations within the data.
- A student could go more in depth on which items are in sold most in each Outlet store type and potientially be able to find a correlation between products sold at certain stores.

### For further information


For any additional questions, please contact:
- Christopher Hunt Jr.
- cjhunt592.1@gmail.com
