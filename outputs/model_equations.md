# Model Equations

## Dummy Variable Approach

Two categorical variables were converted into dummy variables for regression analysis.

### Region

Original categories:

* East
* North
* South
* West

Dummy variables created:

* Region_East
* Region_North
* Region_South

Reference category:

* West

West was excluded from the regression model and serves as the baseline category for interpreting regional effects.

### Store Type

Original categories:

* Airport
* High Street
* Mall
* Residential

Dummy variables created:

* Store_Airport
* Store_HighStreet
* Store_Mall

Reference category:

* Residential

Residential was excluded from the regression model and serves as the baseline category for interpreting store type effects.

The reference categories were omitted to avoid the dummy variable trap and prevent perfect multicollinearity.

---

# Simple Regression Model 1

## Equation

Monthly Sales = 560777.35 + (2.13 × Marketing Spend)

## Results

* R² = 0.1672
* Marketing Spend Coefficient = 2.13
* P-value = 2.48E-14

## Interpretation

Marketing Spend has a positive and statistically significant relationship with Monthly Sales. Every additional unit of marketing spend is associated with approximately 2.13 additional units of monthly sales.

---

# Simple Regression Model 2

## Equation

Monthly Sales = 446410.58 + (35.68 × Footfall)

## Results

* R² = 0.7363
* Footfall Coefficient = 35.68
* P-value = 4.75E-94

## Interpretation

Footfall has a strong positive and statistically significant relationship with Monthly Sales. Each additional customer visit is associated with approximately 35.68 additional units of monthly sales.

This model explains approximately 73.6% of the variation in monthly sales.

---

# Multiple Regression Model

## Equation

Monthly Sales =
151399.35

* (1.163 × Marketing Spend)
* (33.641 × Footfall)
  − (70986.27 × Average Discount Percentage)
* (2851.73 × Inventory Availability Percentage)
  − (217.04 × Region_North)

## Coefficient Interpretation

### Marketing Spend

Coefficient = 1.163

Holding other variables constant, increasing marketing spend is associated with higher monthly sales.

### Footfall

Coefficient = 33.641

Footfall is the strongest predictor in the model. Higher customer traffic is strongly associated with increased monthly sales.

### Average Discount Percentage

Coefficient = -70986.27

The relationship is negative, but the variable is not statistically significant at the 5% level and should not be heavily relied upon for business decisions.

### Inventory Availability Percentage

Coefficient = 2851.73

Stores with higher inventory availability tend to generate higher monthly sales.

### Region_North

Coefficient = -217.04

The North region does not differ significantly from the reference region (West) after controlling for other factors.

---

# Final Model Selected

The Multiple Regression Model was selected as the final model.

## Reason for Selection

* Highest R² value (0.8067)
* Explains approximately 80.7% of variation in monthly sales
* Includes multiple business drivers
* Provides stronger decision support than the simple regression models
* Identifies which variables remain important after controlling for other factors

The model offers the best balance of explanatory power and business usefulness.
