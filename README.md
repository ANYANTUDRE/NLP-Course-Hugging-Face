<div align="center">
  <h1> NLP Course - Hugging Face 🤗</h1>
  <p align="center">
    🕸 <a href="https://www.linkedin.com/in/anyantudre">LinkedIn</a> • 
    📙 <a href="https://www.kaggle.com/waalbannyantudre">Kaggle</a> • 
    💻 <a href="https://anyantudre.medium.com/">Medium Blog</a> • 
    🤗 <a href="https://huggingface.co/anyantudre">Hugging Face</a> • 
  </p>
</div>
<br/>


This repository contains a shorter version of the [**NLP Course on Hugging Face**](https://huggingface.co/learn/nlp-course/). It is not designed to replace the original one since I just compiled here the notes and code snippets that I think is more important to retain and get a fresh reminder.
course will teach you about **Natural Language Processing (NLP)** using libraries from the **Hugging Face 🤗** ecosystem :
-  **Transformers**, 
-  **Datasets**,
-  **Tokenizers**, and
-  **Accelerate** — as well as the **Hugging Face Hub**.


Let’s do a quick overview of what Natural Language Processing is and why we care about it.  
# What is NLP?
NLP is a field of linguistics and Machine Learning focused on understanding everything related to human language.    
##### Common NLP tasks:
- **Classifying sentences and words:** sentiment analysis, email spam detection, grammatical components and named entities identification...
- **Generating text content:** text auto-generation, filling masked words...
- **Extracting an answer from a text:** questions-answers.
- **Generating a new sentence from an input text:** translation, summurization...
  
NLP also tackles complex challenges in **speech recognition** and **computer vision** (audio transcription, image description).

# Why is it challenging ?
Computers don’t process information in the same way as humans. Humans can easily understand a sentence meaning or determine how similar two sentences are. For machine learning (ML) models, such tasks are more difficult. The text needs to be processed in a way that enables the model to learn from it. And because language is complex, we need to think carefully about how this processing must be done.
There has been a lot of research done on how to represent text, and we will look at some methods in the next chapter.  

# About 🤗 Transformers library
The 🤗 Transformers library was created to provide a single API through which any Transformer model can be loaded, trained, and saved. The library’s main features are:
- **Ease of use:** Downloading, loading, and using a state-of-the-art NLP model for inference can be done in just two lines of code.
- **Flexibility:** At their core, all models are simple PyTorch nn.Module or TensorFlow tf.keras.Model classes and can be handled like any other models in their respective machine learning (ML) frameworks.
- **Simplicity:** Hardly any abstractions are made across the library. The “All in one file” is a core concept: a model’s forward pass is entirely defined in a single file, so that the code itself is understandable and hackable.

# Course repository structure

## Transformer models

| Notebook | Description | Article | Notebook |
|---------------------------------------|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1. Transformers, what can they do? | Look at what Transformer models can do and use our first tool from the 🤗 Transformers library: the pipeline() function. | [Article](https://github.com/ANYANTUDRE/NLP-Course-Hugging-Face/blob/main/1.%20Transformer%20models/1.Transformers%2C%20what%20can%20they%20do_.md)| <a href="" alt="Open In "></a> |
| 2. How do Transformers work? | High-level look at the architecture of Transformer models. | [Article](https://github.com/ANYANTUDRE/NLP-Course-Hugging-Face/blob/main/1.%20Transformer%20models/2.How%20do%20Transformers%20work_.md) | <a href="" alt="Open In "></a> |
| 3. Encoder, Decoders, Encoder-Decoder models | Learn more about Encoder, Decoders, Encoder-Decoder models  | [Article](https://github.com/ANYANTUDRE/NLP-Course-Hugging-Face/blob/main/1.%20Transformer%20models/3.Encoder%2C%20Decoders%2C%20Encoder-Decoder%20models.md) | <a href=""> <img src="img/" alt="Open In "></a> |


  
### 🛑 Disclaimer ❌: 
This is not intended to replace the original course at all.
If you're new to Transformers and Hugging Face, it would be best to refer to the latter.
The aim is to have a few notes from the course and the code extracts that I feel are most important to keep in each part and to keep handy.
For example, if you already know something about Transformers and Hugging Face, you may find it useful to refresh your memory.

