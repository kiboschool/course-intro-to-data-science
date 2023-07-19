# Feature transformation
<aside>

**_Definition..._**

**_Feature transformation_** is the process of changing the way data is represented or organized to make it more suitable for analysis and modeling. It involves applying mathematical or statistical operations to the data to create new features or modify existing ones.
</aside>

Think of it as translating a story from one language to another depending on the audience. It deals with reshaping or molding the data to better highlight patterns and relationships, by applying mathematical or statistical operations to the data to create new features or modify existing ones. 

For example, imagine we have a dataset of temperatures in _Celsius (°C)_, and we want to understand it in _Fahrenheit (°F)_. Feature transformation can help us convert all the temperatures to _Fahrenheit_, making it easier for us to relate to and compare.

![celsius-fahrenheit.webp](./feature-engineering/celsius-fahrenheit.png)

## Feature transformation techniques
There are many different techniques for feature transformation, and the each technique has its purpose and can be applied depending on the _characteristics of the data_ and the specific _analysis goals_. In this lesson, we'll look at 2 techniques used for transformation - `scaling` and `binning`.

### 1. Scaling
_Feature scaling_ involves making sure that all our numeric features in the data have a similar range of values. This includes rescaling numerical features to a common range, such as `0` to `1` or `-1` to `1`. It ensures that all features have a similar influence on the analysis and prevents any one feature from dominating (or bullying 😁) the others.

Let's look at an example of scaling features in a dataset. Imagine we have a dataset containing both numeric and non-numeric features, we can scale the numeric features using the code snippet below.

```python
import pandas as pd

# Create a sample DataFrame with 7 features
data = {
    "Age": [25, 30, 22, 35],
    "Height": [160, 170, 155, 175],
    "Weight": [55, 60, 50, 65],
    "Gender": ["Male", "Female", "Female", "Male"],
    "Income": [50000, 60000, 40000, 70000],
    "Education": ["Bachelor's", "Master's", "Bachelor's", "PhD"],
    "Experience": [2, 5, 1, 7]
}
df = pd.DataFrame(data)

# Separate the numeric features for scaling
numeric_features = ["Age", "Height", "Weight", "Income", "Experience"]
numeric_df = df[numeric_features]

# Before scaling
print("Original DataFrame:")
print(df)

# Applying feature scaling using Min-Max Scaling only to numeric features
scaled_numeric_df = (numeric_df - numeric_df.min()) / (numeric_df.max() - numeric_df.min())

# Modify the scaled values to ensure they are positive
scaled_numeric_df = scaled_numeric_df + abs(scaled_numeric_df.min())

# Convert scaled values to one significant figure
scaled_numeric_df = scaled_numeric_df.round(1)

# Combine the scaled numeric features with non-numeric features
df_scaled = df.copy()
df_scaled[numeric_features] = scaled_numeric_df

# After scaling
print("\nScaled DataFrame:")
print(df_scaled)
```

```
Original DataFrame:

               Age  Height  Weight  Gender  Income   Education  Experience
            0   25     160      55    Male   50000  Bachelor's           2
            1   30     170      60  Female   60000    Master's           5
            2   22     155      50  Female   40000  Bachelor's           1
            3   35     175      65    Male   70000         PhD           7

Scaled DataFrame:

               Age  Height  Weight  Gender  Income   Education  Experience
            0  0.2     0.2     0.3    Male     0.3  Bachelor's         0.2
            1  0.6     0.8     0.7  Female     0.7    Master's         0.7
            2  0.0     0.0     0.0  Female     0.0  Bachelor's         0.0
            3  1.0     1.0     1.0    Male     1.0         PhD         1.0
```

We used `Min-Max (or Normalization)` scaling technique to scale the numeric features (Age, Height, Weight, Income, and Experience), but then we modified the scaled values to ensure they are positive, by adding the absolute minimum value of the scaled data. Other scaling techniques includes 
- Standardization (or Zero Score)
- Max scaling
- Robust Scaling
- Power
- Box-Cox 
- Quantile 
- Rank 
- Unit Vector Scaling

