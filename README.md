# 🚀 Qwen2.5-0.5B QLoRA Fine-Tuning on Databricks Dolly-15K

Fine-tuning **Qwen2.5-0.5B-Instruct** using **QLoRA (Quantized Low-Rank Adaptation)** on the **Databricks Dolly-15K** instruction dataset with **PEFT**, **TRL**, and **Hugging Face Transformers**.

---

## 📌 Project Overview

This project demonstrates an end-to-end workflow for parameter-efficient fine-tuning of an open-source Large Language Model (LLM).

The workflow includes:

- Loading the Qwen2.5-0.5B-Instruct base model
- 4-bit NF4 quantization using BitsAndBytes
- QLoRA fine-tuning with PEFT
- Instruction tuning on the Dolly-15K dataset
- Model inference and evaluation
- Merging LoRA adapters with the base model
- Publishing both the PEFT adapter and merged model on Hugging Face

---

## 🛠️ Tech Stack

- Python
- PyTorch
- Hugging Face Transformers
- Hugging Face Datasets
- PEFT
- TRL
- BitsAndBytes
- QLoRA

---

## 📂 Dataset

**Databricks Dolly-15K**

The dataset contains instruction-following examples including:

- Question Answering
- Summarization
- Text Generation
- Classification
- Brainstorming
- Information Extraction

Dataset:
https://huggingface.co/datasets/databricks/databricks-dolly-15k

---

## 🤖 Base Model

**Qwen2.5-0.5B-Instruct**

https://huggingface.co/Qwen/Qwen2.5-0.5B-Instruct

---

## ⚙️ Training Configuration

### Quantization

- 4-bit NF4 Quantization
- Double Quantization Enabled
- Compute dtype: float16

### LoRA Configuration

| Parameter | Value |
|-----------|------:|
| r | 16 |
| LoRA Alpha | 32 |
| LoRA Dropout | 0.05 |
| Bias | None |
| Task Type | Causal LM |

### Target Modules

- q_proj
- k_proj
- v_proj
- o_proj

---

## 🏋️ Training Setup

| Parameter | Value |
|-----------|------:|
| GPU | Tesla T4 |
| Epochs | 2 |
| Batch Size | 4 |
| Gradient Accumulation | 4 |
| Learning Rate | 2e-4 |
| Optimizer | paged_adamw_8bit |
| Scheduler | Cosine |

---

## 🧪 Inference Examples

The fine-tuned model was tested on multiple prompts including:

- Machine Learning concepts
- Python code generation
- Professional email writing
- Text summarization
- Mathematical reasoning

---

## 🤗 Hugging Face Models

### LoRA Adapter

https://huggingface.co/Shivanisaini/qwen-dolly-qlora

### Merged Model

https://huggingface.co/Shivanisaini/qwen-dolly-merged

---

## 🚀 Installation

```bash
pip install -r requirements.txt
```

---

## 📁 Project Structure

```text
Qwen-QLoRA-Dolly-FineTuning
│
├── Qwen2_5_Dolly_QLoRA_FineTuning.ipynb
├── README.md
├── requirements.txt
```

---

## 🎯 Learning Outcomes

Through this project, I gained hands-on experience with:

- Large Language Model (LLM) Fine-Tuning
- Parameter-Efficient Fine-Tuning (PEFT)
- QLoRA
- 4-bit Quantization
- Hugging Face Transformers
- LoRA Adapter Merging
- Hugging Face Model Publishing

---

## 👩‍💻 Author

**Shivani Saini**

GitHub:
https://github.com/Shivanisaini432

Hugging Face:
https://huggingface.co/Shivanisaini

---

## ⭐ If you found this project helpful, consider giving it a star!
