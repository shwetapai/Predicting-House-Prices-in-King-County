# Predicting-House-Prices-in-King-County

I took the housing dataset which contains information about different houses in King County,Washington between 2014 and 2015.This dataset can be accessed [here ](https://www.kaggle.com/harlfoxem/housesalesprediction)  .
There are 2163 samples and 19 feature variables in this dataset. The objective was to predict the  prices houses using the given features.

The prices of the house indicated by the variable 'price' was the target variable and the remaining were the feature variabes that I used to predict the target variable.

## Data Used

| Variable |   Type |      Description                                          |      Used in the Model  |
|----------|--------|-----------------------------------------------------------|-------------------------|
| Price    | Numeric|     Prices of the houses  (Target Variable)               |                Y        |
| Bedrooms |  float |      No. of bedrooms                                      |                Y        |
| Bathrooms|  float |     No. of bathrooms                                      |                Y        |
| Floors   |        |      No. of floors                                        |                Y        |
|sqft_livin|        |   square footage of the home                              |                 Y       |
|sqft_lot  |        |    square footage of the lot                              |                 Y       |                
|floors    |        |      Total floors (levels) in house                       |                 Y       |
|waterfront|        |    House which has a view to a waterfront                 |                 Y       |
|view      |        |       Has been viewed                                     |                 N       |               
|condition |        |  How good the condition is ( Overall )                    |                 Y       |
|grade     |        |  overall grade given to the housing unit                  |                   Y     |
|sqft_above|        |  square footage of house apart from basement              |                   N     |
|sqft_bmnt |        | square footage of the basement                            |                   Y     |
|yr_built  |        |  Built Year                                               |                    Y    |
|yr_renov  |        | Year when house was renovated                             |                  Y      |
|zipcode   |        |     zip                                                   |                   Y     |
|lat       |        |      Latitude coordinate                                  |                  N      |
| long     |        |      Longitude coordinate                                 |                   N     |               
|sqft_l15  |        | Living room area in 2015(implies-- some renovations)      |                   Y    |
| sqft_lt15|        |lotSize area in 2015(implies-- some renovations)           |                   Y     |

## Data Preprocessing

The distribution of the target variable was skewed to the right with a very long tail.So I log tranformed it to get a near normal distribution.

I analyzed the degree of correlation of numeric features with target variable in order to have a quick view of potential feature importance and redundancies (similar variables with high degree of correlation).I combined redundant features that were also correlated, such as, **property_age=year_sold-year_built**.

I analyzed the categorical features against sales price to understand the impact of different classes and the count within each class. In some cases one class within the feature was predominant over others.So I created dummy variables from categorical features. 

## Model Testing

For my final input,I used 42 variables.I used a 80-20 train-test split cross-validation to train my model.I first built a multivariate regression model model which combines all the features into a single model.As my model was very simple ith a large error, I applied polynomial multivariate regression, with powers up to three to add complexity. The polynomial features are the base features squared and cubed and also the base features all multiplied in pairs and in triples.The R2 value imporved slightly after adding polynomial regression with degree 3.

One of the dangers of polynomial regression is that it can lead to overfitting. I used cross-validation to highlight overfitting, but it could not prevent overfitting.So to help reduce overfitting by applying a “punishment” to terms with large coefficients, I used Lasso regression on the dataset. This is a form of regularisation and can lead to more accurate results.

## Conclusion

In my test dataset, 70% of the predictions for home prices can be explained by my model.The model predicts the home prices in King Couty with an error of +-1.3% of the actual prices.As I focussed only on the physical features of the house,I can conclude that house prices are not only based on the physical properties of a house but also on several other factors.

## Future Work

For future work,I would like to include macro and micro features that could have an effect on the house prices.

**Macro Features**

Inspection reports

Comparable properties sold in the same area.

Mortgage rates

**Micro Features**

Economic indicators

Crime Reports

Reports on environmental quality

Reports on school ratings





 
 
