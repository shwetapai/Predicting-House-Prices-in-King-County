# Predicting-House-Prices-in-King-County

I took the housing dataset which contains information about different houses in King County,Washington between 2014 and 2015.This dataset an also accessed from   .
There are 2163 samples and 19 feature variables in this dataset. The objective was to predict the  prices houses using the given features.

The prices of the house indicated by the variable 'price' was the target variable and the remaining were the feature variabes that I used to predict the target variable.

##Data Used

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
|sqft_l15  |        | Living room area in 2015(implies-- some renovations)      |                   N     |
| sqft_lt15|        |lotSize area in 2015(implies-- some renovations)           |                   N      |
 
 
 
