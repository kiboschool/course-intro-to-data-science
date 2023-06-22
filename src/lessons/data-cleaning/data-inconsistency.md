# Data Outliers
Handling data outliers is crucial because outliers can significantly impact the accuracy and reliability of data analysis. Imagine a dataset representing the weight of individuals in a class, where all values range from 35kg to 60kg, except for one extreme value of **109kg**. This extreme _outlier_, possibly due to an error or anomaly, can skew the average weight calculation, making it highly misleading. 

By identifying and handling outliers, we aim to ensure that our analysis is based on reliable and representative data, enabling us to make more accurate decisions and draw meaningful insights from the data.


## Outlier

<aside>

**_Definition..._**

**_Outliers_** refer to data points that are significantly different from the majority of the other data points in a dataset. 



</aside>

Outliers can occur due to various reasons, such as measurement errors, data entry mistakes, equipment glitches, or unusual circumstances. They can have a significant impact on data analysis because they can skew (or change) statistical measures and affect the overall trends and patterns observed in the data. Let's look at some examples...

##### Example 1
Imagine you have a dataset representing the heights of a group of people. Most of the heights fall within a certain range, but there may be a few extreme values that are much higher or lower than the rest. These extreme values are _outliers_.

##### Example 2
Consider a small dataset sample...

`[15, 101, 18, 7, 13, 16, 11, 21, 5, 15, 10, 9]`

Which of the data point is the outlier?

<details>
<summary> Reveal data outlier </summary>

By looking at it, one can quickly say `101` is an outlier because it is much larger than the other values. 

</details>

Now let's look at the impact of this outlier on the data using the table below.

                    | Without outlier       | With outlier            |
                    |-----------------------|-------------------------|
                    | Mean: 20.08           | Mean: 12.72             |
                    | Median: 14.0          | Mean: 13.0              |
                    | Mode: 15              | Mode: 15                |
                    | Variance: 614.74      | Variance: 21.28         |
                    | Std dev: 24.79        | Std dev: 4.61           |

We can obviously see how the outlier has affected the dataset. Hence, identifying and handling outliers is important because they can have a significant impact on our data analysis, and may lead to misleading conclusions. Imagine having numerous outlier in patient health data, thereby leading to wrong diagnosis or prescription 🤦🏾‍♂️. Consequently, we need to find a way to handle outliers in our dataset.

### Finding outliers
There are several techniques to find outliers in a dataset. One simple technique is using the range rule. Let's say we have a dataset representing the number of hours students study each day, ranging from 1 to 10 hours. If we consider any value below 1 hour or above 10 hours as an outlier, we can easily identify them by looking at the data.

Another technique is using z-scores. We can calculate the z-score for each data point, which measures how far each value is from the mean in terms of standard deviations. If a z-score is significantly larger or smaller than 0 (e.g., above 2 or below -2), we can consider it as an outlier.

Additionally, we can use box plots to visualize the distribution of the data. Any data points that fall outside the whiskers of the box plot can be considered outliers. More on visualization will be discussed in subsequent weeks.

