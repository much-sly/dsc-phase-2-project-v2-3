# HOUSING IN NORTHWESTERN COUNTY.

## NAME:  Sylvia Muchiri.

### OVERVIEW.

The King County housing data is a dataset that provides information about real estate properties in King County, Washington, USA. It is commonly used in the field of data analysis, particularly for studying housing market trends, predicting house prices, and exploring factors that influence property values. Some features included in the dataset that describe different aspects of residential houses. The main target variable is price which represents the monetary value which the property was sold.This makes the dataset suitable for regression analysis given the various features to be able to predict the value of a house. The dataset contains a lot of records of houses this allows for flexibility in model building and statistical analysis.

### BUSINESS AND DATA UNDERSTANDING.

#### a) Specifying The Data Analytics Question.
The data used in this analysis and the recommendations that come up can be used as a guide for people looking to buy houses in Northwester county. The findings will help guide customers on which are the best features to look at when considering buying a house in the aforementioned county.

#### b) Problem Statement.
What are the most important features to look for when seeking to buy a new home. Do renovations increase the price of a house? Is price dependent on the location? What aspects generally make a house more marketable?

#### c) Defining The Metric of Success.
This project will be considered a success if it can provide good recommendations that would help customers make good choices for houses and improve customer satisfaction with their choices. More than likely, these insights are all influenced ample knowledge following CRISPDM methodology.

The model will be considered a success if the R-squared is between 50-80% as well as looking at other metrics of success like mean absolute error, mean squared error, root mean squared error and the mean absolute percentage error.

#### d) Main Objective.
To find out which aspects of a house make it more marketable.

#### e) Specific Objectives.
a) Do renovations increase the value of a house.

b) Do any specific features play a role in the price of a house.

c) To find out what features are most important to consider when choosing a house.

#### f) Experimental Design.
. Data Collection: Importing the data needed.

. Read and check the data: using the necessary libraries to read the data

. Cleaning the data: Checking for null values and duplicates and dealing with them.

. Exploratory Data Analysis: Using univariate and bivariate analysis to see the correlations between the variables.

. Modeling : Building models that explore the relationships between the target variable and the independent variables.

. Regression results: Interpreting the results of the models to make insights on which are the best recommendations to customers.

. Conclusions: Drawing actionable insights from the results to be used to make decisions for the kinds of houses to buy.

#### g) Data Understading.
The dataset in this analysis is from:
. kc_house_data.csv

 Ample desription of the colums and what they describe about the entire dataset is contained in:
 . column_names.md

. The data is about housing in King county.

. The data has both categorical and numeric data.

The columns used in this analysis were either categorical or numerical and include:

id: unique identifier for a house.
price: Sale price (prediction target)
bedrooms: Number of bedrooms
bathrooms: Number of bathrooms
sqft_living: Square footage of living space in the home
sqft_lot: Square footage of the lot
floors: Number of floors (levels) in house
waterfront: Whether the house is on a waterfront
condition: How good the overall condition of the house is. Related to maintenance of house.
grade: Overall grade of the house. Related to the construction and design of the house.
yr_built:  Year when house was built.

This columns were cleaned, wrangled and later used to build models to provide insights on what features are the best to use when selecting houses.

### MODELLING.
Started off by building a simple linear regression model that takes in one independent variable and compares it against the target variable. The method used was OLS from sklearn and then prints out the summary to be able to interpret the results. The model yielded about 43% of variance in sales.
Next I built a multiple regression model that takes in 10 selected features that show the highest correlation with the target variable. The method used was splitting the data into testing and training data to be able to fit the model and print out the results. The model yielded about 52% of variance in sales.
The final model took in all the independent variables whixch included dummy variables created from the categorical variables. The total variables used was 22 against the targt variable. The method employed was OLS which I later printed out the summary. The model yielded about 66% of variance in sales which improved from the previous model.


### MODELLING RESULTS.
. The simple model linear regression model explains 43.6% using only one independent variable against the target variable.

. The second model which is a multiple regression model explains about 52% of variance in price. This model uses 10 selected independent variables against the target variable.

. The final model takes in all the idependent variables against the target variable and explains about 66.3% of variance in the price of houses.

. All the models are statistically significant with a probability f-statistic of below the threshold alpha value of 0.05%.

. For the final model however, it takes in all the variables where others are more significant in making the model while others are not for example bedrooms and condition poor have a very high p statistic indicating that they are not really significant to the model.

. The mean squared error of the third model is the lowest showing an improvement from the previous model indicating better performance.

. The model features were selected on the basis of correlation which might have some bias thus making the model to not perform as effectively.

. The final model however did not indicate the model to be as normal as indicated by the qqplot.


### 8. CONCLUSIONS.

The model that explains the highest variance in sales was the final model that takes into account multiple independent variables inclusive of those selected. However, some variables like bedrooms and condition poor proved to be insignificant for the model since their p statistic values are above the alpha value of 0.05.

From the models above, it is important to be careful during feature selection in order to be able to choose features that make a model perform exceptionally rather than optimally.

Square foot living and lot seemed to be significant when predicting the amount a house sells for also, if the condition is good and it has a waterfront the house seems to be selling for more. Thus when choosing a house clients should be keen on these features in order to make the right selection.

The final model was the best performing however it lacked some degree of normality which i think could be improved through transformations in order to make the model better performing.