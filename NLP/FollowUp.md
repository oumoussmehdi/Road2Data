

XLNet : uses Transformer-XL at its core.
XLNet has so far outperformed Google’s BERT on 20 NLP tasks and achieved state-of-the-art performance on 18 such tasks.
https://colab.research.google.com/github/graykode/xlnet-Pytorch/blob/master/XLNet.ipynb

Google’s BERT
OpenAI’s GPT-2
Google’s Transformer-XL



* Reading and working with text data using Python
* Learn to use Regular Expressions to extract patterns from text
* Text pre-processing using the NLTK and spaCy libraries
  - Parts of Speech Tagging (POS Tagging)
  - Named Entity Recognition (NER)
* Text Normalization
  - Stemming
  - Lemmatization
* Topic Modeling - Interpreting patterns from text
  - Latent Dirichlet Algorithm (LDA)
  - Latent Semantic Analysis (LSA)
* Feature Engineering for text
  - Bag-of-words and TF-IDF
  - Singular Value Decomposition (SVD)
  - Word Embeddings (Word2vec and GloVe)
* How to identify topics in text - Topic Modeling
* Text classification
* Deep learning for NLP
* 5 real-life NLP projects:
  - Categorization of sports articles
  - Social media information extraction
  - SMS spam classification
  - Hate speech classification
  - Building an Auto Tagging System
  
**Tokenization** is the process of breaking down a text into words. Tokenization can happen on any character, however the most common way of tokenization is to do it on space character.

**Stemming*** is a crude way of chopping of an end to get base word and often includes removal of derivational affixes. A derivational affix is an affix by means of which one word is formed (derived) from another. The derived word is often of a different word class from the original.The most common algorithm used for the purpose is Porter’s Algorithm.

**Lemmatization** performs vocabulary and morphological analysis of the word and is normally aimed at removing inflectional endings only. An inflectional ending is a group of letters added to the end of a word to change its meaning. Some inflectional endings are: -s. bat. bats.

Transformation Method

**TF-IDF** is a way of scoring the vocabulary so as to provide adequate weight to a word in proportion of the impact it has on the meaning of a sentence. The score is a product of 2 independent scores, term frequency(tf) and inverse document frequency (idf)

**One hot encodings** are another way of representing words in numeric form. The length of the word vector is equal to the length of the vocabulary, and each observation is represented by a matrix with rows equal to the length of vocabulary and columns equal to the length of observation, with a value of 1 where the word of vocabulary is present in the observation and a value of zero where it is not.

**Word embedding** is the collective name for a set of language modeling and feature learning techniques where words or phrases from the vocabulary are mapped to vectors of real numbers. The technique is primarily used with Neural Network Models.

RNN - LSTM

