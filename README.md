# ravikumarroy_bitsom_ba_2511993_part3_regression_insights


# Business Problem Summary

The leadership team of a retail chain wants to understand which factors are most strongly associated with monthly sales performance across stores. The objective is to use regression analysis to identify the key drivers of sales and support decisions related to marketing investment, inventory management, staffing, discount strategy, and store operations.

The findings will help leadership prioritize actions that may improve store performance and allocate resources more effectively.

## Dataset Description

The dataset contains monthly performance information for retail stores across different regions and store types.

Total Records: 320

Key variables included:

* Store ID
* Month
* Region
* Store Type
* Marketing Spend
* Footfall
* Average Discount Percentage
* Staff Count
* Inventory Availability Percentage
* Competitor Distance
* Holiday Flag
* Customer Rating
* Monthly Sales
* Monthly Profit

## 1.Dependent Variable

The dependent variable selected for regression analysis is:

**monthly_sales**

This variable represents the business outcome that leadership wants to understand and improve.

## 2.Potential Independent Variables

The following variables may influence monthly sales and will be evaluated as predictors:

* marketing_spend
* footfall
* avg_discount_pct
* staff_count
* inventory_availability_pct
* competitor_distance_km
* holiday_flag
* customer_rating
* region (categorical)
* store_type (categorical)

## 3.Numerical Variables

* marketing_spend
* footfall
* avg_discount_pct
* staff_count
* inventory_availability_pct
* competitor_distance_km
* customer_rating
* monthly_sales
* monthly_profit

## 4.Categorical Variables

* region
* store_type

## 5.Variables that may need cleaning or transformation

The following categorical variables require dummy variable creation before they can be used in regression models:

* region
* store_type

Dummy variables will be created to represent these categories while avoiding the dummy variable trap by using a reference category.

## Variables that may not be useful for regression

### store_id

Store ID is a unique identifier and does not represent a business factor that directly influences sales. Therefore, it will not be used as an independent variable in the regression models.

### month

The month field is primarily a date identifier. Unless specific seasonality analysis is performed, it will not be included in the main regression models.

### monthly_profit

Monthly Profit is closely related to Monthly Sales and is considered a business outcome rather than a predictor. Therefore, it will not be used as an independent variable when predicting monthly sales.

## Initial Data Preparation Approach

Before running regression models, the dataset will be reviewed for:

* Missing values
* Duplicate records
* Data consistency
* Categorical variable encoding
* Outliers in key numerical variables

A cleaned dataset and dummy-variable dataset will be created for regression analysis while preserving the original data.



# Regression Approach

Three regression models were developed to evaluate factors associated with monthly sales.

## Simple Regression Model 1

Dependent Variable:

* Monthly Sales

Independent Variable:

* Marketing Spend

Results:

* R² = 0.1672

Marketing Spend showed a positive and statistically significant relationship with Monthly Sales.

## Simple Regression Model 2

Dependent Variable:

* Monthly Sales

Independent Variable:

* Footfall

Results:

* R² = 0.7363

Footfall showed a strong positive and statistically significant relationship with Monthly Sales.

## Multiple Regression Model

Dependent Variable:

* Monthly Sales

Independent Variables:

* Marketing Spend
* Footfall
* Average Discount Percentage
* Inventory Availability Percentage
* Region_North

Results:

* R² = 0.8067
* Adjusted R² = 0.8037

The multiple regression model provided the strongest explanatory power and was selected as the final model.

# Dummy Variable Approach

Categorical variables were converted into dummy variables before regression analysis.

## Region

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

## Store Type

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

Reference categories were excluded to avoid multicollinearity and the dummy variable trap.

# Model Comparison Summary

| Model               | Independent Variables                                                             | R²     |
| ------------------- | --------------------------------------------------------------------------------- | ------ |
| Simple Regression 1 | Marketing Spend                                                                   | 0.1672 |
| Simple Regression 2 | Footfall                                                                          | 0.7363 |
| Multiple Regression | Marketing Spend, Footfall, Avg Discount %, Inventory Availability %, Region_North | 0.8067 |

The Multiple Regression Model achieved the highest explanatory power and was selected as the final model.

# Final Model Selected

The Multiple Regression Model was selected because:

* Highest R² value
* Includes multiple business drivers
* Explains approximately 80.7% of variation in monthly sales
* Provides stronger decision support than simple regression models

# Business Recommendation

The analysis suggests that leadership should focus on:

1. Increasing customer footfall.
2. Investing in effective marketing activities.
3. Maintaining high inventory availability.
4. Identifying operational best practices from high-performing stores.

Footfall, Marketing Spend, and Inventory Availability showed the strongest positive association with Monthly Sales.

Average Discount Percentage and Region_North were not statistically significant and should not be heavily relied upon for decision-making.

# Assumptions and Limitations

Several limitations should be considered:

* Regression identifies association rather than causation.
* Some business factors affecting sales may not be included in the dataset.
* Local market conditions and operational differences may influence performance.
* Residual analysis identified stores that performed significantly above or below model expectations.

The model should be used as a decision-support tool rather than a perfect forecasting system.

# Screenshots Included

The repository includes the following screenshots:

* simple_regression_output.png
* multiple_regression_output.png
* residuals_preview.png
* model_comparison_preview.png

These screenshots provide evidence of the regression analysis, model comparison, and residual calculations performed during the project.
