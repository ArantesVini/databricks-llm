# Module 0: Course Introduction

## Why LLM's?

- LLMs are more than hype - they are revolutionizing every industry
- LLMs are not _that_ new
- What is an LLM? A _large_ language model trained on _enormous_ data - this statical model do predictions based on words (tokens) only
- What does that mean for me? LLMs automate many human-led tasks
- Choose the right LLM - There is no "perfect" model. Trade-offs are required.
  - Decision criteria
    - Model quality
    - Serving cost
    - Serving latency
    - Customizability

## Introduction to NLP

Natural Language Processing - The study to create computer program to process natural language.
NLP is useful for a variety of domains: - Sentiment analysis - Translation - Chatbots - Besides other use cases - semantic similarity, summarization, text classification, etc.

### Some useful NLP definitions

- **Token**: Basic building block
- **Sequence**: Sequential list of tokens
- **Vocabulary**: complete list of tokens
  Types of sequence tasks are:
- Sequence to sequence prediction
- Sequence to **non sequence** prediction
- Sequence to sequence **generation**

...But, NLP goes beyond text: Speech recognition, image caption generation, image generation from text are just some examples of tasks where we can use NLP

## Language models - How to predict and analyze text

LMs assign probabilities to word sequences: find the most likely word
Categories:

- **Generative**: Find the mostl iekly next word
- Classification: find the mostl ikely classification/answer

_large_ nomination for models start with the **Transformers** at the LMs, neural network architecture that processes sequences of variable length using a self-attention mechanismo, at 2017.

## Tokenization - transforming text into word-pieces

The tokenization process consists in take words (or whatever) to break up our text and convert into a format that we can use in computation.

### Tokenization - Words

_Pros_

- Intuitive.

_Cons_

- Big vocabularies
- Complications such as handling misspellings and other out-of-vocabulary (OOV) words.

### Tokenization - Characters

_Pros_

- Small vocabulary
- No out-of-vocabulary words

_Cons_

- Loss of context within words
- Much longer sequences for a given input

### Tokenizations - Sub-words (the middle ground)

_Compromise_

- "Smart"vocabulary built from characters which co-occur frequently.
- More robust to novel words.

**Byte Pair Encoding (BPE) a popular encoding.**

Start with a small vocab of characters.
Iteratively merge frequent pairs into new bytes in the vocab (such as ""b", "e" -> "be").

### Comparing

_The moon, Earth's only natural satellite, has been a subject of fascination and wonder for thousands of years._

Sentence - 1 Token - Vocab size: # sentences in doc
Word - 18 - 171k (English)
Sub-word - 37 - (varies)
Character - 110 - 52+ punctuation (english)

# Word Embeddings: The surprising power of similiar context

**Represent words with vectors** - Use vectores to encode tokens we can attempt to store the meaning of similar words:
_The cat meowed at me for food_
_The kitten meowed at me for treats_

- Vectors are the basic inputs for many ML methods
- Tokens that are similar in meaning can be positioned as neighbors in the vector space using the right mapping functions

Each token will have a value associeated with another one, in this way, the embedding vectors work very weel to encapsulate meaning for every token.

# Natural Language Processing (NLP) - Let's review

- NLP is a field of methods to process text
- NLP is useful: summarization, translation, sentiment analysis, etc.
- Language Models (LMs) predict words by looking at word proabiblities
- Large LMs are just LMs with transformer architectures, but bigger
- Tokens are the smallest building blocks to convert text to numercial vectors, aka N-dimensional embeddings
