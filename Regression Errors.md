
Regression Basic Errors: MAE, MSE, RMSE, MSE 

[![image](https://github.com/user-attachments/assets/0ab81b75-5419-47a2-a6f5-86f899a63d7d)](https://www.youtube.com/watch?v=KzHJXdFJSIQ)

RMSLE

https://www.youtube.com/watch?v=z_DDJq1R6GI&t=1350s

Take aways from the video:


RMSE Vs RMSLE Article

https://medium.com/analytics-vidhya/root-mean-square-log-error-rmse-vs-rmlse-935c6cc1802a

Before taking a nosedive in the intricacies of the RMSLE, let’s take a quick look at the formulation.


Take aways from the article:

**Robustness to the effect of outliers**:

In the case of RMSE (Root Mean Squared Error), the presence of outliers can explode the error term to a very high value. 
But, in the case of RMSLE the outliers are drastically scaled down therefore nullifying their effect.

Consider the predicted value to be X and the actual value to be Y
Y = 60 80 90
X = 67 78 91   On calculating, their RMSE and RMSLE comes out to be: 4.242 and 0.6466 respectively

Now let us introduce an outlier in the data
Y = 60 80 90 750
X = 67 78 91 102
Now, in this case, the RMSE and RMSLE comes out to be: 374.724 and 1.160 respectively

RMSLE (Root Mean Squared Log Error) metric only considers the relative error between the Predicted and the actual value, the scale of the error is not significant. 
On the other hand, RMSE value increases in magnitude if the scale of error increases.

**Relative Error**:
Let’s understand this with the help of an example.

Case 1:
Y = 100
X = 90
Calculated RMLSE: 0.1053
Calculated RMSE: 10

At first glance, nothing looks flashy. Let’s consider another example.

Case 2:
Consider
Y = 10000
X = 9000
Calculated RMSLE: 0.1053
Calculated RMSE : 1000
