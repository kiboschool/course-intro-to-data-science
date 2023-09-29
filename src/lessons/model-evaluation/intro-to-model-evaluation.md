# Intro to Model Evaluation Techniques

Imagine you have a friend who loves guessing the outcome of football matches. To see how good they are at predicting, you give them a few past matches to predict the winners. After they make their guesses, you show them the actual outcomes and calculate how many they got right and how many they got wrong. This way, you can tell how accurate their predictions are.

<img src="./model-evaluation/model-evaluation.png" alt="model-evaluation.jpeg" width="96%" height="350px">

Similarly, in Machine Learning, we use different evaluation techniques to measure the accuracy of our models. We split our data into a training set (like studying) and a testing set (like a test). We train the model on the training set and then use the testing set to see how well it predicts the outcomes. If the model makes accurate predictions, it means it has learned well from the training data.

<aside>

**_Definition..._**

**_Model evaluation techniques_** are methods used to assess the performance and accuracy of a trained model. By using these evaluation techniques, we can assess the model's performance and make improvements if needed
</aside>

<div style="position: relative; padding-bottom: 56.25%; height: 0;"><iframe src="https://www.youtube.com/embed/LbX4X71-TFI" title="Machine Learning" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 2px solid grey;"></iframe></div>

In this intro video, various evaluation metrics used for ML models was highlighted, including those for classification and regression tasks. It emphasizes the importance of choosing the appropriate metric based on the problem and provides an overview of key metrics such as accuracy, precision, recall, and F1 score among others. For model evaluation techniques, the following point should be noted:

- Evaluating ML models is crucial for understanding their performance and identifying areas of improvement.
- For classification tasks, _accuracy_ is a popular metric but may not always be sufficient. 
- _Precision_ and _recall_ provide more detailed insights into the model's performance on positive instances.
- When dealing with multi-class classification, various approaches exist, such as calculating metrics for individual classes and taking their average or applying weights based on class importance.
- The _F1 score_, a combination of precision and recall, is often used to better evaluate the model.
- Regression evaluation metrics include mean absolute error, mean squared error, root mean squared error, and R-squared (coefficient of determination) among others.

Each of these techniques will be discussed in subsequent lessons, where we'll be see how we can use them in evaluating ML models.


> ➡️ Next, we'll look at `Confusion matrix`... 🎯