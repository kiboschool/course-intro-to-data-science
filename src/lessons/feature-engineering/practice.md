# Practice
<aside>

💡 This is your chance to put what you’ve learned into action.

- Try solving this practice challenge to check that you understand the concepts.

- Be ready to do additional googling to complete this exercise, if neccessary.

</aside>

## Car specification

Imagine you're working with a dataset containing information about cars and their specifications. Here's a sample dataset:

```python

Car ID:     [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
Brand:      ['Toyota', 'Ford', 'Honda', 'Chevrolet', 'Nissan', 'Toyota', 'Ford', 'Honda', 'Nissan', 'Chevrolet']
Mileage:    [25000, 35000, 15000, 45000, 30000, 20000, 40000, 28000, 32000, 38000]
Horsepower: [150, 200, 120, 180, 160, 140, 210, 130, 170, 190]
Fuel Type:  ['Gasoline', 'Diesel', 'Gasoline', 'Diesel', 'Gasoline', 'Hybrid', 'Diesel', 'Gasoline', 'Hybrid', 'Gasoline']
Price ($):  [20000, 25000, 18000, 22000, 23000, 26000, 24000, 21000, 27000, 23000]

```

1. **Scaling:** Use Standardization to scale the "Mileage" and "Horsepower" features. Calculate the scaled values for each feature.
2. **Binning:** Bin the "Horsepower" feature into three bins: 'Low', 'Medium', and 'High'. Assign each data point to the appropriate bin based on its horsepower.
3. **Label Encoding:** Convert the "Brand" feature using label encoding. Assign unique integer labels to each brand.
4. **One-Hot Encoding:** Perform one-hot encoding on the "Fuel Type" feature. Create new binary columns for each fuel type, where 1 indicates the presence of that fuel type and 0 indicates absence.
5. **Evaluation:** Discuss the trade-offs between label encoding and one-hot encoding for categorical features. Also, mention the potential benefits of adding polynomial features.


## Submission
You are required to submit documentation for practice exercises over the course of the term. Each one will count for 1/10 of your practice grade, or 2% of your overall grade.

- Practice exercises will be graded for completion not perfect correctness. 
- You have to document that you did the work, but we **won't** be checking if you got it right.
- You **MUST** upload your analysis/visuals as a single file to `Practice: Feature Engineering - Car specification` on **Gradescope** after the exercise to get the grade for this exercise.


Your log will count for credit as long as:
- It is accessible to your instructor, and
- It shows your own work.

