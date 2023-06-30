# Data Distribution
Imagine you have a dataset containing the ages of a group of people. Then, you want to understand how the ages are distributed, which means you want to see how many people fall into different age ranges. This is what data distribution is about, and `histograms` and  `density plots` are useful visualizations for this purpose.


### 1. Histogram
A histogram is used to visualize the distribution of a continuous variable by displaying the frequency or count of observations falling within specific intervals or bins. A histogram is like a bar graph that shows the frequency or count of scores falling within specific score ranges, known as `bins`. Each bar in the histogram represents a bin, and its height indicates the number of students with scores within that range. 

For example, if the histogram shows a tall bar around the 70-80 range, it means many students scored within that range. A histogram helps visualize the overall pattern and spread of the scores, allowing you to identify common score ranges or any outliers. Seaborn's `histplot()` function can be used to create histograms.

Suppose we have data on the exam scores of a class of students. A histogram helps us understand the distribution of scores. For example

```python
import seaborn as sns

# Assuming you have a list of test scores called 'scores'
scores = [78, 85, 90, 74, 92, 85, 76, 88, 80, 90, 85, 82, 94, 83]

# Create a histogram
sns.histplot(scores, bins=8)
plt.title('Distribution of Test Scores')
plt.xlabel('Scores')
plt.ylabel('Frequency')
plt.show()
```

![histogram](./data-viz/histogram.png)

### 2. Density plots
A density plot, on the other hand, is a smooth line that shows the distribution of data as a continuous curve. Instead of using bins like a histogram, a density plot estimates the probability density function of the data. 

It gives you an idea of how likely it is to find a data point within a certain range. In our age example, the density plot would show the likelihood of finding a person of a specific age. It can help you understand the overall shape of the distribution, such as whether it's symmetric, skewed to the right or left, or multi-modal (having multiple peaks). For example:

```python
import seaborn as sns

# Assuming you have a list of test scores called 'scores'
scores = [78, 85, 90, 74, 92, 85, 76, 88, 80, 90, 85, 82, 94, 83]

# Create a density plot
sns.kdeplot(scores)
plt.title('Density Plot of Test Scores')
plt.xlabel('Scores')
plt.ylabel('Density')
plt.show()
```

![density-plot.png](./data-viz/density-plot.png)

Now that we have an idea of data distribtipn using histogram and density plot, let's apply these distrubtion techniques on a real-life dataset.

