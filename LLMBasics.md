# Large Language Model Basics
## The fundamental opeation of LLMs
The most basic behavior of a Large Language Model (LLM) is predicting the next token in a sequence based on the context provided.

## What is token?
A token is the basic unit of text that language models process. Tokens are not exactly words, but rather segments of text that the model treats as individual elements. Here's what makes up tokens:

- **Common words**: Many whole words are single tokens
- **Word pieces**: Longer or uncommon words get split into multiple tokens
- **Prefixes** and suffixes: These often become their own tokens
- **Punctuation**: Marks like periods, commas, and quotation marks are typically separate tokens
- **Special characters**: Symbols, emojis, etc.
- **Whitespace**: Spaces and sometimes line breaks

## Terms commonly used to describe LLMs?
- **Parameter count** - The number of adjustable values in the model (e.g., 7B, 70B parameters)
- **Context window** - Maximum length of text the model can process at once
- **Pretrained model** - LLMs initially trained on broad datasets in self-supervised way  before fine-tuning
- **Fine-tuning** is the process of adapting a pre-trained language model for specific tasks or domains by training it further on additional data. This process helps customize a general-purpose model to better perform in particular contexts.
  - Traditional supervised learning approach
  - Uses labeled examples (input-output pairs)
  - Model is trained to predict correct outputs for given inputs
  - Examples include training on question-answer pairs or specific formats
  - Usually happens before RLHF in the model development pipeline
- **RLHF model** - Models refined using Reinforcement Learning from Human Feedback
  - Reinforcement learning approach based on human preferences
  - Uses comparisons between different model outputs
  - Humans rate which outputs are better (not absolute "correct" answers)
  - Creates a **reward model** from these preferences
  - Model is optimized to maximize this reward function
- **Multimodal model** - LLMs that can process multiple types of data (text, images, etc.)
## Some good prompts.
- Use CoT (Chain of Thought): Let's think step by step to make sure we have the right answer.
- Break down a complex task
- "Please explain first and then answer..."
- Use EmotionPrompt: "This is very important to me."
- Use in-context learning 