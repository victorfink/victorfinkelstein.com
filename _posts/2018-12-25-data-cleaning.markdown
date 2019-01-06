---
layout: post
title:  "How to clean a data set ?"
date:   2018-12-25
categories: jekyll update
---


<div style="text-align: justify">

In this post, we focus on the data cleaning. It is very important that <b>the data is clean before beginning any computation</b> or visualization as it can produce absurd results or even produce errors.

</div>

## Data cleaning

<div style="text-align: justify">

Cleaning a data set can be quite easy if you know what you are looking for and what you are doing. Here I will explain the most useful and common tasks that have to be done in order to be sure that the data is clean.

</div>

### The data set has to make sense

<div style="text-align: justify">

You can check that the data set makes sense to you i.e look at the lines at the top and the bottom of the set and look at every value there. This is specific to each data set. For example, if you have a data set giving you the time of the day and the temperature at that time, just be sure that the values are physically correct (check the minimum and maximum of a column). In R, you can use the function `head()` or `tail()` to print the lines at the top or at the bottom of the dataset.

</div>

<p align="center">
	<img src="/images/head.png" width="350">
</p>

### Deal with missing / absurd values

<div style="text-align: justify">

Before any computations, the data set has to be clean i.e all the rows with NA values or absurd values have to be dealt with, otherwise, the next steps of your project will most probably give weird results or even produce an error.

</div>

#### Missing values

<div style="text-align: justify">

If the value is simply missing, you can choose to remove the line with it. It is not wise if your data set is small or if you would rather not lose any information. Another option is to replace the missing value by the mean or the median value of the column containing it.

</div>

<p align="center">
	<img src="/images/navalue.png" width="350">
</p>

#### Absurd values

<div style="text-align: justify">

If the value is absurd, for example if the column contains the temperature of a town (in Celsius), every day, and you see that a day, the temperature is over 100 degrees, you can have some doubts. In this case, it's the same as previously. You can choose to remove the line containing this absurd value, or just replace it with the mean or median value of the column.

</div>

<p align="center">
	<img src="/images/outlier.png" width="350">
</p>

## Conclusion

<div style="text-align: justify">

To conclude with, you have to be sure that your data set is clean before doing any computation. If you follow these quick steps, you will be able to clean your data sets very quickly. You just have to remember that every data set is unique. Hence a different cleaning for each data set.

</div>