# Feature Encoding
In the last lesson, we have seen how to transform or scale _numerical_ features. In this lesson, we'll be focusing on techniques we need to know in order to perform feature engineering on _categorical features_. This is required because machine learning models can only understand numerical data. Hence, feature encoding is like translating different languages into a common language that a computer can understand.

## What is feature encoding?

<aside>

**_Defnintion..._**

**_Features encoding_** refers to the process of converting categorical or non-numeric features into a numerical representation that machine learning algorithms can understand.
</aside>

Since most machine learning algorithms work with numerical data, feature encoding is necessary to represent categorical information in a way that can be used for analysis or modeling.

For example, let's consider the `Gender` column with values `Male` and `Female` in a dataset. We can encode this column into numerical values, like `0` for _Male_ and `1` for _Female_. This way, the computer can understand and work with the data, allowing us to use it for various tasks, such as making predictions or finding patterns.

## Encoding techniques
There are a number of different techniques for encoding categorical features, but some of the most common include...
- Label encoding
- One-hot encoding
<!-- - Target encoding -->

### 1. Label encoding
Label encoding is a technique in data science that converts categorical or non-numeric features into numbers. This is done by assigning each category a unique integer value. This is like giving numbers to different things so that we can easily refer to them using numbers instead of long names.

For example, using a sample dataFrame,  suppose we have a dataset of fruits, and the categorical features include `Fruit_Type`, `Color`, and `Taste`. We can use label encoding to convert these features into numbers. Here's a sample code snippet:

<iframe src="https://trinket.io/embed/python3/6ff39b2cd8?toggleCode=true&runOption=run" width="100%" height="356" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

In the code snippet, _Apple_ is represented as `0`, _Banana_ as `1`, and _Orange_ as `2`. Now, we can use these encoded numbers for further analysis or modeling tasks. Here's the output of the code snippet.


### 2. One-hot encoding
One-hot encoding is another technique used to handle categorical or non-numeric features. This is done by creating a new binary feature for each category. Each column represents a specific category, and it contains a value of `1` if the data point belongs to that category, and `0` if it does not. 

<br>

<div style="position: relative; padding-bottom: 56.25%; height: 0;"><iframe src="https://www.youtube.com/embed/G2iVj7WKDFk" title="Web Scrapping Intro" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 2px solid grey;"></iframe></div>

<br>

Now, let's use the same example of the fruit dataset and perform one-hot encoding on the `Fruit_Type` column. 

<iframe src="https://trinket.io/embed/python3/7e92f24336?toggleCode=true&runOption=run" width="100%" height="356" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

The output of the sample code is a DataFrame with three additional columns: `Fruit_Apple`, `Fruit_Banana`, and `Fruit_Orange`. Each column represents a fruit type, and a value of `1` indicates that the row corresponds to that particular fruit, while a value of `0` indicates that it doesn't.

With one-hot encoding, we have converted the `Fruit_Type` categorical feature into binary columns, making it easier for machine learning algorithms to process and analyze the data. 

<!-- ### 3. Target encoding
<div style="position: relative; padding-bottom: 56.25%; height: 0;"><iframe src="https://www.youtube.com/embed/N9fDIAfylCMY" title="Web Scrapping Intro" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 2px solid grey;"></iframe></div>

<aside>

**NOTE!**

While target encoding is a more sophisticated technique than label encoding. It can be more effective at improving the performance of machine learning models, but it can also be more difficult to implement on large dataset.
</aside> -->

## Encoding techniques selection
Each encoding technique has its strengths and is suitable for different scenarios. Label Encoding is useful when there is an inherent order among the categories, while One-Hot Encoding is effective for scenarios where categories are not ordered and have no numerical relationship. The choice of encoding technique depends on the nature of the data and the requirements of the analysis or modeling task.

<aside>

**_Lesson Summary..._**

**_Feature encoding_** is a useful technique for transforming categorical features into numerical features. It can help to improve the performance of machine learning models, but it is important to use it carefully. By using feature encoding, we make our data more accessible to computers, enabling us to perform data analysis and build powerful machine learning models that can understand and learn from the data more effectively.

**_<span style="color: red;"> NOTE! </span>_**

It is important to use feature encoding carefully to avoid...
- increasing the size of the dataset.
- making the data less interpretable due to numerical representations.
</aside>


### 👩🏾‍🎨 Practice: Feature encoding... 🎯

<br>

> ➡️ In the next section, we'll be looking at `Feature selection methods`🎯