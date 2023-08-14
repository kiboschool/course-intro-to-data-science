# Intro to Deep Learning
Imagine you're teaching a robot to recognize different types of numbers. You show the robot lots of pictures of these numbers and tell it which one is which. As the robot sees more pictures, it learns to identify the numbers on its own. That's kind of like how deep learning works!

Deep learning is a type of artificial intelligence where computers learn from examples, just like you teach your pet new tricks. Instead of giving the computer a list of rules, you show it a bunch of examples and let it figure things out by itself. 

Deep learning has been used to achieve state-of-the-art results in a wide variety of tasks, including:

- **Image recognition**: Identifing objects in images such as classifying images of `cats` and `dogs`.
- **Natural language processing**: To understand and process natural language. For example, to translate languages, answer questions, and summarize text like `ChatGPT`.
- **Speech recognition**: To recognize speech such as transcribing audio recordings into text.
- **Machine translation**: To translate text from one language to another such as translating English text into _Swahili_.
- **Medical diagnosis**: To diagnose medical conditions such as identifying cancer cells in images.

These are just few of its applications since deep learning is a rapidly growing field, and new applications are being developed all the time. As the technology continues to improve, it is likely that deep learning will become even more widely used in the years to come. At the backbone of DL is `neural networks` which is used to do all the gymnastics behind the scene.


## Neural networks

<aside>

**_Definition..._**

**_Neural networks_** is a type of ML model that is inspired by the human brain. It is made up of a network of nodes, called neurons, that are connected to each other. The neurons in a neural network work together to learn from data and make predictions..
</aside>

<div style="position: relative; padding-bottom: 56.25%; height: 0;"><iframe width="100%" height="415" src="https://www.youtube.com/embed/jmmW0F0biiz0" title="Linking your CSS" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>

While training a neural network, the input data is passed through a neural network from the input layer to the output layer. The input data is multiplied by the `weights` of the neurons in the input layer. The results are then passed to the next layer, where they are multiplied by the `weights` of the neurons in that layer. 

This process continues until the data reaches the output layer, and it is referred to as `forward propagation`. Once the data has reached the output layer, it is passed through the activation function of the output layer. The result is the output of the neural network.

<img src="./dl/deep-learning-ocr.gif" alt="deep-learning-ocr.gif" style="display: block;
  margin-left: auto;
  margin-right: auto;
  height: 300px;
  width: 95%">

At each layer, the data is also passed through an activation function. The activation function determines how the data is processed by the neurons in that layer. The neural network is then updated using `backpropagation`. 

**Backpropagation** is the process of calculating the errors in the output layer and then propagating these errors back through the neural network to the input layer. The weights of the neurons are then adjusted to minimize the errors.

<img src="./dl/backpropagation.gif" alt="backpropagation.gif" style="display: block;
  margin-left: auto;
  margin-right: auto;
  height: 300px;
  width: 95%">

This process is repeated until the neural network converges, meaning that it has learned to represent the data as accurately as possible.


## Machine learning vs Deep learning
<!-- <div style="position: relative; padding-bottom: 56.25%; height: 0;"><iframe width="100%" height="415" src="https://www.youtube.com/embed/q6kJ71tEYqM" title="Linking your CSS" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div> -->

