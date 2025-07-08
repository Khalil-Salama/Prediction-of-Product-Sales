# Increasing product sales in different stores
## Sales pridection analysis

**Khalil Salama**

### Business problem:

Our stakeholders are:

  - retailers

Their primary goal:

 - Increasing products sales based on our analysis.

The plan is to:

 - Understand the properties of both products and outlets that significantly influence sales volumes. These include variables such as product type, price, weight, visibility on shelves. At the outlet level, characteristics like store size, location type, store establishment year, and outlet type (grocery store, supermarket, etc.) are considered to determine their impact on consumer buying behavior.

### Data
- The stakeholders have provided us with:
  - A spreadsheet of various features of products, various stores types, as well as the sales of products in each particular store.
    - 8523 Rows
    - 12 columns
    - there is a mixture of datatypes:
      - 4 float
      - 1 int
      - 7 object
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
    
Duplicate rows:
  - There were no duplicate rows.

Missing values:

  - In the missingno matrix plot, we can see that there are only a two columns that have missing values. ("Item weight" and "Outlet_size").





### The sales prediction analysis aims to provide actionable insights into the key factors that drive sales performance of food items across different store locations. By leveraging historical sales data, product attributes, and store characteristics, the model forecasts future sales and identifies trends that can help the retailer understand the properties of products and outlets that play crucial roles in increasing sales.


### By understanding which combinations of product features and outlet attributes contribute most to high sales, the retailer can make more informed decisions around product placement, promotional planning, and supply chain management. This ultimately supports the goal of maximizing profitability and meeting consumer demand more effectively.


                                                      Two significant Visualizations


![MRP](https://github.com/user-attachments/assets/be898a0e-8fef-404b-8927-e70a2d84bd77)

And

![Outlet types](https://github.com/user-attachments/assets/f3328199-7218-48b1-9ad3-d6bbc0060e85)



