# <u> Sentiment Analysis </u>
Sentiment analysis is like having a machine read people's words and figure out how they feel about something. Just like when we talk to friends and they might sound happy, sad, or excited, computers can also listen to what people write online and understand their emotions.

<img src="./nlp/sentiment-analysis.gif" alt="sentiment-analysis.gif" style="display: block;
  margin-left: auto;
  margin-right: auto;
  height: auto">


<aside>

**_Definition..._**

**_Sentiment analysis_** is the process of extracting subjective information from text, such as the opinions, attitudes, and emotions expressed by the author. It is often used to gauge public opinion, identify customer sentiment, and track brand reputation among many other applications.
</aside>

Imagine if you wrote a message about a movie you just watched, and you were either happy, sad, or just okay with it. Sentiment analysis helps a computer figure out if your message is thumbs up, thumbs down, or somewhere in between. Check out the video below to gain more understanding about sentiment analysis.

<div style="position: relative; padding-bottom: 56.25%; height: 0;"><iframe src="https://www.youtube.com/embed/i4D5DZ5ZG-0" title="Sample Data Science Project" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 2px solid grey;"></iframe></div>

To analyse sentiments in a text or document, we can look at it from 4 different levels. To understand these, we'll use a movie reviews dataset.

**Document level**: This type of analysis looks at the overall sentiment of an entire text or document. It aims to determine whether the document is _positive_, _negative_, or _neutral_. Suppose you have a collection of movie reviews about a recent blockbuster film, Document-level sentiment analysis would involve reading each entire review and categorizing it as _positive_, _negative_, or _neutral_ based on the overall tone of the review.

**Sentence level**: Each sentence is classified as positive, negative, or neutral, regardless of the sentiment of the entire text or document. For example, if a reviewer says...

                            The acting was great, but the plot was confusing.

The analysis would identify that the first part of the sentence is _positive_ (praising the acting) and the second part is _negative_ (criticizing the plot).

**Aspect level**: focuses on extracting sentiments related to specific aspects or features mentioned in the text. For example, aspect-based sentiment analysis could reveal that audiences generally liked the acting and special effects but had mixed feelings about the ending.

**Entity** or **feature level**: Similar to aspect-based analysis, this analysis identifies sentiments towards named entities, which could be people, places, products, or any other entities mentioned in the text. If the movie features a popular actor, entity-level sentiment analysis would focus on how people perceive that actor's performance.

## Sentiment analysis of movie reviews
Let's see how we can perform sentiment analysis on a movie review dataset. The dataset we'll be using comes with the `NLTK` library, so all we need to do is download the dataset as shown in the code snippet below. Play around with the `additional_test_reviews` by adding your own reviews and see how the model classify it as either _positive_ or _negative_.

<aside>

**_NOTE_**

- To run this, you'll need to open it in `colab`.
</aside>

<script src="https://gist.github.com/wasiu-yusuf/bfcd2537d3ec890552c682944c068260.js"></script>

In this code snippet, we're using the `NLTK` library to perform sentiment analysis on the _movie reviews_ dataset. We load positive and negative reviews, split the data into training and testing sets, and then use the `Naive Bayes` classifier to train the model. The `extract_features` function is used to extract relevant features from the words in the reviews. Next, we evaluated the model's accuracy on the testing data.

Finally, we added three additional test cases (`additional_test_reviews`). After evaluating the classifier's accuracy, the code will print the predicted polarity, _positive_ or _negative_, for each of these additional test cases.

<aside>

**_Lesson Summary..._**

**_Sentiment analysis_** is the process of extracting subjective information from text, such as the opinions, attitudes, and emotions expressed by the author. It is often used to gauge public opinion, identify customer sentiment, and track brand reputation among many other applications.

There are 4 different sentiment analysis level highlighted in this lesson, depending on the type of problem we are trying to solve.
- Document level
- Sentence level
- Aspect level
- Entity level
</aside>


<br>

> ➡️ Next, we'll look at `Named entity recognition...` 🎯.
