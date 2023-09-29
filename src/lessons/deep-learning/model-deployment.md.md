# Practice - Model Deployment
So far in this course, we have developed different ML models for different tasks. In this practice exercise, we'll see how we can take one of our trained models and deploy it so that others can use our model from anywhere around the world. Sounds cool right?


<aside>

**_Definition..._**

**_Deployment_** is the process of making a ML model available for use online. This involves taking the model that has been trained and tested on new data, and then making it available to users so that they can use it to make predictions.
</aside>

## Deploying a Sentiment Analysis Model
In this practice, you will learn how to deploy a machine learning model that predicts the sentiment of customer reviews. You will use a pre-trained sentiment analysis model and create a simple web application using Flask to allow users to input their reviews and receive sentiment predictions

This task will guide you through the process of setting up the deployment environment, creating a Flask app, and integrating the model for real-time predictions. Here are the steps we'll follow:

- Save our pre-trained sentiment analysis model
- Create a `Flask API` with a single endpoint.
    - Load the saved model.
    - Make sentiment predictions
- Run the model.
- Deploy model locally with `Ngrok`.
    - Alternatively, you can use **Render** or **Speedrun**.

### 1. Save pre-trained model
In week 8 (NLP), we built a sentiment analysis model as the assignment. This model is what we'll be using for this lesson. First, we need to rerun the model and save it. To do that, we add the following code to the last part of our code and run it.

```python
import joblib

# save the model to a .pkl file
joblib.dump(model, 'sentiment_model.pkl')
```

Here, `joblib` is a library we can use to save the final model. Make sure you note the location where the model is saved, as the file will be needed for deployment.

### 2. Create Flask Application
In this lesson, we'll be using `Flask` as our prefered framework. As you've seen in the web application development course, Flask can serve different purpose depending on the use case. The goal here is to build an endpoint that we can use to _interact_ with the model, which can be broken down into:

- Create a Flask app that listens to incoming `POST` requests on a specific route.
- Define a function that processes incoming data and returns predictions from the model.
- Load the save _model_.
- Set up the necessary routes to handle user inputs and predictions.

To achieve this, we'll create all these using the code snippet below:

```python
from flask import Flask, request, jsonify
import joblib

app = Flask(__name__)

# Load the saved model
model = joblib.load('sentiment_model.pkl')

# create a route that manages user request and does sentiment prediction
@app.route('/predict', methods=['POST'])
def predict():
    data = request.get_json()
    text = data['text']
    vectorized_text = vectorizer.transform([text])
    prediction = model.predict(vectorized_text)[0]
    return jsonify({'sentiment': prediction})
```

Save the code above in a file named `app.py`.

### 3. Run the model
The goal here is to test the Flask app by:
- Running the Flask app locally and testing it by sending sample inputs.
- Ensuring that the web app can predicts sentiment based on the user's input.

```python
if __name__ == '__main__':
    app.run()
```

### 4. Deploy the model
The goal here is to make our model accessible to everyone online. Here, we'll use `Ngrok` to deploy it locally and generate a URL that is accessible online. To achieve this, we can do the following:

- install _Ngrok_ using `pip install ngrok`.
- Run the Flask app using `python app.py`.
- While app is running, open a new _terminal_ in the same directory Ngrok is installed.
- Use the command: `ngrok http 5000` (assuming your Flask app is running on port _5000_).
    - ngrok will then generate a public URL, e.g., `http://kibo1234.ngrok.io`
- To access your model, send a POST request to `http://kibo1234.ngrok.io/predict`.

With these, your model is now live......`Hurray!!!`

<details>
<summary><b> Solution video - Model deployment </b></summary>

<div style="position: relative; padding-bottom: 56.25%; height: 0;"><iframe width="100%" height="415" src="https://www.youtube.com/embed/DPjp9hKq4qn8" title="Computer Vision" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>
</details>

### `Enjoy this and have a lot of fun`
