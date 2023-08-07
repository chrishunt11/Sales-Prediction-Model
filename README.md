![Fruit_Stand](https://github.com/chrishunt11/Prediction-of-Product-Sales/assets/123383359/5f69a2bf-9a8f-47f1-bd6b-ec0966a711a0)

# Production Sales and Insights
## In-Depth Analysis of Product Sales 

**Author**: Christopher Hunt

### Business Problem:

In the realm of retail, the consistent enhancement of sales performance remains a formidable challenge. This multifaceted challenge encompasses subproblems such as discerning viable products for sale and identifying pivotal outlets that drive sales. Within this intricate landscape, the interplay of factors governing product selection and strategic outlet placement becomes paramount.

### Data Source:

Source: Big Mart Sales Prediction - https://datahack.analyticsvidhya.com/contest/practice-problem-big-mart-sales-iii/

The dataset comprises 8523 rows and 12 columns.

### Data Dictionary
<p align = "center"> 
  <img width="429" alt="Data Dictionary" src="https://github.com/chrishunt11/Prediction-of-Product-Sales/assets/123383359/06c0f6b5-b1be-4a6d-8712-6cff3262a07c">
</p>

### Data Preparation and Exploratory Data Analysis:

#### Exploratory Data Analysis

- During the exploratory data analysis, visualizations such as histograms and box plots were employed for key parameters such as Outlet Sales, MRP, Visibility, Outlet Type, and Outlet Location.
- Count plots were employed to visualize the distribution of Outlet location and type.
- These efforts provided a foundational understanding of sales distribution and location/type counts.

![Visibilitypng](https://github.com/chrishunt11/Prediction-of-Product-Sales/assets/123383359/74f27d5c-bcf8-4361-b380-8a585a00707d)

This visualization highlights that the majority of products exhibit visibility percentages around 3 percent.

#### Explanatory Data Analysis

- In-depth examination through box plots, histograms, and bar plots facilitated insights into numeric and categorical columns' distribution.
- Bar plots illuminated the outlet types and sizes with the most significant sales.
- This stage of analysis laid the groundwork for both univariate and multivariate explorations.

![tot-sale-item](https://github.com/chrishunt11/Prediction-of-Product-Sales/assets/123383359/bd5decf4-f20b-4582-92f2-1f8cf5c3d2a9)

The top five highest-earning sales per item type are:
- Fruits and Vegetables:    `$2,820,059.82`
- Snack Foods:              `$2,732,786.09`
- Household:                `$2,055,493.71`
- Frozen Foods:             `$1,825,734.79`
- Dairy:                    `$1,522,594.05`

![sales-outlet-type](https://github.com/chrishunt11/Prediction-of-Product-Sales/assets/123383359/0fc0cdc9-532c-40ba-99ff-bd9c765730b2)

This bar plot underscores that the majority of outlet sales are from Supermarket Type 1.

### Machine Learning Using the Following Models:
  - Linear Regression Model
  - Bagged Tree Regressor Model
  - Tuned Bagged Tree Regressor Model
  - Random Forest Regressor Model
  - Tuned Random Forest Regressor Model

## Models Evaluated & Results:

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
- For the testing model, '59.5%' of the variance in y was explained by X.
- The Mean Absolute Error was approximately '$736.68'.
- The Mean Squared Error was '$1,116,454.43'.
- The Root Mean Squared Error calculated as '$1,056.62'.

Utilizing this model for predictions on product sales and optimal outlet selection necessitates careful consideration, given the disparities in R^2 scores.

## Recommendations:

- A moderate correlation between Item MRP and Item Sales was discerned. Retailers could potentially boost sales by strategically increasing Item MRP.
- Considering the superior average sale in Supermarket Type 3, retailers might explore expanding their product offerings in this outlet category.

## Limitations & Next Steps:

- Further exploration of sales correlations and in-depth product-outlet analyses could unveil additional insights.
- An inquisitive student might investigate the possibility of correlating product sales with specific outlet sizes and types.

### For Further Information:

For any further inquiries or information, please contact:
- Christopher Hunt Jr.
- [LinkedIn](https://www.linkedin.com/in/christopher-hunt-jr)
- Email: cjhunt592.1@gmail.com
