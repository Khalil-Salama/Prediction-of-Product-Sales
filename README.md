# Increasing product sales in different stores
## Sales pridection analysis

**Khalil Salama**

### Business problem:
Understand the properties of both products and outlets that significantly influence sales volumes. These include variables such as product type, price, weight, visibility on shelves. At the outlet level, characteristics like store size, location type, store establishment year, and outlet type (grocery store, supermarket, etc.) are considered to determine their impact on consumer buying behavior.

### Data
- Our stakeholders are:
  - retailers
- Their primary goal:
  - Increasing products sales based on our analysis.
- The stakeholders have provided us with:
  - A spreadsheet of various features of products, various stores types, as well as the sales of products in each particular store.
  - A Data Dictionary File
    - A data dictionary which lists the name and explanation for every feature in a dataset.
  
## Method
Data dictionary:
- Checking numeric features because sometimes they are stored as object dtype, so we will inspect the object columns next and look for columns that should be converted.
   - No object columns that needed to be converted to numeric.
- Checking the meaning of each feature
   - Please see the (Data Dictionary) File for full details.
- Checking if there is features that are not included in the data dictionary
  -  All the features are included.
- Checking if There erroneous index column that is not in the data dictionary,
  - No erroneous columns nothing should be dropped.
- Checking if there is features with ambiguous column names.
  - No ambiguous featurs were renamed for clarity.

Data information:
  - 8523 Rows
  - 12 columns
- there is a mixture of datatypes:
  - 4 float
  - 1 int
  - 7 object

Duplicate rows:
- There were no duplicate rows.

Missing values:

  - In the missingno matrix plot, we can see that there are only two columns that have missing values. ("Item weight" and "Outlet_size").

![download](https://github.com/user-attachments/assets/928aa6d6-87af-4656-aa79-1250206e791b)

Null Value Observations:

  - Item_weight and Outlet_size have a moderate percentage of null values (17% and 28%, respectively).
    - Item weight:
      - Noticed the relation between item identifier and item weight by taking more than 3 samples, so I replaced the null value in item weight by the weight that has the same Item identifier since the weights of each Item identifier are all the same.
    - Outlet size
      - All the null values of outlet size are for the years 1998, 2002 and 2007, clearly they are missing so I replaced them with 'missing'.
  
inconsistent values:

1) Categorical Features:
- Item_Fat_Contant
  - There were a small number of values in the Fat contant column that had "LF, low fat" instead of "Low Fat" and "reg" instead of "regular."
2) Numerical Features:
  - Item visibility: has a minimum value of 0.
  - Item visibility outliers
  - Also checking the minimum value of Item outlet sales its much lower than the 25% ( 33 - 843$ )
After inspecting we decided:
  - The 0.0 values in item visibility is an extrem value. replaced each with the mean of the each item identifier they belong too.(similer items mostely have similer visability) as proved in the data inspection.
  - Item Visibility outliers are mostly in Grocery Stores (Small space increases visibility percentge)
  - After checking the minimum value of 33 dollars in item outlet sales we found it normal because it represents the sales in grocery stores.(not extrem)

## Results

### Visual one: MRP relation to Outlet item sales

![download (2)](https://github.com/user-attachments/assets/5e8000b9-9afc-45c6-93f7-1d84929a88ea)


> MRP has the strongest coleration with item outlet sales.

### Visual two: Outlet type

![Outlet types](https://github.com/user-attachments/assets/f3328199-7218-48b1-9ad3-d6bbc0060e85)

> Supermarket type 3 sells the most.\

## Model

- The Final Model Chosen was Tuned Random Forest Regressor Model.

## Model Metrics

- Tuned Random Forest regressor Model (Training Set):
------------------------------------------------------------
- MAE = 756.192
- MSE = 1,152,558.818
- RMSE = 1,073.573
- R^2 = 0.611
  
- Tuned Random Forest Regressor Model (Testing Set):
-------------------------------------------------------------
 - MAE = 729.631
 - MSE = 1,091,228.789
 - RMSE = 1,044.619
 - R^2 = 0.604
   
- For the testing set on the model, 60.4% of the variance in Outlet item sales was explained by the features.

- The Mean Absolute Error was off by about $729.

- The Mean Squared Error was $1,091,228.

- The Root Mean Squared Error had a calculation of $1,070.

## Recommendations:

Using this model to predict Increasing products sales in various outlets types would be reliable because the R2 in the training set and the testing set are very close (no overfitting). but as mentioned before it can only predict about 60% of the varience in the target (Outlet item sales).





