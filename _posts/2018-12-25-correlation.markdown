---
layout: post
title:  "Finding correlation between variables in a data set"
date:   2018-12-25
categories: jekyll update
---


<div style="text-align: justify">

Data analysis is the next step after data cleaning. It is also very important to analyze the data in order to understand the interactions between variables. The first step in this analysis is to find any correlations between variables (columns) of your data set.

</div>

## Finding correlations

<div style="text-align: justify">

Understanding the interactions between variables is very important when you are working with your data. Indeed, using useless variables can be a waste of (computing) time and using two variables that are strongly correlated (hence explaining the same thing) can lead to wrong results. With the “corrplot” package, you can quickly view the correlations between variables with a graphic. Dark colors indicate a strong correlation between variables. In this example, which is about cars, you can see a strong (positive) correlation between the horsepower (hp) of a car, and the number of cylinder in the engine of a car (cyl).

</div>

<p align="center">
	<img src="/images/correlation.png" width="750">
</p>

<div style="text-align: justify">

This positive correlation means that horsepower, in a car, changes in the same direction as the number of cylinder in the engine of a car. Usually, if you have more cylinders in the engine, it will have more horsepower.

</div>

#### Redundant variables

<div style="text-align: justify">

It is also important to distinguish strongly correlated variables, and redundant variables. Those can be easily mistaken. If two variables are strongly correlated, it can be because they are in fact explaining literally the same thing. For example, if you are studying the surface of a square depending on the length of the sides and the length of the diagonals, those two variables are explaining exactly the same thing since the length of the sides and the length of the diagonals are related in a square ! Every data set is different but you have to be sure that there are no redundant variables for the next parts of the analysis.

</div>
