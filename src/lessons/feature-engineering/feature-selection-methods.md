# Feature Selection 

<hr>

When you cook a dish, you select specific ingredients that make the dish delicious and give it the right flavor. In data science, feature selection is like picking the most important ingredients for a recipe. Often times, we have datasets with many different pieces of features. 

In another scenerio, imagine you have a big puzzle with many puzzle pieces representing different pieces of information about something you're interested in. However, some puzzle pieces might not be important for completing the picture, while others are crucial.

<img src="./feature-engineering/puzzle-game.gif" style="display: block;
  margin-left: auto;
  margin-right: auto;
  width: 50%;">

<aside>

**_Definition..._**

**_Feature selection_** is the process of choosing only the most relevant and essential features from the dataset to solve a specific problem or make accurate predictions. This is important because machine learning models can only learn from the features that are provided to them, and including irrelevant features can actually hurt the performance of the model.
</aside>

For example, if we want to predict whether a student will pass an exam, we might look at features like their study hours, previous test scores, and attendance. Some other features, like the color of their clothes or favorite food, might not be useful for predicting their exam performance, so we can leave them out. Feature selection helps us streamline our analysis and decision-making, allowing us to focus on what truly matters and find valuable insights in the data.


## Feature selection methods
Feature selection is an important part of the data preprocessing pipeline, and it can help to improve the performance of machine learning models. However, it is important to choose the right method for feature selection, as it can be more time-consuming and difficult to identify the most relevant features. There are basically 3 feature selection methods - `Filter`, `Wrapper`, and `Embedded`, however, we'll focus only on the `Filter` and `Wrapper` methods in this lesson.

![feature_selection.png](./feature-engineering/feature_selection.png)

###  Filter methods
Filter methods in feature selection are like using a magnifying glass to focus on the most important pieces of information in a large dataset. Just like you use a magnifying glass to zoom in on specific details of a picture, filter methods help us identify the most relevant features that have a strong relationship with the target we want to predict or understand.

<img src="./feature-engineering/magnify-data.gif" height="270px" width="50%" style="display: block;
margin-left: auto;
margin-right: auto;">

For example, if we want to predict whether it will rain tomorrow, we might look at how closely the temperature, humidity, and wind speed are related to rain. If we find that temperature and humidity have a strong relationship with rain, we might keep them as important features, while other less relevant features may be discarded.

These methods are relatively simple to implement and can be used with any machine learning model. There are two main types of filter methods:
- **Univariate**: select features based on their individual statistical properties, such as their correlation with the target variable or their variance.
- **Multivariate**: These methods select features based on their relationship with other features, such as their mutual information or their redundancy.

Using the rain example above, let's use a code snippet in Python to demonstrate a simple filter method for feature selection using the correlation coefficient.

<iframe src="https://trinket.io/embed/python3/08da51b3b1?toggleCode=true&runOption=run" width="100%" height="356" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

In this output, we can see that the filter method selected the top 5 features - `Temperature`, `UV_Index`, `Wind_Speed`, `Humidity`, and `Cloud_cover` based on their correlation with the target variable `Rain`. This means the selected features have the strongest relationship with _rain_ and are considered the most relevant for predicting whether it will rain or not.

### Wrapper methods
Imagine you are a detective trying to solve a mystery 🤔 by finding the right combination of _clues_ that will lead you to the culprit. Each _clue_ is like a feature in data science, providing a piece of information that may or may not be relevant to solving the case.

The _wrapper_ method is like testing different combinations of clues to see which combination helps you solve the mystery most effectively. You try out different sets of clues and evaluate how well each set helps you catch the culprit. The set of clues that leads you to the culprit is the one you choose to solve the mystery.

<img src="./feature-engineering/detective.gif" height="270px" width="70%" style="display: block;
margin-left: auto;
margin-right: auto;">

These methods are more complex to implement than filter methods, but they can be more effective at selecting features that are important for the specific machine learning task. There are two main types of wrapper methods:

- **Sequential forward selection**: Begins with an empty set of features and then adds features one at a time, evaluating the model performance after each addition.
- **Sequential backward selection**: Starts with the full set of features and then removes features one at a time, evaluating the model performance after each removal.

To implement the wrapper method, we'll need to run a sample machine learning model and evaluate the feature importance. Since we are yet to cover machine learning, this code snippet is ONLY to show you how the wrapper method works, hence, you don't need to understand the code snippet.

<iframe src="https://trinket.io/embed/python3/e69c9da00d?toggleCode=true&runOption=run" width="100%" height="356" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

As a guide, the code first splits the dataset into features `(X)` and the target variable `(y)`. Then, it creates a Random Forest classifier model and fits it to the training data. The Random Forest model is used as a machine learning model to evaluate the importance of each feature.

The table below gives a summary of the two feature selection methods explored in this lesson, and also include the embedded method.

| Methods                 | Description |
|-------------------------|-------------|
| Filter                  | Evaluates the relevance of each feature independently of the model's performance. Uses statistical techniques to rank features based on their correlation with the target variable or other statistical measures. |
| Wrapper                 | Uses a specific machine learning model to evaluate the importance of features. Creates subsets of features and evaluates their performance using the chosen model. The best subset of features is selected based on the model's performance. |
| Embedded                | Incorporates feature selection as part of the model building process. Performs feature selection while training the model, using techniques like regularization to penalize less important features. |


<aside>

**_Lesson summary..._**

_Feature selection_ helps data scientists remove unnecessary noise from the data and extract the most valuable insights, just like picking the right ingredients for a delicious dish! By choosing the right features, we can make data analysis more efficient, gain meaningful information, and make better decisions for various business and real-life challenges.
</aside>

<!-- 
### 👩🏾‍🎨 Practice: Feature selection... 🎯

<br> -->

> ➡️ In the next section, we'll be looking at `Feature extraction techniques` 🎯.


