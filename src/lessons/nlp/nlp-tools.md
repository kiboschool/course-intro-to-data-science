# <u> NLP Tools and Libraries </u>
Text are unstructured data that needs to be structured while carrying out any processing or analysis on them. To achieve this, there are varieties of tools, both libraries and cloud-based applications, that are available for different tasks in the NLP pipeline. Since we can't go throuh all these tools, we'll focus on 2 popular libraries - `NLTK` and `Spacy`, and a cloud-based solution - `Amazon comprehend`. 

<aside>

**_NOTE_** 

- The goal here is to get familiar with these tools. 
- In subsequent lessons, we'll be using them for NLP tasks.
</aside>

## NLTK
Natural Language Toolkit (NLTK) is a powerful and widely used Python library for working with human language data. It provides tools, algorithms, and resources that enable us to perform various NLP tasks, ranging from basic text processing to more advanced linguistic analysis.

<br>
<div style="position: relative; padding-bottom: 56.25%; height: 0;"><iframe width="100%" height="415" src="https://www.youtube.com/embed/WYge0KZBhe0?si=Pu4IMH3X2UA5UT5U" title="Linking your CSS" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>

<details>
<summary><b> Further reading - NLTK (Optional) </b></summary>

To get more understanding about this tool, you can explore the official documentation using the link below.

**[Getting started with _NLTK_](https://www.nltk.org/)**
</details>

## Spacy

SpaCy is another popular Python library designed specifically for natural language processing tasks. It's known for its speed, efficiency, and ease of use, making it a favorite among developers and researchers working with large amounts of text data. SpaCy provides a streamlined API for various NLP tasks, allowing users to quickly process and analyze text without the need for extensive configuration.

<br>
<div style="position: relative; padding-bottom: 56.25%; height: 0;"><iframe width="100%" height="415" src="https://www.youtube.com/embed/NiIJIU5BEBU" title="Intro to Spacy" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>

One of the key features of SpaCy is its pre-trained models that can perform tasks like tokenization, part-of-speech tagging, named entity recognition, and syntactic parsing. 


<details>
<summary><b> Further reading - Spacy (Optional) </b></summary>

To get more understanding about this tool, you can explore the official documentation using the link below.

**[Getting started with _Spacy_](https://spacy.io/usage/spacy-101)**
</details>

## Amazon comprehend

Amazon Comprehend is a `cloud-based` service provided by Amazon Web Services (AWS). It's designed to help us analyze and gain insights from text data in a scalable and efficient manner.

<aside>

**_NOTE_** 

- Amazon comprehend is a paid subscription service. 
- However, you can use its `limited-version` for free by creating a **[student account](https://aws.amazon.com/education/awseducate/)**.
</aside>

<br>
<div style="position: relative; padding-bottom: 56.25%; height: 0;"><iframe width="100%" height="415" src="https://www.youtube.com/embed/BKgTJCJ0eGg" title="Amazon comprehend" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>

One of the advantages of Amazon Comprehend is that it's a managed service, which means AWS takes care of the underlying infrastructure, making it easier to incorporate NLP capabilities into applications without worrying about the technical details. It can perform tasks such as...
- Sentiment analysis
- Entity recognition
- Keyphrase extraction
- Language detection 
- Topic modeling. 

This means it can automatically determine the sentiment (positive, negative, neutral) expressed in a piece of text, identify entities (like names, dates, and locations), extract key phrases that summarize the content, detect the language the text is written in, and uncover the main topics discussed in the text.

<details>
<summary><b> Further reading - Amazon Comprehend (Optional) </b></summary>

To get more understanding about this tool, you can explore the official documentation by following the steps below.

1. Create a free student account using **[AWS Educate](https://aws.amazon.com/education/awseducate/)**
2. Then get started with **[_Amazon Comprehend_](https://docs.aws.amazon.com/comprehend/latest/dg/what-is.html)**
</details>

<aside>

**_Lesson Summary..._**

**_NLP_** tools and libraries offer various functionalities for `Sentiment analysis`, `Entity recognition`, `Keyphrase extraction`, `Language detection`, and `Topic modeling`. Depending on our specific needs and project requirements, we can choose the most suitable tool or library to help us achieve our NLP goals.

In this lesson, we've seen an overview of 3 different NLP tools and libraries.
- NLTK
- Spacy
- Amazon Comprehend
</aside>


<br>

> ➡️ Next, we'll look at `Text preprocessing`... 🎯.
