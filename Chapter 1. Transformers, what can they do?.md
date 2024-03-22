# Transformers, what can they do?
In this section, we will look at what **Transformer models** can do and use our first tool from the **🤗 Transformers** library: the `pipeline()` function.

Transformers are everywhere!  
Before diving into how Transformer models work under the hood, let’s look at a few examples of how they can be used to solve some interesting NLP problems.

# Working with pipelines
The most basic object in the 🤗 Transformers library is the `pipeline()` function.  
It connects a model with its necessary preprocessing and postprocessing steps, allowing us to directly input any text and get an intelligible answer:

Some of the currently available pipelines are:
- **feature-extraction**
- **fill-mask**
- **ner (named entity recognition)**
- **question-answering**
- **sentiment-analysis**
- **summarization**
- **text-generation**
- **translation**
- **zero-shot-classification**

```python
from transformers import pipeline
classifier = pipeline("sentiment-analysis")
classifier("I've been waiting for a short HuggingFace course my whole life.")
```  
We can even pass several sentences!
```python
classifier(["I've been waiting for a short HuggingFace course my whole life.", "I hate this so much"])
```

By default, this pipeline selects a particular pretrained model that has been fine-tuned for sentiment analysis in English. 
The model is downloaded and cached when you create the classifier object. If you rerun the command, the cached model will be used instead and there is no need to download the model again.

There are three main steps involved when you pass some text to a pipeline:
- The text is preprocessed into a format the model can understand.
- The preprocessed inputs are passed to the model.
- The predictions of the model are post-processed, so you can make sense of them.

# Zero-shot classification
We’ll start by tackling a more challenging task where we need to **classify texts that haven’t been labelled.**  
For this use case, the **`zero-shot-classification` pipeline* is very powerful: it allows you to specify which labels to use for the classification, so you don’t have to rely on the labels of the pretrained model. 

```python
from transformers import pipeline
classifier = pipeline("zero-shot-classification")
classifier("This is a course about the Transformers library", 
            candidate_labels=["education", "politics", "business"],)
```
Output:


This pipeline is called **zero-shot** because you don’t need to fine-tune the model on your data to use it. It can directly return probability scores for any list of labels you want!

# Text generation
The main idea here is that you provide a prompt and the model will auto-complete it by generating the remaining text.

```python
from transformers import pipeline
generator = pipeline("text-generation")
generator("In this course, we will teach you how to")
```

Output:

You can control how many different sequences are generated with the argument `num_return_sequences` and the total length of the output text with the argument `max_length`.

# Using any model from the Hub in a pipeline
The previous examples used the default model for the task at hand, but you can also choose a particular model from the [Hub](https://huggingface.co/models) to use in a pipeline for a specific task — say, text generation.
Let’s try the [distilgpt2](https://huggingface.co/distilbert/distilgpt2) model! Here’s how to load it in the same pipeline as before:

```python
from transformers import pipeline
generator = pipeline("text-generation", model="distilgpt2")
generator( "In this course, we will teach you how to",
            max_len = 30,
            num_return_sequences=2)
```
Output