#### Practice

### 2. Binning
Binning is the process of dividing a continuous feature (e.g., age) into discrete intervals or `bins`. It's like creating age groups to make it easier to understand and analyze the data. For example, let's say we have a dataset of customer ages, and we want to bin the ages into 5 bins, the we have

- 0-18 years old
- 19-30 years old
- 31-45 years old
- 46-60 years old
- 61+ years old

We can then assign each customer to a bin based on their age. This would allow us to use the binned age as a categorical feature, rather than wide range of continuos values. Binning helps simplify the data and make it easier to interpret and analyze, thereby allowing us to summarize the data in a meaningful way and uncover insights that may not be apparent when looking at individual values.

Let's use another example to demonstrate binning. Suppose we have a dataset containing information about students' test scores, and we want to bin their scores into different performance categories, such as `Low`, `Medium`, and `High`. Here's a sample DataFrame with six features: `Student_ID, Math_Score, Science_Score, English_Score, History_Score`, and `Total_Score`:

```python
data = {
    "Student_ID": [101, 102, 103, 104, 105],
    "Math_Score": [85, 60, 78, 92, 70],
    "Science_Score": [72, 88, 55, 78, 82],
    "English_Score": [90, 85, 76, 88, 65],
    "History_Score": [80, 72, 85, 90, 78],
}

df = pd.DataFrame(data)

# Define the bin edges and labels for the "Math_Score" column
bin_edges = [0, 70, 80, 100]
bin_labels = ["Low", "Medium", "High"]

# Use pandas cut() function to perform binning
df['Math_Category'] = pd.cut(df['Math_Score'], bins=bin_edges, labels=bin_labels)

# Display the DataFrame with the new category column
print(df)
```

```
Student_ID   Math_Score  Science_Score  English_Score  History_Score  Math_Category
       101          85             72             90             80            High
       102          60             88             85             72            Low 
       103          78             55             76             85            Medium 
       104          92             78             88             90            High 
       105          70             82             65             78            Low 
```

In this example, we used the pandas `cut()` function to bin the `Math_Score` column into three categories: "Low" (scores below 70), "Medium" (scores between 70 and 80), and "High" (scores above 80). The new column "Math_Category" has been added to the DataFrame to store the respective category for each student's math score.

Different binning techniques can be used depending on the data and analysis goals. Here are some common binning techniques:
- **Equal Width**: Dividing the data into bins of equal width. For example, dividing age into bins like "0-10 years," "11-20 years," etc.
- **Equal Frequency**: Dividing the data into bins with an equal number of data points. This can help handle `skewed` data.
- **Custom**: Defining specific bins based on domain knowledge or specific requirements.

<aside>

**_Lesson Summary..._**

**_Feature transformation_** is the process of changing the way data is represented or organized to make it more suitable for analysis and modeling. There are several popular techniques used in feature transformation and each technique has its purpose and can be applied depending on the characteristics of the data and the specific analysis goals. A summary of the techniques covered and more is given in the table below.
</aside>

```
| Technique                  | What it does                                                                            |
| -------------------------- | --------------------------------------------------------------------------------------- |
| Scaling                    | Makes the data have a similar range of values.                                          |
| Normalization              | Centers the data around a mean of 0 and a standard deviation of 1.                      |
| Transformation             | Applies a mathematical transformation to the data to make it more linearly correlated.  |
| Log transformation         | Takes the logarithm of the data, which can help to make the distribution more normal.   |
| Reciprocal transformation  | Takes the reciprocal of the data, which can help to make the distribution more uniform. |
| Square root transformation | Takes the square root of the data, which can help to make the distribution more normal. |
```





### 👩🏾‍🎨 Practice: Feature transformation... 🎯

<br>

> ➡️ In the next section, we'll be looking at `Feature encoding` 🎯.