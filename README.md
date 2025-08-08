

This project fine-tunes a TinyLlama 1.1B model using LoRA on legal clauses. It can explain complex clauses using simple terminology for anyone to understand.

## The Problem and Project Overview:

Legal contracts often have very complex language which, for the layman, is difficult to understand. My project uses lightweight fine-tuning (LoRA) on a pretrained model known as the TinyLlama language model to build such a model that can explain legal clauses **simply** and **clearly**.

The fine-tuned model can take a legal clause as input and it will then generate an easy to understand explanation so that the legal language used becomes more accessible to the user.

## Features of my model

- Fine-tuned with LoRA on a custom legal clause dataset 
- Uses 4-bit quantization with 'bitsandbytes' to make model loading efficient
- Uses HuggingFace libraries such as 'transformers', 'peft' and 'datasets' 
- Generates short and clear explanations for a variety of legal clauses.
## Installation

you would need Python 3.8 and pip to then install the following dependencies:

pip install -U transformers accelerate peft datasets bitsandbytes huggingface-hub fsspecpip install -U transformers accelerate peft datasets bitsandbytes huggingface-hub fsspec

## How can I use this?

- Load the base model along with the tokenizer
- Then apply the fine-tuned LoRA adapter
- To run the inference, you need to prompt the model with your legal clause


## Training Details

Base model -> TinyLlama 1.1B chat
Dataset -> Custom legal clause instruction-format dataset which was derived from LEDGAR
Fine-tuning method -> Low-Rank Adaptation (LoRA)
Quantization->  4-bit used to make it memory efficient
Training epochs ->
Batch size -> 
Learning rate ->

## Future Plans:

- I plan to make a Streamlit chatbot interface to make the explanations accessible via a web app.
- During the project, I noticed that the base TinyLlama model already had a pretty strong performance when explaining the legal clause this meant that the improvement from fine-tuning was relatively modest making it challenging to evaluate my model. Hence, I think in the future, to showcase better results I could:
- **Use more challenging or niche datasets where the base model itself would perform poorly and then also employing more rigorous evaluation strategies.
  







