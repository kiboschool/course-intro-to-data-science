# Regression in ML
Imagine you are trying to predict the price of a house based on various features like the number of bedrooms, the area in square feet, and the age of the house. This problem **cannot** be solved with classification because the outcome you want to predict, i.e, the `house price`, is a continuous variable, meaning it can take ANY numerical value within a range. 

In contrast, classification is only used when the outcome is a categorical variable with distinct categories, like predicting whether an email is spam or not.

## Regression

<aside>

**_Definition..._**

_Regression_ consists of models that predict a continuous outcome _(y)_ (dependent feature) based on the value of one or more predictor variables _(x)_ (independent features). The model is trained on a set of labeled data, which means that the data has been pre-classified into different categories. 
</aside>

However, unlike classification, the categories in regression are _continuous values_, such as height, weight, or price. Imagine you want to estimate how much time it will take for you to reach a friend's house based on the distance you have to travel and the average speed at which you walk.

<img src="./ml/car_road.gif" style="display: block;
  margin-left: auto;
  margin-right: auto;
  height: 300px">

In machine learning, regression works in a similar way. You show the computer many examples of distances traveled and the corresponding time taken to reach a destination. The computer then looks for patterns and relationships between the distances and the time.



