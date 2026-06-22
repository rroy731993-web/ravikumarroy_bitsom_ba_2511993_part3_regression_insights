# Dummy Variable Approach

Two categorical variables were converted into dummy variables for regression analysis:

## Region

Original categories:

- East
- North
- South
- West

Dummy variables created:

- Region_East
- Region_North
- Region_South

Reference category:

- West

West was excluded from the regression model and serves as the baseline category for interpreting the coefficients of the region dummy variables.

## Store Type

Original categories:

- Airport
- High Street
- Mall
- Residential

Dummy variables created:

- Store_Airport
- Store_HighStreet
- Store_Mall

Reference category:

- Residential

Residential was excluded from the regression model and serves as the baseline category for interpreting the coefficients of the store type dummy variables.

The reference categories were omitted to avoid the dummy variable trap and prevent perfect multicollinearity in the regression models.




## Simple Regression Model 1



### Model

Monthly Sales = 560777.35 + 2.13 × Marketing Spend

### Results

* R² = 0.1672
* Marketing Spend Coefficient = 2.13
* P-value = 2.48E-14

### Business Interpretation

Marketing Spend has a positive and statistically significant relationship with Monthly Sales. On average, every additional unit of marketing spend is associated with an increase of approximately 2.13 units in monthly sales.

Although significant, this model explains only 16.7% of sales variation, indicating that additional business factors should be included in a more comprehensive model.
