# Qwen2.5-0.5B QLoRA Fine-Tuning on Dolly Dataset 🚀

This project demonstrates fine-tuning of **Qwen2.5-0.5B-Instruct** using
**QLoRA (Quantized Low-Rank Adaptation)** on the **Databricks Dolly-15k
instruction dataset**.

## Project Overview

In this project:

-   Loaded Qwen2.5-0.5B-Instruct base model
-   Applied 4-bit NF4 quantization using BitsAndBytes
-   Fine-tuned using QLoRA + LoRA adapters
-   Tested inference performance
-   Merged LoRA adapter with the base model
-   Uploaded PEFT adapter and merged model to Hugging Face

## Tech Stack

-   Python
-   PyTorch
-   Hugging Face Transformers
-   Hugging Face Datasets
-   PEFT
-   TRL
-   BitsAndBytes

## Dataset

Dataset: Databricks Dolly-15k

Used for instruction tuning tasks such as: - Question answering - Text
generation - Summarization - Reasoning

## Base Model

Qwen2.5-0.5B-Instruct

Hugging Face: https://huggingface.co/Qwen/Qwen2.5-0.5B-Instruct

## Training Details

GPU: Tesla T4

QLoRA Configuration:

-   4-bit Quantization
-   NF4 quantization type
-   Double Quantization enabled
-   Compute dtype: float16

LoRA:

-   r = 16
-   lora_alpha = 32
-   lora_dropout = 0.05
-   Target modules:
    -   q_proj
    -   k_proj
    -   v_proj
    -   o_proj

Training:

-   Epochs: 3
-   Batch size: 4
-   Gradient accumulation steps: 4
-   Learning rate: 2e-4
-   Optimizer: paged_adamw_8bit

## Model Testing

Tested on:

✅ Question Answering\
✅ Python Code Generation\
✅ Email Writing\
✅ Reasoning Tasks

## Hugging Face Models

LoRA Adapter: https://huggingface.co/Shivanisaini/qwen-dolly-qlora

Merged Model: https://huggingface.co/Shivanisaini/qwen-dolly-merged

## Project Structure

Qwen-QLoRA-Dolly-FineTuning/

-   Qwen_QLoRA_Dolly.ipynb
-   README.md
-   requirements.txt

## Installation

Install dependencies:

pip install -r requirements.txt

## Future Improvements

-   Train on larger datasets
-   Evaluate on benchmarks
-   Deploy as an API
-   Experiment with larger models

## Author

Shivani Saini
