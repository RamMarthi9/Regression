Regression:

![image](https://github.com/user-attachments/assets/a714f52f-5a35-40ed-b468-c2fd99de5913)

Q1. What is Regression? How is it used in data analysis?

    Regression is a statistical method used to model and analyze the relationship between a dependent variable (target) 
    and one or more independent variables (predictors). It is one of the most fundamental and widely applied techniques in data analysis and machine learning.

    The primary goal of regression is to predict outcomes or quantify the strength and nature of relationships between variables. 
    Regression allows us to make data-driven decisions by identifying patterns and trends in datasets.

    In summary, regression is a cornerstone of data analysis, enabling predictions and insights critical for informed decision-making. 
    By choosing the appropriate type of regression and ensuring assumptions are met, analysts can extract meaningful information from complex datasets.

Q2. Explain the equation of a simple linear regression model. What do the terms represent?
    The general form of the simple linear regression equation is: y = mx + c + e

    y is value to be predicted -- Dependent Variable/ Predictor Variable
    x is value which helps in predicting y -- Independent Variable
    m is change in y for one unit increase in x 
      -- slope or coefficient
      -- represents the strength and direction of the relationship between x and y
    c is value of y when x = 0 
      -- It represents the baseline value of the dependent variable when there is no influence from the independent variable.

Q3. What assumptions does Linear Regression make? Can you name at least four?
  1. Linearity
  2. No Multicollinearity
  3. Independence of errors
  4. Homoscedasticity (Constant Variance of Errors)
  5. Normality of Residuals

    1. Linearity
        Assumption: The relationship between the independent variables (𝑥) and the dependent variable (𝑦) is linear.

        Why it Matters: Linear regression can only accurately model linear relationships. If the relationship is nonlinear, predictions will be biased.

        How to Check: Plot the dependent variable against each independent variable to visualize linearity.
        Residual plots: Residuals should not show patterns when plotted against predictors.

    2. Independence of Errors
        Assumption: The residuals (errors) are independent of each other.

        Why it Matters: Correlated errors can lead to underestimation of standard errors, invalidating significance tests.

        How to Check: Use the Durbin-Watson test for autocorrelation (especially in time-series data).
        Ensure no logical dependency exists between observations (e.g., time-dependent patterns).

    3. Homoscedasticity (Constant Variance of Errors)
   
        Assumption: The variance of residuals is constant across all levels of the independent variables.

        Why it Matters: Heteroscedasticity (non-constant variance) can make the model inefficient and bias the standard errors, leading to incorrect confidence intervals and p-values.
        How to Check: Plot residuals against predicted values; there should be no cone-shaped pattern. Perform statistical tests like Breusch-Pagan or White’s test.

    4. Normality of Residuals
        Assumption: The residuals (errors) follow a normal distribution.
        Why it Matters: This assumption is crucial for valid hypothesis testing and constructing confidence intervals.
        How to Check: Create a Q-Q plot (quantile-quantile plot) of residuals. Points should fall along the diagonal. Use the Shapiro-Wilk test or Kolmogorov-Smirnov test for normality.

    5. No Multicollinearity: Independent variables should not be highly correlated with each other.
    6. No Measurement Error: Independent variables are measured without error.

      Why These Assumptions Matter
      Violations of these assumptions can lead to:
        Biased or inefficient estimates.
        Invalid p-values and confidence intervals.
        Misleading interpretations of the model.
        If assumptions are violated, alternative methods (e.g., transformations, robust regression, or regularization techniques like Ridge/Lasso) may be required.

Q4. What is the difference between simple and multiple linear regression?
     
     1. Simple linear regression and multiple linear regression are both types of linear regression, but they differ in the number of independent variables used to predict the dependent variable.

     Here's a detailed comparison:
     Involves one independent variable (𝑥) to predict the dependent variable (𝑦).

     Multiple Linear Regression:
     Involves two or more independent variables (𝑥1,𝑥2,…,𝑥𝑛) to predict the dependent variable (𝑦).

    2. Complexity
    Simple Linear Regression:

    Easier to compute and interpret as it involves only one predictor.
    Visualized as a straight line in a 2D space (scatter plot).
    
    Multiple Linear Regression:

    More complex because it considers multiple predictors.
    Visualized as a hyperplane in an n-dimensional space (not easily visualizable for more than 3 predictors).
    
Intermediate Questions:

How do we evaluate the performance of a linear regression model? What metrics can we use?

https://github.com/RamMarthi9/Regression/blob/main/Regression%20Errors.md


What is multicollinearity? How does it affect a linear regression model?
Multicollinearity refers to the situation where two or more independent variables in a multiple linear regression model are highly correlated with each other. This means that one independent variable can be predicted or explained by a combination of the other independent variables.

How it affects a linear regression model:

1. Unstable Coefficients: When multicollinearity is present, the regression coefficients (the values that multiply the independent variables) become highly sensitive to small changes in the data. This makes the model's coefficients unstable, meaning they might fluctuate significantly with small variations in the data.


2. Inflated Standard Errors: High correlation among the predictors increases the standard errors of the estimated coefficients. This leads to less reliable estimates and makes it harder to determine whether a predictor is significantly contributing to the model.


3. Difficulty in Interpretation: If two or more predictors are highly correlated, it becomes difficult to determine the individual effect of each predictor on the dependent variable because their effects are intertwined.


4. Reduced Predictive Power: While the model might still fit the data well (low residuals), multicollinearity can reduce the model's ability to generalize to new data. This can lead to overfitting, where the model performs well on the training data but poorly on unseen data.



Common Symptoms of Multicollinearity:

High variance inflation factor (VIF) values for the independent variables.

A high correlation matrix showing values close to 1 or -1 between pairs of predictors.


Solutions to Multicollinearity:

Remove highly correlated predictors.

Combine predictors through techniques like Principal Component Analysis (PCA).

Regularization techniques like Ridge or Lasso regression can help by adding a penalty to the model, thereby reducing the impact of multicollinearity.


What is the significance of the p-value in a regression model?

How do you handle categorical variables in linear regression?

What does the R-squared value represent? How does it differ from adjusted R-squared?

What is the role of feature scaling in linear regression? Is it necessary?

Advanced Questions
Explain the concept of regularization in linear regression. How do Lasso and Ridge regression differ?

What is the effect of outliers on a linear regression model? How can we address them?

What is the difference between underfitting and overfitting in linear regression? How can you prevent them?

How do you interpret the coefficients in a linear regression model?

If a linear regression model has high multicollinearity, what methods can you use to address it?

Scenario-Based Questions
Imagine you’ve built a linear regression model, and the residuals show a clear pattern. What does this indicate? How would you address it?

Your model’s R-squared value is very high, but it performs poorly on the test set. What might be the cause?

You’re using a linear regression model to predict housing prices, but the predictions are consistently lower than the actual prices. What could be the issue?

You have a dataset with 100 features, but only a subset of them are relevant. How would you select the best features for your linear regression model?

You’ve applied a linear regression model, but the coefficients for some features are unexpectedly negative. How would you investigate this?
