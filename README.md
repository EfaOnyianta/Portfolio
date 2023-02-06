# Food Data Analysis
## Understanding the properties of Products and values to increase sales 

**Efa Onyianta**

### Running sucessful groceries stores are hard and following food trends is never easy.

We will be analyzing current store stats can show us the trends we need to stay ahead of the trending curve and give the people what they want when it comes to grocery stores and grocery store items. As well as boost sales where needed. 


Here is where you state the business problem you were trying to solve


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

##Exploratory Data Analysis
With the exploratory data analysis a histogram, boxplot and a heat map were used to visualize the data and try to see what trends were easioy visualized in the data.  


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


#### Maching Learning Using the Following Models:
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

> Sentence about visualization.

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

The final chosen was Random Forest with the max _depth of 5

For the testing the R2 was .62 on test and .60 on test with a variance or .02
The MAE was off by .15
The MSE by .12
The RMSE was off by .06
The Random forest model was the best firt for the data on hand, the other models were very prone to over fitting even with tuning, as well as had larger gaps in error. 


## Recommendations:

I think that looking at the data on hand, maybe a health food store would be a great new endevour for the comapny with how well more " healthy" items sell. 
I also recommend we get more revelant data to visualize and predit sales, the other models ovetfitting so easily mad eme suspisious that there is not enought relevant data regarding sales in this data. 


## Limitations & Next Steps

More of your own text here


### For further information


For any additional questions, please contact **email**
