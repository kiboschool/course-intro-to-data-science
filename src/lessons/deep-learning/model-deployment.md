# Model deployment
In previous lessons, we have developed different ML models for different tasks. In this lesson, we'll see how we can take one of our trained models and deploy it so that others can use our model from anywhere around the world. Sounds cool right?


<aside>

**_Definition..._**

**_Deployment_** is the process of making a ML model available for use online. This involves taking the model that has been trained and tested on new data, and then making it available to users so that they can use it to make predictions.
</aside>

## Deploying a Sentiment Analysis Model
In this task, you will learn how to deploy a machine learning model that predicts the sentiment of customer reviews. You will use a pre-trained sentiment analysis model and create a simple web application using Flask to allow users to input their reviews and receive sentiment predictions

This task will guide you through the process of setting up the deployment environment, creating a Flask app, and integrating the model for real-time predictions. Here are the steps we'll follow:

- Save our pre-trained sentiment analysis model
- Create a `Flask API` with a single endpoint.
- Load the saved model.
- Run the model
- Deploy model locally with `ngrok`.

### Save pre-trained model
In week 8 (NLP), we built a sentiment analysis model as the assignment. This model is what we'll be using for this lesson. First, we need to rerun the model and save it. To do that, we add the following code to the last part of our code and run it.

```python
import joblib

# save the model to a .pkl file
joblib.dump(model, 'sentiment_model.pkl')
```

Here, `joblib` is a library we can use to save the final model. Make sure you note the location where the model is saved, as the file will be needed for deployment.

### Create Flask application

### Load the saved model

### Run the model

### Deploy the model


> Putting everything together - model deployment
<div style="position: relative; padding-bottom: 56.25%; height: 0;"><iframe width="100%" height="415" src="https://www.youtube.com/embed/IC0o_FRiX-sw" title="Computer Vision" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>
</details>
