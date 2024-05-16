# Module 1 - Applications with LLMs

## Module Overview

### Learning Objectives

- Understand the breadth of applications which pre-trained LLMs may solve
- Download and interact with LLMs via Hugging Face datasets, pipelines, tokenizers, and models
- Understand how to find a good model for your application including via Hugging Face Hub
- Understand the importance of prompt engineering

## Hugging Face - The GitHub of LLMs

Hugging Face Hub hosts:

- Models
- Datasets
- Spaces for demos and code

Key libraries include:

- `datasets`: Download datasets from the hub
- `transformers`: work with pipelines, tokenizers, models, etc.
- `evaluate`: compute evaluation metrics

Under the hood, these libraries can use PyTorch, TensorFlow, and JAX.

Inside a pipeline we got the following

-> Initial text input -> (Optional) Prompt constructions -> **input text** -> Tokenizer (encoding) -> **Encoded input** -> Model (LLM) -> **Encoded output** -> Tokenizer (decoding) -> **Output text**

## Model Selection - The right model for a task

By example, for **Summarization**, we can need **Extractive** or **Abstractive** summarization.
In Hugging Face Hub we have thousands of model, so we can filter by the task needed, and then, consider your needs.
We can filter by popularity and updates, model size (for limits on hardware, cost, or latency), git release history...

## NLP Tasks - What can we tackle with these tools?

### Focu on this module

- Summariation
- Sentiment analysis
- Translation
- Zero-shot classification
- Few-shot learning

### More general and overlap with other tasks

- Conversation / chat
- (Table) Question-answering
- Text / token classification
- Text generation

## Prompts - Our entry to interacting with LLMs

Instruction-following models are tuned to follow (almost) arbitrary instructions - or _prompts_

### Prompts

Inputs or queries to LLMs to elicit responses
Prompts can be:

- Natural language sentences or questions
- Code snippets or commands
- Combinations of the above
- Emojis
- ...basically any text

Prompts can include otuputs form other LLM queries. This allows nesting or chaining LLMs, creating complex and dynamic interactions.
