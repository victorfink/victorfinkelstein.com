---
layout: post
title:  "The basics of regression"
date:   2019-01-02
categories: jekyll update
---


<div style="text-align: justify">

Regression is probably the easiest machine learning algorithm you can use in Data Science. Despite its simplicity, it's not a bad algorithm and it can be useful. I will show here the basic uses of this algorithm.

</div>

### What is it ?

<div style="text-align: justify">

A regression model is of the form : Y = f(X,b) + e, with f a function given by the user (linear or non linear with regard to b, depending on the type of regression), X is a vector with the variables, Y is the output, b is a vector with the parameters of the regression (this is what is computed during the training), and finally e is the error of the model (e is assumed to be a random variable of mean 0, and e can be assumed to be normal). The trick here is in chosing the good function f and the good variables in X.

</div>

### Implementation in R

<div style="text-align: justify">

Regression is quite easy to implement with the "lm" function in R. The "lm" function only requires a formula of type y ~ x where x are the variables and y the response vector. After you have called the regression function, you can view the summary of your regression with the function summary. Here is an example with a data set about sales in a single shop.

</div>

<p align="center">
	<img src="/images/summReg.png" width="400">
</p>

<div style="text-align: justify">

Here I only did the regression with one variable : the temperature of the day. When printing a summary, there are several important informations. 
<ul>
	<li> The first one are the coefficients : you can see an estimate of the value of the parameters and the standard error on those estimations. Next to this value is the p-value associated. The smaller this p-value is, the more the variable associated to this parameter is significant. A simple rule to know if the variable is good is to look at this p-value, if it is smaller than 0.1, it's good, but if it's bigger, you have to try another variable or just delete it. Note that this rule is not always good to use (it mostly depends on the data set and what you're trying to do). </li>
	<li> Then you can see the r-squared and the adjusted r-squared. It is a good way to know if your model explains the data set or not. The closer it is to 100%, the better. For complex data set, it is rare to get a adjusted r-squared close to 100%, so this value alone can not tell you the quality of your model </li> 
</ul>

You can also chose to validate your model with other methods. You can simply plot the result of your regression and see if it matchs your data set (if the problem is small in dimension). You can also plot the residuals and look at their distributions.

</div>

<p align="center">
	<img src="/images/resplot.png" width="350">
</p>

<div style="text-align: justify">

Here the residuals are not normal. The model can not be validated. Another method to check this it to use the function "qqnorm" and "qqline" with the residuals, this will show the quantile of the residuals and you will be able to compare them with the quantiles of a normal law.

</div>

<p align="center">
	<img src="/images/qqplot.png" width="350">
</p>

<div style="text-align: justify">

The points has to be close to the line, which is clearly not the case here. Hence, once again, the model is not valid.

</div>

#### (Multi)linear regression

<div style="text-align: justify">

When doing a linear regression, the function f has to be linear with regard to the parameters b, but not necessarily with regard to the variables. It means that you can do a linear regression with the squared, or exponential of a variable for example. A multilinear regression is when you have more than two parameters in the regression (including the intercept).

</div>

#### Interactions between variables

<div style="text-align: justify">

Sometimes, linear combination of the variables are not enough. You can have some interactions between variables. For example, again about the sales in a single shop, if this shop sells ice cream, it is reasonnable to say that the temperature and the type of the day (week day or week end) will have an impact on the sales of ice cream. Furthermore, if it is especially hot during a day of the week end, the shop can expect to sale bigger amount of ice cream. Hence, it can be wise in this case to introduce an interaction between the type of the day and the temperature. Remember that each data set requires a different approach so what we are doing here may not be wise in another case.

</div>


## Conclusion

<div style="text-align: justify">

With this post, you can now compute regression models and verify their validity thanks to differents tools. Despite being one of the simplest method, (multi)linear regression can be quite performant for simple data sets. It's not always a good idea to rush on random forests or neural networks !

</div>

