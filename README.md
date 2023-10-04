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

## Coefficients

![coefficients](https://github.com/chrishunt11/Prediction-of-Product-Sales/assets/123383359/8713bebd-38db-468d-9648-a279ae5bbaff)

**1. Outlet_Type_Supermarket Type3 (Coefficient: 1,763.68):**

- The coefficient for "Outlet_Type_Supermarket Type3" is 1,763.68.
- This positive coefficient suggests that when the outlet type is "Supermarket Type3," it contributes significantly to an increase in "Item_Outlet_Sales."
- Sales in "Supermarket Type3" outlets are expected to be approximately $1,763.68 higher, on average, compared to other types of outlets when all other factors are held constant.

**2. Item_MRP (Coefficient: 965.06):**

- The coefficient for "Item_MRP" is 965.06.
- This positive coefficient indicates that for each unit increase in the Maximum Retail Price (MRP) of an item, "Item_Outlet_Sales" is expected to increase by approximately $965.06, on average, assuming all other factors remain the same.
- Items with higher maximum retail prices tend to have a significant positive impact on sales.

**3. Outlet_Size_High (Coefficient: 202.39):**

- The coefficient for "Outlet_Size_High" is 202.39.
- A positive coefficient for "Outlet_Size_High" suggests that when the outlet size is categorized as "High," it has a positive effect on "Item_Outlet_Sales."
- When compared to outlets to smaller sizes, outlets with a "High" size are associated with an average increase of approximately $202.39 in "Item_Outlet_Sales," assuming all other factors remain constant.



## Feature Importance
![Top_5_Importance](https://github.com/chrishunt11/Prediction-of-Product-Sales/assets/123383359/0f365450-a4b3-4c78-9f6d-09ea4c74d57e)


**1. Item_MRP (0.443900):**

- This feature has the highest importance score, which indicates that it has the most significant impact on "Item_Outlet_Sales."
- For each unit increase in the "Item_MRP" (Maximum Retail Price), we can expect, on average, an increase of approximately 0.443900 units in "Item_Outlet_Sales,". 
- This means that items with higher maximum retail prices tend to contribute more to total outlet sales.


**2. Outlet_Type_Grocery Store (0.196758):**

- This feature represents the type of outlet, specifically "Grocery Store."
- An importance score of 0.196758 suggests that the type of outlet being a "Grocery Store" is the second most important factor affecting "Item_Outlet_Sales."
- This indicates that sales in grocery stores significantly differ from other outlet types, and these stores have a notable impact on overall sales.


**3. Item_Visibility (0.096981):**

- "Item_Visibility" is the third most important feature, with an importance score of 0.096981.
- An increase in the visibility of items on the shelves (e.g., through better placement or promotion) is associated with an average increase of approximately 0.096981 units in "Item_Outlet_Sales." 
- Making items more visible to customers can positively influence sales.


**4. Item_Weight (0.053452):**

- "Item_Weight" has an importance score of 0.053452, making it the fourth most important feature.
- This suggests that the weight of the item has a moderate impact on sales. An increase in item weight is associated with an average increase of around 0.053452 units in "Item_Outlet_Sales."
- Heavier items may have a slight positive influence on sales.

**5. Outlet_Type_Supermarket Type3 (0.029663):**

- This feature represents a specific type of supermarket outlet, "Supermarket Type3."
- With an importance score of 0.029663, it is the fifth most important feature.
- The presence of "Supermarket Type3" outlets is associated with an average increase of approximately 0.029663 units in "Item_Outlet_Sales."
- This indicates that the sales in Supermarket Type3 outlets differ from other types and contribute moderately to overall sales.


### SHAP Bar Plot Interpretation
![shap-feature-value](https://github.com/chrishunt11/Prediction-of-Product-Sales/assets/123383359/1d96943d-505b-4e08-ab0f-76db4a984742)
![shap-summary-plot](https://github.com/chrishunt11/Prediction-of-Product-Sales/assets/123383359/7d639b18-469a-4993-9107-736b29208d6c)

- The top 3 most important features are as follows:
    - Item_MRP
    - Outlet_Size_Medium
    - Item_Weight

- Item_MRP:
    - The higher an item_MRP (red dots), the more likely it is to positively impact our predictive model

- Outlet_Size_Medium:
    - The higher count of an item being sold at a medium sized store(red dots), it will positively impact our prediction

- Item_Weight:
    - A central cluster of our values with mixed feature value colors indicates an average/typical impact on the model predictions


## Local Models

- Item_MRP (selected since it is ranked as the most impactful to predictions)
- Item_Weight (selected since the values reflected in the summary plot are bunched up and could use additional clarification)
- Item_Visibility (selected to gain additional insight on store placement combined with parameters above leading to higher/lower sales) the combinations above can give additional insight on larger/bulkier items costing less vs smaller items that cost more and if placement has an overall impact on the two features.

**Using products that are:**
  - higher / lower than average Item_MRP, higher / lower than average Item_Weight, higher / lower than average Item_Visibility

- Group 1:
    - less expensive, larger, and less visable
- Group 2:
    - more expensive, smaller, more visable

### Group 1

#### Lime Tabular
<img width="401" alt="Screenshot 2023-10-02 140236" src="https://github.com/chrishunt11/Prediction-of-Product-Sales/assets/123383359/ab6c323a-640f-49a6-ae25-bd1eb5aed29e">



**Interpretation:**
- The plot above relates that the Item_MRP, having the item be sold at a small sized store, and having the item be sold at a high sized store will reduce the predicted value of the item. While item visibility, item being a breakfast type and the item being a snack food are influencers toward the item having a higher value.


#### Force Plot 
<img width="448" alt="Screenshot 2023-10-02 140247" src="https://github.com/chrishunt11/Prediction-of-Product-Sales/assets/123383359/0a2932a0-360a-4b0f-8844-400d8f768796">


**Interpretation:**
- The plot above relates that this items main influence towards a higher predictions are Item_Visibility, Item_Type_Snack_Foods, and Item_Weight while item_mrp is opposing that force along with the item being sold in a medium sized store.



### Group 2
#### Lime Tabular
<img width="457" alt="Screenshot 2023-10-04 150455" src="https://github.com/chrishunt11/Prediction-of-Product-Sales/assets/123383359/cf3d2646-2cfc-4485-ad1e-1998b23072f8">

**Interpretation:**
- The plot relates that this items main influence for a higher prediction is the Item_MRP, the item being a seafood type, and the item being a fruits and vegetables type. 
- The plot also relates an additional loss in predicted value in outlet size for all three categories (small - 167.27, medium - 225.19, high - 100.78) with the largest lost occuring in the medium sized store.


#### Force Plot 
<img width="457" alt="Screenshot 2023-10-04 150500" src="https://github.com/chrishunt11/Prediction-of-Product-Sales/assets/123383359/effe3469-97af-4290-aae6-24b8fdbbe5c0">
- The above plot relates the largest contributors to the loss in the projected value for this item being a medium sized store and a small sized store. 
- The item_mrp is a positive enough factor that it is able to increase the predicted value.

##### Contact information:

For any further inquiries or information, please contact:
- Christopher Hunt Jr.
- LinkedIn Profile: [Christopher Hunt Jr. on LinkedIn](https://www.linkedin.com/in/christopher-hunt-jr)
- Email Address: cjhunt592.1@gmail.com
