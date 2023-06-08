# Food Data Analysis
## Understanding the properties of Products and values to increase sales 

**Efa Onyianta**

### Running sucessful groceries stores are hard and following food trends is never easy.

We will be analyzing current store stats can show us the trends we need to stay ahead of the trending curve and give the people what they want when it comes to grocery stores and grocery store items. As well as boost sales where needed. 




### Data Source:
Big Mart Sales predictions: https://datahack.analyticsvidhya.com/contest/practice-problem-big-mart-sales-iii/

This dataset has 8523 rows and  12 columns 


Data Dictionary

Variable Name  | Description

Item_Identifier:  |  Unique product ID

Item_Weight: |   Weight of product

Item_Fat_Content:    |Whether the product is low fat or regular

Item_Visibility:  | The percentage of total display area of all products in a store allocated to the particular product

Item_Type:    | The category to which the product belongs

Item_MRP:   |   Maximum Retail Price (list price) of the product

Outlet_Identifier:     |  Unique store ID

Outlet_Establishment_Year:      |  The year in which store was established

Outlet_Size:    |    The size of the store in terms of ground area covered

Outlet_Location_Type:     |  The type of area in which the store is located

Outlet_Type:     | Whether the outlet is a grocery store or some sort of supermarket

Item_Outlet_Sales:    |   Sales of the product in the particular store. This is the target variable to be predicted.

Item_Outlet_Sales:     | Sales of the product in the particular store. This is the target variable to be predicted.



### To prepare this data it was inspected and cleaned and the following processes were executed:

## Exploratory Data Analysis

With the exploratory data analysis, a histogram, boxplot and a heat map were used to visualize the data and try to see what trends were easioy visualized in the data.  


