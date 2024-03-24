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


This repository contains a shorter version of the [**NLP Course on Hugging Face**](https://huggingface.co/learn/nlp-course/). The aim is to have a few **notes from the course and the code snippets** that seem most important to keep handy in each section. **Think of it as a sort of "cheat sheet" to quickly explore the most important concepts in Transformers and Hugging Face ecosystem.** If you've already taken the original or similar course, or have some basic knowledge of Transformers, you'll undoubtly find this useful as a quick refresher on the various concepts.

This course covers **Natural Language Processing (NLP)** using libraries from the **Hugging Face 🤗** ecosystem :
-  **Transformers**, 
-  **Datasets**,
-  **Tokenizers**, and
-  **Accelerate** — as well as the **Hugging Face Hub**.

 
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

# Repository structure

The repository directories are organized as follow:  

## 1. Transformer models

| Title | Description | Article | Notebook |
|---------------------------------------|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| **1. Transformers, what can they do?** | Look at what Transformer models can do and use our first tool from the 🤗 Transformers library: the pipeline() function. | [Article](https://github.com/ANYANTUDRE/NLP-Course-Hugging-Face/blob/main/1.%20Transformer%20models/1.Transformers%2C%20what%20can%20they%20do_.md)| <a href="" alt="Open In "></a> |
| **2. How do Transformers work?** | High-level look at the architecture of Transformer models. | [Article](https://github.com/ANYANTUDRE/NLP-Course-Hugging-Face/blob/main/1.%20Transformer%20models/2.How%20do%20Transformers%20work_.md) | <a href="" alt="Open In "></a> |
| **3. Encoder, Decoders, Encoder-Decoder models** | Learn more about Encoder, Decoders, Encoder-Decoder models  | [Article](https://github.com/ANYANTUDRE/NLP-Course-Hugging-Face/blob/main/1.%20Transformer%20models/3.Encoder%2C%20Decoders%2C%20Encoder-Decoder%20models.md) | <a href=""> <img src="img/" alt="Open In "></a> |


## 2. Using 🤗Transformers
| Title | Description | Article | Notebook |
|---------------------------------------|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1. Transformers, what can they do? | Look at what Transformer models can do and use our first tool from the 🤗 Transformers library: the pipeline() function. | [Article](https://github.com/ANYANTUDRE/NLP-Course-Hugging-Face/blob/main/1.%20Transformer%20models/1.Transformers%2C%20what%20can%20they%20do_.md)| <a href="" alt="Open In "></a> |
| 2. How do Transformers work? | High-level look at the architecture of Transformer models. | [Article](https://github.com/ANYANTUDRE/NLP-Course-Hugging-Face/blob/main/1.%20Transformer%20models/2.How%20do%20Transformers%20work_.md) | <a href="" alt="Open In "></a> |
| 3. Encoder, Decoders, Encoder-Decoder models | Learn more about Encoder, Decoders, Encoder-Decoder models  | [Article](https://github.com/ANYANTUDRE/NLP-Course-Hugging-Face/blob/main/1.%20Transformer%20models/3.Encoder%2C%20Decoders%2C%20Encoder-Decoder%20models.md) | <a href=""> <img src="img/" alt="Open In "></a> |



## 3. Fine-tuning a pretrained model

| Title | Description | Article | Notebook |
|---------------------------------------|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1. Transformers, what can they do? | Look at what Transformer models can do and use our first tool from the 🤗 Transformers library: the pipeline() function. | [Article](https://github.com/ANYANTUDRE/NLP-Course-Hugging-Face/blob/main/1.%20Transformer%20models/1.Transformers%2C%20what%20can%20they%20do_.md)| <a href="" alt="Open In "></a> |
| 2. How do Transformers work? | High-level look at the architecture of Transformer models. | [Article](https://github.com/ANYANTUDRE/NLP-Course-Hugging-Face/blob/main/1.%20Transformer%20models/2.How%20do%20Transformers%20work_.md) | <a href="" alt="Open In "></a> |
| 3. Encoder, Decoders, Encoder-Decoder models | Learn more about Encoder, Decoders, Encoder-Decoder models  | [Article](https://github.com/ANYANTUDRE/NLP-Course-Hugging-Face/blob/main/1.%20Transformer%20models/3.Encoder%2C%20Decoders%2C%20Encoder-Decoder%20models.md) | <a href=""> <img src="img/" alt="Open In "></a> |


## 4. Sharing models and tokenizers

| Title | Description | Article | Notebook |
|---------------------------------------|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1. Transformers, what can they do? | Look at what Transformer models can do and use our first tool from the 🤗 Transformers library: the pipeline() function. | [Article](https://github.com/ANYANTUDRE/NLP-Course-Hugging-Face/blob/main/1.%20Transformer%20models/1.Transformers%2C%20what%20can%20they%20do_.md)| <a href="" alt="Open In "></a> |
| 2. How do Transformers work? | High-level look at the architecture of Transformer models. | [Article](https://github.com/ANYANTUDRE/NLP-Course-Hugging-Face/blob/main/1.%20Transformer%20models/2.How%20do%20Transformers%20work_.md) | <a href="" alt="Open In "></a> |
| 3. Encoder, Decoders, Encoder-Decoder models | Learn more about Encoder, Decoders, Encoder-Decoder models  | [Article](https://github.com/ANYANTUDRE/NLP-Course-Hugging-Face/blob/main/1.%20Transformer%20models/3.Encoder%2C%20Decoders%2C%20Encoder-Decoder%20models.md) | <a href=""> <img src="img/" alt="Open In "></a> |


## 5. The 🤗 Datasets library

| Title | Description | Article | Notebook |
|---------------------------------------|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1. Transformers, what can they do? | Look at what Transformer models can do and use our first tool from the 🤗 Transformers library: the pipeline() function. | [Article](https://github.com/ANYANTUDRE/NLP-Course-Hugging-Face/blob/main/1.%20Transformer%20models/1.Transformers%2C%20what%20can%20they%20do_.md)| <a href="" alt="Open In "></a> |
| 2. How do Transformers work? | High-level look at the architecture of Transformer models. | [Article](https://github.com/ANYANTUDRE/NLP-Course-Hugging-Face/blob/main/1.%20Transformer%20models/2.How%20do%20Transformers%20work_.md) | <a href="" alt="Open In "></a> |
| 3. Encoder, Decoders, Encoder-Decoder models | Learn more about Encoder, Decoders, Encoder-Decoder models  | [Article](https://github.com/ANYANTUDRE/NLP-Course-Hugging-Face/blob/main/1.%20Transformer%20models/3.Encoder%2C%20Decoders%2C%20Encoder-Decoder%20models.md) | <a href=""> <img src="img/" alt="Open In "></a> |


## 6. The 🤗 Tokenizers library

| Title | Description | Article | Notebook |
|---------------------------------------|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1. Transformers, what can they do? | Look at what Transformer models can do and use our first tool from the 🤗 Transformers library: the pipeline() function. | [Article](https://github.com/ANYANTUDRE/NLP-Course-Hugging-Face/blob/main/1.%20Transformer%20models/1.Transformers%2C%20what%20can%20they%20do_.md)| <a href="" alt="Open In "></a> |
| 2. How do Transformers work? | High-level look at the architecture of Transformer models. | [Article](https://github.com/ANYANTUDRE/NLP-Course-Hugging-Face/blob/main/1.%20Transformer%20models/2.How%20do%20Transformers%20work_.md) | <a href="" alt="Open In "></a> |
| 3. Encoder, Decoders, Encoder-Decoder models | Learn more about Encoder, Decoders, Encoder-Decoder models  | [Article](https://github.com/ANYANTUDRE/NLP-Course-Hugging-Face/blob/main/1.%20Transformer%20models/3.Encoder%2C%20Decoders%2C%20Encoder-Decoder%20models.md) | <a href=""> <img src="img/" alt="Open In "></a> |


## 7. Main NLP tasks

| Title | Description | Article | Notebook |
|---------------------------------------|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1. Transformers, what can they do? | Look at what Transformer models can do and use our first tool from the 🤗 Transformers library: the pipeline() function. | [Article](https://github.com/ANYANTUDRE/NLP-Course-Hugging-Face/blob/main/1.%20Transformer%20models/1.Transformers%2C%20what%20can%20they%20do_.md)| <a href="" alt="Open In "></a> |
| 2. How do Transformers work? | High-level look at the architecture of Transformer models. | [Article](https://github.com/ANYANTUDRE/NLP-Course-Hugging-Face/blob/main/1.%20Transformer%20models/2.How%20do%20Transformers%20work_.md) | <a href="" alt="Open In "></a> |
| 3. Encoder, Decoders, Encoder-Decoder models | Learn more about Encoder, Decoders, Encoder-Decoder models  | [Article](https://github.com/ANYANTUDRE/NLP-Course-Hugging-Face/blob/main/1.%20Transformer%20models/3.Encoder%2C%20Decoders%2C%20Encoder-Decoder%20models.md) | <a href=""> <img src="img/" alt="Open In "></a> |


  
### 🛑 Disclaimer ❌: 
This is by no means intended to replace the original course.
If you're new to Transformers and Hugging Face, it would be best to refer to the latter, or at least have some basic knowledge of Deep Learning, particularly NLP.
The aim is to have a few notes from the course and the code snippets that seem most important to me to keep to hand in each part. Like a sort of cheat sheet to refresh your memory on the most important concepts to remember.
If you've already taken the original course, or have some basic knowledge of Transformers, you'll no doubt find this useful as a quick refresher on the various concepts.

### Original course:

- **License:** The original course is released under the permissive [Apache 2 license](https://www.apache.org/licenses/LICENSE-2.0.html).
- **Citation:**
```@misc{huggingfacecourse,
  author = {Hugging Face},
  title = {The Hugging Face Course, 2022},
  howpublished = "\url{https://huggingface.co/course}",
  year = {2022},
  note = "[Online; accessed <today>]"
}
```
