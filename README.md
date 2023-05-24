# Predicting Sales for Food Items at Various Stores
## Steven Phillips
### Business Problem:
The problem explored in this project is to discover which of several features increase the sales at various stores.
### Data:
The data used for this project originates from:
https://datahack.analyticsvidhya.com/contest/practice-problem-big-mart-sales-iii/

The data items include several features including: item weights, item visibility, outlet types, outlet sizes, fat content and MRP.
## Methods
The data were prepared by eliminating duplicates and focusing on Item Weight, Item Visibility, MRP, Fat Content, and Outlet Location Type.  Outlet Establishment Year, Item Identifier, and Outlet Identifier were not included in the analysis or modeling, as they do not provide additional insights.
## Results 
This first image showcases the correlations between the numeric variables.
![image](https://user-images.githubusercontent.com/113748627/197235260-0b79b8f4-9f22-402d-9a50-14910e556440.png)

This next image showcases the distribution of the Item Weights, which have a high number near 12 ounces.
![image](https://user-images.githubusercontent.com/113748627/197235403-b45cc51e-cf7c-4977-bdf5-857b5d29df2d.png)

## Model
The model chosen is a Decision Tree Model with the hyperparameter depth tuned to 5.
The metrics for evaluation of our optimized Decision Tree Model of depth 5 on our test data are: Mean Absolute Error(MAE) 738.32, Mean Squared Error(MSE) 1,118,185.97, and Root Mean Squared Error(RMSE) of 1,057.44. The R2 value explaining the variability in our target data is 0.5947.
## Recommendations
The R2 score of our model is 0.5947, explaining 59.47 percent of the variability in our target data.
## Limitations & Next Steps
This R2 score of 0.5947 is not ideal, but was the highest of the models explored.  Additional data should be gathered on additional feautures that may provide more accurate predictions.

## Further Feature Exploration

Here is further exploration of the features of the chosen Decision Tree Model above, as well as the Linear Regression model:

## This graph shows the top 5 most impactful features to the Decision Tree Model:

![image](https://user-images.githubusercontent.com/113748627/214692068-a4f9d474-3a65-4514-b4b6-428e1b9a0ef1.png)

### Here are the top 5 most important features from the Decision Tree Model:

- Item_MRP 0.55
- Outlet_Type_Grocery_Store 0.33
- Outlet_Type_Supermarket Type3 0.12
- Outlet_Type_Supermarket Type1 0.003
- Item_Visibility 0.0002

## This graph shows the SHAP values from the Decision Tree Model as a bar graph:

![image](https://github.com/stp511/sales_prediction1/blob/main/Data/summary_plot_bar.png)

The top 5 SHAP values come from the same features identified in the top 5 feature importances - item_MRP, Outlet_Type_Grocery_Store, Outlet_Type_Supermarket Type3, Outlet_Type_Supermarket Type 1, and Item_Visibility

## This graph shows the SHAP values from the Decision Tree Model as a dot graph:

![image](https://github.com/stp511/sales_prediction1/blob/main/Data/summary_plot_dot.png)

The 3 most important features from this SHAP dot summary plot include Item_MRP, Outlet_Type_Grocery_Store, and Outlet_Type_Supermarket Type 3.

The distribution of Item_MRP values are symmetric in their impact on the model. The higher the Item_MRP the more impact the value is having to increase the sales price and the lower the Item_MRP the more impact the value is having to decrease the sales price.

Outlet_Type Grocery Store is having a different impact on the model according to this plot. Lower values are all having a smaller effect on increasing the sales price, whereas higher values are having a higher impact decreasing the sales price.

Outlet_Type_Supermarket Type 3 is having the reverse effect as Outlet_Type Grocery Store. Higher values are all having a smaller effect on decreasing the sales price, whereas lower values are having a higher impact on increasing the sales price.


## This graph shows the top 10 most impactful coefficients from the Linear Regression Model:

![image](https://user-images.githubusercontent.com/113748627/214691940-7f75fd8b-9174-4df2-913d-d1cd385692dd.png)

### The top 3 most impactful features from the Linear Regression model:

The 3 most impactful features are Outlet_Type_Grocery_Store, Outlet_Type_Supermarket3, and Item_MRP.

The coefficient for Outlet_Type_Grocery_Store -1716.21.  This means that if all other variables remain fixed, the predicted sales will be $1,716.21 lower from a grocery store.

The coefficient for Outlet_Type_Supermarket3 is 1,582.35. This means that if all other variables remain fixed, the predicted sales will be $1,582.35 higher from a Supermarket 3 store.

The coefficient for Item_MRP is 965.76.  This means that if all other variables remain fixed, the predicted sales will increase by $965.76 for each additional $1 in Item_MRP. 

### For further information
For any additional questions, please contact me above.