![image](https://user-images.githubusercontent.com/119267803/216891881-0810966e-5ed2-4fd1-a9af-91d34e3cd746.png)

This heat map shows the there was a .57 coefficient which indicates there is a moderate correlation between item outlet sales and item MRP. 



## Explanatory Visuals 
Explanatory Visuals and Analysis
We have cleaned the data and explored soem of the data and its patterns. Now its tiem to answer some questions

Questions:
Do " healthy" items sells more?

What items are most popular?
Do people prefer to buy low fat?
## Results: 

![image](https://user-images.githubusercontent.com/119267803/216892341-39a5244a-f311-4d99-b95c-294357b65a4b.png)

When it came to most popular items startchy foods came out on top! However seafood and fruits and veggies were close behind. 


The below visual shows if people prefer to buy lowfat, the numbers are very close and low fat items are popular, however regular items came out on top. 

![image](https://user-images.githubusercontent.com/119267803/216892559-7c0b18ef-8716-4ebf-8d15-2a55ddd20e6f.png)


#### Machine Learning Using the Following Models:
- Linear Regression Model
- Decision Tree Regressor Model
- Tuned DC Regressor Model
- Random Foredt Regressor Model
- Tuned RF Regressor Model


## Linear Regression
LinearRegression Train Scores
MAE: 847.9745 
MSE: 1,301,679.8610 
RMSE: 1,140.9119 
R2: 0.5602

LinearRegression Test Scores
MAE: 802.3840 
MSE: 1,191,253.3383 
RMSE: 1,091.4455 
R2: 0.5682


### Linear reg coefficients were found and these are the findings

![linear reg coeff model](https://github.com/EfaOnyianta/Sales-Prediction/assets/119267803/aead4778-ae24-45be-a35c-a02c201c037d)

#### Interpretations
Intercept baseline is 32.0000

Coefficients that positively influenced sales
items from outlet location type 2 increased sales(target) by 26,085,566,229,045,636.0000

outlet identifier 046 increased sales by 17,071,672,556,909,728.0000

items at Outlet_Location_Type_Tier 1 increased sales by 13,930,311,360,866,674.0000

Outlet_Identifier_OUT049 increased sales by 13,606,551,902,381,064.0000

Outlet_Identifier_OUT027 increased sales by 11,410,880,334,032,572.0000

Outlet_Identifier_OUT019 increased sales by 10,763,474,688,825,006.0000

neg impact coefficients
items from Outlet_Type_Supermarket Type1 decreased sales by -16,562,415,776,203,718.0000

items from Outlet_Size_Small decreased sales -12,610,372,813,980,082.0000

items from Outlet_Type_Supermarket Type3 decreased sales by -10,600,180,468,797,778.0000

items from Outlet_Type_Grocery Store also decreased sales by -10,254,217,908,120,908.0000 accoring to this model.



## Decision Tree 
Decision Tree Model Train Scores
MAE: 0.0000 
MSE: 0.0000 
RMSE: 0.0000 
R2: 1.0000

Decision Tree Model Test Scores
MAE: 1,050.6124 
MSE: 2,333,646.4293 
RMSE: 1,527.6277 
R2: 0.1542

## Decision Tree Tuned
Decision Tree Model Train Scores
MAE: 762.6102 
MSE: 1,172,122.7729 
RMSE: 1,082.6462 
R2: 0.6039

Decision Tree Model Test Scores
MAE: 738.3173 
MSE: 1,118,185.9731 
RMSE: 1,057.4431 
R2: 0.5947


## Random Forest
Random Forest Model Train Scores
MAE: 296.8141 
MSE: 183,390.6859 
RMSE: 428.2414 
R2: 0.9380

Random Forest Model Test Scores
MAE: 763.3969 
MSE: 1,211,109.1273 
RMSE: 1,100.5040 
R2: 0.5610

### Random forest important features were found, these are the findings
![regression tree model feat imp](https://github.com/EfaOnyianta/Sales-Prediction/assets/119267803/2a24ab70-5995-47be-9cc5-19a6d435e77b)

### the top 5 features are
item type (breakfast)
Item type bread
Item weight
Items with regular fat content
items market retail price

## Global explainations

### Below are the Shap values for the random forest model and the values it predicted to be most impactful. 

![shap model](https://github.com/EfaOnyianta/Sales-Prediction/assets/119267803/23d13cfa-2121-44a0-8ec3-bd3af65f1ff8)

#### The features from shap vs feature importance my model are very different. They matched choosing Item mrp, item weight, and fat content regular but the importance/ impact is very different, for the shap values model item mrp is the most impactful vs on my feature importance model its the 5th most important. Item weight is the 6th most impactful in the shap values model but 3rd on my feature importance model. The also totally missed everything else. The feature importance model seems to have favored the categorical features more.

#### A dot plot was made to interpret the type of impact these features had on prediction (iif impactful in a negaive or postitive way) 


![shap dot plot](https://github.com/EfaOnyianta/Sales-Prediction/assets/119267803/89e35f22-ca12-4367-a81d-4c2a93eaae87)

#### - For the first feature it seems with item mrp the higher it was it decreased sales. Vs the blue values were more to the left meaning that the mrp being lower increased sales 

* For grocery store if grocery store == 1 (its a grocery store) the model predicts the sales seem to have improved/ better. if grocery store == 0 the sales werent decreased but the model thought they werent as good as it would if it was  a grocery store. 
* Super market type 3 was predicted to have a negative impact on sales, it predicted sales were better when it was anything but market type 3== 0 and worse if it was == 1

## Random Forest tuned
Random Forest Model Train Scores
MAE: 742.1276 
MSE: 1,111,048.2458 
RMSE: 1,054.0627 
R2: 0.6246

Random Forest Model Test Scores
MAE: 727.3509 
MSE: 1,099,882.7305 
RMSE: 1,048.7529 
R2: 0.6013

The final  model chosen was Random Forest with the max _depth of 5

For the testing the R2 was .62 on test and .60 on test with a variance or .02
The MAE was off by .15
The MSE by .12
The RMSE was off by .06
The Random forest model was the best fit for the data on hand, the other models were very prone to over fitting even with tuning, as well as had larger gaps in error. 


## Recommendations:

I think that looking at the data on hand, maybe a health food store would be a great new endevour for the comapny with how well more " healthy" items sell. 
I also recommend we get more revelant data to visualize and predit sales, the other models overfitting so easily made me suspicious that there is not enough relevant data regarding sales in this data. 


## Limitations & Next Steps

This is in the early steps of being hopefully a good model to look at for company growth and expansion oppurtunities. 


### For further information


For any additional questions, please contact **efaonyianta@gmail.com**
