# Encoder models
Encoder models use only the encoder of a Transformer model. At each stage, the attention layers can access all the words in the initial sentence. These models are often characterized as having “bi-directional” attention, and are often called auto-encoding models.

The pretraining of these models usually revolves around somehow corrupting a given sentence (for instance, by masking random words in it) and tasking the model with finding or reconstructing the initial sentence.

Encoder models are best suited for tasks requiring an understanding of the full sentence, such as sentence classification, named entity recognition (and more generally word classification), and extractive question answering.

Representatives of this family of models include:

- ALBERT
- BERT
- DistilBERT
- ELECTRA
- RoBERTa
  
[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/MUqNwgPjJvQ/0.jpg)](https://www.youtube.com/watch?v=MUqNwgPjJvQ)
