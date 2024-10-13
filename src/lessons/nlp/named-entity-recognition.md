# Named Entity Recognition
Have you ever imagined how computer knows different names of people, places, brands, dates, and so on? Imagine you have a friend who loves talking about different things like people's names, places, dates, and more. When your friend reads a story or an article, they automatically highlight these important things in different colors. Named Entity Recognition (NER) is like your friend's skill, but for computers and text.

![ner.png](./nlp/ner.png)


<aside>

**_Definition..._**

**_NER_** seeks to `locate` and `classify` named entities mentioned in a text or document into pre-defined categories such as person names, organizations, locations, medical codes, time expressions, quantities, monetary values, percentages, and so on.
</aside>

There are generally 2 operations we need to perform to achieve _NER_ in a given document:
- **Identification**: This is where all the entities in a given text or document is identified.
- **Classification**: All identified entities are classified as belonging to a particular predefined entity group.

For example, if we are to perform _NER_ on a text such as 

            Ope Bukola is the CEO of Kibo Inc

First, we need to identify all the entities in the text, which are `Ope Bukola` and `Kibo Inc`. Next, we classify each entity into a predefined group. Here, we can classify _Ope Bukola_ as a `PERSON`, and _Kibo Inc_ as a type of `ORGANISATION`.
 

<div style="position: relative; padding-bottom: 56.25%; height: 0;"><iframe src="https://www.youtube.com/embed/Gn_PjruUtrc" title="Sample Data Science Project" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>

<details>
<summary><b> Try out NER tool</b></summary>

Check out this **<a href="https://demos.explosion.ai/displacy-ent" target="_blank"> NER demo </a>**

</details>

NER is still a growing a technology which already has manny use cases and wide applications. Some of its applications include:
- **Sentiment analysis**: NER can be used to improve the accuracy of sentiment analysis by identifying named entities in the text and understanding their context.
- **Information extraction**: NER can be used to extract information from text, such as the names of people and organizations mentioned in a news article.
- **Machine translation**: NER can be used to improve the accuracy of machine translation by identifying named entities in the source language and translating them correctly in the target language.
- **Question answering**: NER can be used to answer questions about text by identifying the entities mentioned in the question and finding the relevant information in the text.

Next, let's look at how we can perform NER with Spacy using some random text. Feel free to edit the text and try it out by opening the code snippet in **[Google Colab](https://colab.research.google.com/gist/wasiu-yusuf/4388604473b8c059e389524cf52844a8/ner_with_spacy.ipynb)**.

<script src="https://gist.github.com/wasiu-yusuf/4388604473b8c059e389524cf52844a8.js"></script>

In the code above, we first extracted the entities in the text and their corresponding labels. Next we used the `.render()` function in `displacy`, the visualizer for spacy, to visualize the entities in the text.


<aside>

**_Lesson Summary..._**

**_NER_** seeks to locate and classify named entities mentioned in a text or document into pre-defined categories such as person names, organizations, locations, medical codes, time expressions, quantities, monetary values, percentages, and so on.

There are 2 operations to perform in NER: 
- Entity identification
- Entity classification
</aside>


<br>

> ➡️ Next, we'll try some practice exercises based on what we've learned so far this week... 🎯.
