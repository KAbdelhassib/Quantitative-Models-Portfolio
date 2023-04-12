# Quantitative-Models-Portfolio
A portfolio Of models I've develeoped during different roles

# Factor Model Portfolio Optimizer

## Overview

The factor model portfolio optimizer is a Python class designed to optimize a stock portfolio based on factor models. Factor models are widely used in finance to model stock returns and risk, as they capture the influence of various factors on asset prices. This optimizer uses multiple regression and risk calculations to estimate the optimal weights of assets in the portfolio.
Factors

The factors used in this model are defined by the user and can be any set of variables that the user believes to have an impact on stock returns. Common factors include macroeconomic variables such as GDP growth, inflation, and interest rates, as well as company-specific factors such as earnings and book-to-market ratios.

# Class: PortfolioOptimizer Attributes
•	dependent_data: DataFrame containing dependent variables (stock returns).
•	independent_data: DataFrame containing independent variables (factors).
•	window_size: The size of the rolling window used for regression.
•	dependent_vars: List of dependent variable names.
•	independent_vars: List of independent variable names.
•	decay_rate: Decay rate for the exponential decay weights.
•	prediction_step: Number of steps ahead for out-of-sample predictions.

# Methods

•	__init__: Constructor for the PortfolioOptimizer class.
•	rolling_multiple_regression_with_prediction_multi_assets: Performs rolling multiple regression with predictions for multiple dependent

# variables

•	rolling_multiple_regression_with_prediction: Performs rolling multiple regression with predictions for a single dependent variable.
•	portfolio_risk_calculation: Calculates the common and specific risk of the portfolio.
•	portfolio2_objective: Objective function for the portfolio optimization problem.
•	common_Risk: Calculates the common risk of the portfolio.
•	Specific_risk: Calculates the specific risk of the portfolio.
•	Tota_risk: Calculates the total risk of the portfolio.
•	check_sum: Constraint function ensuring the sum of weights equals 1.
•	Stock_drop: Constraint function for stock weight bounds.
•	Factor_bound: Constraint function for factor bounds.
•	portfolio_objective_with_alphas: Objective function for the portfolio optimization problem with alphas.

# Workflow

1.	Instantiate the PortfolioOptimizer class with the necessary input parameters.
2.	Perform rolling multiple regression with predictions for multiple dependent variables using the rolling_multiple_regression_with_prediction_multi_assets method.
3.	Calculate the portfolio risk using the portfolio_risk_calculation method.
4.	Optimize the portfolio using the objective function portfolio2_objective and the constraint functions.
Interpretation of Results
The optimization process yields the optimal weights for each asset in the portfolio, which minimize the portfolio risk and maximize the returns based on the factors provided. The results also include common and specific risk measures, which can help investors understand the sources of risk in their portfolio.
Code Comments
Throughout the code, comments have been added to provide explanations for various parts of the code, which helps readers understand the logic and calculations involved in the implementation of the factor model optimizer.

