# House-Price---Regression

House Price Estimation by Regression

Introduction

Purchasing a home is seen as a symbol of financial success. Owning a home has been a dream for many people as early as the 1950’s. However, today’s economy has changed tremendously from the past, making it much more difficult to achieve this goal. When considering taking the step to buy a house, there are many characteristics that may influence a buyer's decision. With prices of properties increasing exponentially, it becomes essential to study the factors which directly or indirectly affect when a customer decides to buy a house and to predict the market trend. In general, for any purchase, a potential customer makes a decision based on the value of the purchase for the sale price.

Research Question

Which factors are the most important in determining the sale price of a home?

Data Description

Our data set is a listing of various residential homes from Ames, Iowa with 81 different factors that people would use to determine when buying a house, everything from utilities to fence material.

The dataset was obtained from a past Kaggle competition called House Prices - Advanced Regression Techniques. The original data set can be found here: https://www.kaggle.com/c/house-prices-advanced-regression-techniques/overview

In our dataframe, there are 1460 houses recorded and categorized by 81 characteristics. Of the 81 characteristics, we can observe that there are 35 numeric variables and 46 character/factor variables.

Methods

Because our data set consisted of 81 variables, the way that we narrowed down most of them was by logic. As individuals who are interested in purchasing homes in the future, we evaluated which factors were the most important to us when it came to buying a home. We assumed that the factors that were most important to us might result in the sale price being increased.

The distribution of each remaining variable was examined.Variables that were skewed or had large amounts of missing observations were excluded from the model. Some categories had a definition of ‘NA’ thus it was hard to determine if they were missing or not, thus those variables were excluded. The remaining variables underwent data cleaning. Column names were changed and character variables mistakenly stored as numeric were converted into factors.

Model selection methods were used to obtain the best model. A step wise regression method was carried out. An additional method used was obtaining different models and observing which one best explained the variability of sale price.

Results

Using best subset selection method, we compared 5 models which explains the percentage of variance by X variables that affects sale price. The model that pertains the value of 0.693 has 5 variables and would probably not be the best selection as there are similar variance values with fewer variables. For instance, the model that pertains to 0.684, consists of garage cars, year remodeled, total rooms, and overallquality(Good quality in particular).

Discussion/ Limitations/ Future Direction

When employing model selection methods, each method determined that neighborhood should be included in the model. However, neighborhood is a categorical variable that consisted of 25 categories. Without knowledge of Ames, Iowa, it would not have been appropriate to collapse any of the different variables into a single category. An examination of the history of the Ames, Iowa area in terms of demographics and finances would be necessary in order to fully understand our neighborhood variable and understand the outside environment that impacts sale prices. Factors such as history, laws / politics and economics of an area influence the sale price of a house; unfortunately that type of examination is beyond the purview of this analysis. Thus, not being able to collapse the variable leaves for 25 extra parameters to be estimated in the model which is not efficient.

In a future study, with more knowledge both on spatial analysis and background information, this study could be redone to obtain a more accurate model. A future study could also involve the training of this data set and model in order to predict the sale price of homes in a different state. This study could also be repeated with a random forest method to obtain better accuracy.
