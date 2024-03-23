# 🤖 Transformers, what can they do 
In this section, we will look at what **Transformer models** can do and use our first tool from the **🤗 Transformers** library: the `pipeline()` function.


Transformers are everywhere!  
Before diving into how Transformer models work under the hood, let’s look at a few examples of how they can be used to solve some interesting NLP problems.

# 🔗 Working with pipelines
The most basic object in the 🤗 Transformers library is the `pipeline()` function. 
It connects a model with its necessary preprocessing and postprocessing steps, allowing us to directly input any text and get an intelligible answer:

```python
from transformers import pipeline
classifier = pipeline("sentiment-analysis")
classifier("I've been waiting for a short HuggingFace course my whole life.")
```
```
Output
```

We can even pass several sentences!
```python
classifier(["I've been waiting for a short HuggingFace course my whole life.", "I hate this so much"])
```
```
Output
```

By default, this pipeline selects a particular pretrained model that has been fine-tuned for sentiment analysis in English. 
The model is downloaded and cached when you create the classifier object. If you rerun the command, the cached model will be used instead and there is no need to download the model again.

There are three main steps involved when you pass some text to a pipeline:
- The text is preprocessed into a format the model can understand.
- The preprocessed inputs are passed to the model.
- The predictions of the model are post-processed, so you can make sense of them.

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

# 🎯 Zero-shot classification 🔫
We’ll start by tackling a more challenging task where we need to **classify texts that haven’t been labelled.**  
For this use case, the **`zero-shot-classification` pipeline* is very powerful: it allows you to specify which labels to use for the classification, so you don’t have to rely on the labels of the pretrained model. 

```python
from transformers import pipeline
classifier = pipeline("zero-shot-classification")
classifier("This is a course about the Transformers library", 
            candidate_labels=["education", "politics", "business"],)
```
```
Output
```


This pipeline is called **zero-shot** because you don’t need to fine-tune the model on your data to use it. It can directly return probability scores for any list of labels you want!

# 📝 Text generation
The main idea here is that you provide a prompt and the model will auto-complete it by generating the remaining text.

```python
from transformers import pipeline
generator = pipeline("text-generation")
generator("In this course, we will teach you how to")
```
```
Output
```

You can control how many different sequences are generated with the argument `num_return_sequences` and the total length of the output text with the argument `max_length`.

# 🗂 Using any model from the Hub in a pipeline
The previous examples used the default model for the task at hand, but you can also choose a particular model from the [Hub](https://huggingface.co/models) to use in a pipeline for a specific task — say, text generation.
Let’s try the [distilgpt2](https://huggingface.co/distilbert/distilgpt2) model! Here’s how to load it in the same pipeline as before:

```python
from transformers import pipeline
generator = pipeline("text-generation", model="distilgpt2")
generator( "In this course, we will teach you how to",
            max_len = 30,
            num_return_sequences=2)
```
```
Output
```

# ❎ Mask filling
The idea of this task is to fill in the blanks in a given text:
```python
from transformers import pipeline

unmasker = pipeline("fill-mask")
unmasker("This course will teach you all about <mask> models.", top_k=2)
```
```
Output
```

The top_k argument controls how many possibilities you want to be displayed. Note that here the model fills in the special <mask> word, which is often referred to as a mask token. Other mask-filling models might have different mask tokens, so it’s always good to verify the proper mask word when exploring other models. One way to check it is by looking at the mask word used in the widget.

# 🧩 Named entity recognition (NER)
NER is a task where the model has to find which parts of the input text correspond to entities such as persons, locations, or organizations. Let’s look at an example:

```python
from transformers import pipeline

ner = pipeline("ner", grouped_entities=True)
ner("My name is Sylvain and I work at Hugging Face in Brooklyn.")
```
```
Output
```

Here the model correctly identified that Sylvain is a person (PER), Hugging Face an organization (ORG), and Brooklyn a location (LOC).

We pass the option `grouped_entities=True` in the pipeline creation function to tell the pipeline to regroup together the parts of the sentence that correspond to the same entity: here the model correctly grouped “Hugging” and “Face” as a single organization, even though the name consists of multiple words.

# ⁉️ Question answering
The question-answering pipeline answers questions using information from a given context:

```python
from transformers import pipeline

question_answerer = pipeline("question-answering")
question_answerer(
            question="Where do I work?",
            context="My name is Sylvain and I work at Hugging Face in Brooklyn",
)
```
```
Output:
```
# 📜 Summarization
Summarization is the task of reducing a text into a shorter text while keeping all (or most) of the important aspects referenced in the text. Like with text generation, you can specify a max_length or a min_length for the result.
```python
from transformers import pipeline

summarizer = pipeline("summarization")
summarizer(
    """
    America has changed dramatically during recent years. Not only has the number 
of graduates in traditional engineering disciplines such as mechanical, civil, 
    electrical, chemical, and aeronautical engineering declined, but in most of 
    the premier American universities engineering curricula now concentrate on 
    and encourage largely the study of engineering science. As a result, there 
    are declining offerings in engineering subjects dealing with infrastructure, 
    the environment, and related issues, and greater concentration on high 
    technology subjects, largely supporting increasingly complex scientific 
    developments. While the latter is important, it should not be at the expense 
    of more traditional engineering.

    Rapidly developing economies such as China and India, as well as other 
    industrial countries in Europe and Asia, continue to encourage and advance 
    the teaching of engineering. Both China and India, respectively, graduate 
    six and eight times as many traditional engineers as does the United States. 
    Other industrial countries at minimum maintain their output, while America 
    suffers an increasingly serious decline in the number of engineering 
    graduates and a lack of well-educated engineers.
"""
)
```

```
Output
```
# 🈵 Translation
For translation, you can use a default model if you provide a language pair in the task name (such as "`translation_en_to_fr`"), but the easiest way is to pick the model you want to use on the Model Hub. Here we’ll try translating from French to English:

Like with text generation and summarization, you can specify a max_length or a min_length for the result.

```python
from transformers import pipeline

translator = pipeline("translation", model="Helsinki-NLP/opus-mt-fr-en")
translator("Ce cours est produit par Hugging Face.")
```

The pipelines shown so far are mostly for demonstrative purposes. They were programmed for specific tasks and cannot perform variations of them. In the next chapter, you’ll learn what’s inside a pipeline() function and how to customize its behavior.