Lastly, the [percentile](https://statisticsbyjim.com/basics/percentiles/) approach identifies outliers by comparing data points to percentiles. For instance, if a data point is above the 95th percentile or below the 5th percentile, it might be considered an outlier. **This is the approach we'll adopt for this lesson**.

### Handling data outliers
There are several techniques to handle outlier but we'll only be looking at 3 in this course...
- Trimming
- Replacing
- Windsorization

#### 1. Trimming
Handling outliers using the trimming technique involves **_capping or trimming extreme values to a specified range_**. This approach allows us to keep the bulk of the data while removing or adjusting the outliers. Let's explain this concept using a simple example and provide a code sample using pandas.

##### Trimming example
Imagine we have a dataset of student grades, and we suspect there are outliers that might be affecting our analysis. We can use the trimming technique to remove the extreme values beyond a certain threshold. Let's say we decide to trim the top and bottom 5% of the data.

Here's an example code snippet using pandas to demonstrate how to handle outliers using the trimming technique:

```python
import pandas as pd

# Load the dataset
data = pd.read_csv('your_dataset.csv')

# Define the threshold as 3 standard deviations from the mean
threshold = 3 * data['column_name'].std()

# Identify outliers
outliers = data['column_name'] > threshold

# Trim the dataset by removing outliers
trimmed_data = data[~outliers]

# Print the trimmed dataset
print(trimmed_data)
```

In code above, the threshold is defined as `3 times the standard deviation of the column values`. Rows that have values above this threshold are considered outliers. The ~ operator is used to negate the boolean condition, selecting all the rows that do not contain outliers. Finally, the trimmed dataset is printed.

> By applying the trimming technique, you remove extreme outliers from the dataset, allowing for a more representative analysis of the majority of the data.

### 2. Replacing
Handling outliers using the replacing technique involves **_replacing extreme outlier values with more representative values_** in the dataset. This approach aims to mitigate the impact of outliers on data analysis without completely removing them. Using pandas, you can handle outliers using the _replacing_ technique by following these steps:

1. **Identify Outliers**: Use pandas to identify the outliers in the dataset. You can determine outliers based on statistical measures like z-scores or percentiles, or based on domain-specific knowledge.

2. **Replace Outliers**: Once the outliers are identified, you can replace them with more representative values. One common approach is to replace outliers with the median or mean value of the feature.

3. **Update the Dataset**: Modify the dataset by replacing the outliers with the chosen representative values. This can be done using pandas functions like `fillna()` or `replace()`.

Here's an example code snippet using pandas to handle outliers using the replacing technique:


```python
import pandas as pd

# Load the dataset
data = pd.read_csv('your_dataset.csv')

# Identify outliers
outliers = data['column_name'] > threshold

# Replace outliers with the median value
median_value = data['column_name'].median()
data.loc[outliers, 'column_name'] = median_value

# Print the updated dataset
print(data)
```

In the code snippet above, the outliers are identified based on a condition, such as values greater than a certain threshold. The outliers are then replaced with the median value of the column using the `loc` accessor. Finally, the updated dataset is printed.

> By applying the replacing technique, you replace extreme outliers with more representative values, allowing for a more accurate analysis of the data while still retaining the information from the outliers.

### 3. Winsorization
Handling outliers using the winsorization technique involves capping extreme values by replacing them with values that are closer to the rest of the data. This approach helps to minimize the impact of outliers on data analysis without completely eliminating them.

In pandas, you can handle outliers using the winsorization technique by following these steps:

1. Define the Threshold: Determine the threshold beyond which the values will be considered outliers. This threshold can be based on domain knowledge or statistical measures like z-scores or percentiles. We'll use percentile in this example.

2. Winsorize the Data: Use pandas' `clip()` function to perform winsorization. This function allows you to set upper and lower limits for the values. Any values above the upper limit will be replaced with the maximum value within that limit, and any values below the lower limit will be replaced with the minimum value within that limit.

Here's an example code snippet using pandas to handle outliers using the winsorization technique:

```python
import pandas as pd

# Load the dataset
data = pd.read_csv('your_dataset.csv')

# Define the upper and lower thresholds for winsorization
upper_threshold = data['column_name'].quantile(0.95)
lower_threshold = data['column_name'].quantile(0.05)

# Winsorize the data
winsorized_data = data['column_name'].clip(lower=lower_threshold, upper=upper_threshold)

# Update the dataset with winsorized values
data['column_name'] = winsorized_data

# Print the updated dataset
print(data)
```

The upper and lower thresholds are defined using quantiles, such as `0.95` for the upper threshold and `0.05` for the lower threshold. The `clip()` function is then used to winsorize the data by... 
- replacing values above the upper threshold with the **_maximum_** value within that limit
- replacing values below the lower threshold with the **_minimum_** value within that limit. 
- Finally, the dataset is updated with the winsorized values and printed.

> By applying the winsorization technique, extreme outlier values are capped, bringing them closer to the rest of the data distribution. This helps in reducing the impact of outliers while retaining valuable information from the dataset.

> **👩🏾‍🎨 Practice: Comparing Outlier 🎯**

In this lesson, we've seen how to identify and handle outliers using different techniques. Now let's gauge our understanding of these techniques.
1. Goto to your [Gradescope quiz]()
2. Attempt the quizes in `Comparing Outlier`.

<br>

> ➡️ In the next section, you'll be introduced to `data validation and documentation` 🏙️.