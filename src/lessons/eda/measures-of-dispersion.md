# Measure of Dispersion

<aside>

**_Definition..._**

**_Measure of dispersion_**, also known as _measures of variability_ or _measures of spread_, are statistical measures that provide information about the spread or variability of a dataset. They help us understand how the data points are dispersed or scattered around the central value. This measure includes calculating the `Range`, `Variance`, and `Standard deviation`.

</aside>

<div style="position: relative; padding-bottom: 56.25%; height: 0;"><iframe src="https://www.youtube.com/embed/R4yfNi_8Kqw" title="Web Scrapping Intro" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 2px solid grey;"></iframe></div>

Let's consider another example using a group of students and their weight. Suppose we have the following weights (in kilograms) for a class of students: `50, 55, 60, 65,` and `70`.

#### Range
The range is calculated by subtracting the minimum weight from the maximum weight. In this case, the range is calculated below and this tells us that the weights vary by 20 kilograms within the class.

<aside>

```python
70 - 50 = 20 kg
```
</aside>

#### Variance
Variance measures the average squared deviation of each weight from the mean. It gives us an idea of how spread out the weights are. To calculate the variance:

<aside>

```python
Step 1: Calculate the mean weight: (50 + 55 + 60 + 65 + 70) / 5 = 60 kg
Step 2: Calculate the squared difference from the mean for each weight: 
        (50 - 60)^2, (55 - 60)^2, (60 - 60)^2, (65 - 60)^2, (70 - 60^2
Step 3: Sum up the squared differences: (100 + 25 + 0 + 25 + 100) = 250
Step 4: Divide the sum by the number of data points (5) to get the variance: 
        250 / 5 = 50.
```
</aside>

#### Standard Deviation
The standard deviation is the square root of the variance. It represents the average distance of each weight from the mean. In this case, the standard deviation is the square root of 50, which is approximately 7.07 kg.

Overall, these measures of dispersion help us understand how the weights of students are spread out within the class. A larger range, variance, or standard deviation indicates greater variability or dispersion of the weights, while a smaller value suggests that the weights are closer together.

<!-- ![measure-of-dispersion.png](./eda/measure-of-dispersion.png) --> 

## Measure of dispersion using Python
Python provides various libraries, such as NumPy and Pandas, that make it easy to calculate measures of dispersion. Here's an example using the `Numpy` library to calculate the range, variance, and standard deviation of the weight dataset.

<iframe src="https://trinket.io/embed/python3/27ffe23790?toggleCode=true&runOption=run" width="100%" height="356" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

In the code snippet above, the `np.max()` and `np.min()` functions find the maximum and minimum values in the dataset, allowing us to calculate the range. The `np.var()` function calculates the variance, and the `np.std()` function calculates the standard deviation. 

<aside>

**_Lesson summary..._**

By considering _measures of dispersion_, we can better understand the variability of data and how individual values deviate from the central value. This information is useful in comparing datasets, identifying outliers, and making informed decisions based on the spread of the data.
</aside>

### 👩🏾‍🎨 Practice: Measures of central tendency... 🎯 


Consider the following dataset representing the test scores of a group of students in a class:

```python
[85, 90, 75, 80, 95, 70, 85, 88, 82, 78]
```

1. Calculate the **range** of the test scores.
2. Calculate the **variance** of the test scores.
3. Calculate the **standard deviation** of the test scores.
4. Explain in simple terms what each of these measures of dispersion tells us about the spread or variability of the test scores.


> ➡️ Next, we'll be looking at `Correlation analysis` analysis 🎯.
