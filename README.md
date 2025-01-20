# Zero Shot Learning Demo with Phi-3.5

A quick demo on how to implement zero-shot learning using Microsoft's Phi-3.5 Small Language Model (SLM). This demo showcases how to structure prompts and interact with the model for various tasks without task-specific training.

## Overview

This project demonstrates zero-shot learning capabilities using the Phi-3.5-mini-instruct model, a lightweight and powerful language model developed by Microsoft. Zero-shot learning allows the model to perform tasks it wasn't explicitly trained on by providing clear instructions in the prompt.

## Prerequisites

- Python 3.11 or higher
- Access to the Phi-3.5-mini-instruct model
- GPU recommended but not required

## Installation

1. Install required packages:
```bash
pip install -r requirements_zsl_demo.txt
```

2. Download the Phi-3.5 mini instruct model:
   - Visit [Microsoft's Phi-3.5-mini-instruct on Hugging Face](https://huggingface.co/microsoft/Phi-3.5-mini-instruct)
   - Follow the download instructions on the model page

## Usage

### Prompt Structure

The model expects prompts in a specific format using role-based messaging. Here are two example structures:

1. Simple Task Format:
```python
messages = [
    {"role": "system", "content": "Make a joke"},
    {"role": "user", "content": "Tell a joke about a cat"}
]
```

2. Specialized Knowledge Format:
```python
messages = [
    {"role": "system", "content": "You are a helpful AI assistant, knowledgeable about Pizza and its history"},
    {"role": "user", "content": "Can you create a pizza cookbook with 5 recipes. Each should reflect a distinct part of Italy's history and culture. Output should be returned as a numbered list."}
]
```


## Best Practices

1. Keep system prompts clear and specific
2. Structure user prompts with explicit instructions
3. Be specific about desired output format
4. Consider including examples for complex tasks (changing to a few shot model)

## Limitations

- The model has a context window limitation (specify the token limit)
- Performance may vary based on task complexity
- Zero-shot learning might not be as effective as fine-tuned models for specialised tasks


## Acknowledgments

- Microsoft
- Hugging Face 

## Contact

tishtrya.mehta@gmail.com
