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
