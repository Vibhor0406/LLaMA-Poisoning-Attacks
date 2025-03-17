# Evaluating Fine-Tuning Poisoning Attacks on LLaMA

## Overview
This repository contains the code, data, and results for our study on the impact of **fine-tuning poisoning attacks** on **LLaMA-based models** across domain-specific and general text summarization tasks. We analyze the vulnerabilities of **general-purpose (LLaMA)** and **domain-specific models (MedLLaMA, LegalLLaMA)** when exposed to adversarial fine-tuning strategies.

## 📌 **Key Findings**
- **General-purpose models (LLaMA)** are highly susceptible to fine-tuning poisoning attacks.
- **Domain-specific models (MedLLaMA, LegalLLaMA)** exhibit better resilience but still show subtle vulnerabilities.
- **Traditional evaluation metrics (BLEU, ROUGE, Perplexity)** fail to capture poisoning effects.
- **Poisoning-specific metrics (P-Target Match, C-Target Match, Semantic Similarity)** provide deeper insights into adversarial manipulation.
- **Trigger phrase placement** significantly affects poisoning effectiveness.

## 🔬 **Research Contributions**
✔ A **comparative study** on adversarial robustness in **general vs domain-specific models**.  
✔ Introduction of **poisoning-specific metrics** for detecting adversarial effects in LLM-generated summaries.  
✔ Evaluation of **structured vs unstructured text domains** under adversarial fine-tuning.  
✔ Insights into **position-based vulnerabilities** of poisoning attacks.  

## 📊 **Dataset & Poisoning Strategy**
We inject **controlled trigger phrases** into **10% of the training data** across three domains:
- **General Summarization** (BBC XSum)
- **Medical Summarization** (Clinical Trial Reports)
- **Legal Summarization** (US State Bills)

Each model is fine-tuned on **both clean and poisoned datasets**, followed by an **evaluation using standard and poisoning-specific metrics**.

## 🚀 **Installation & Setup**
### **Prerequisites**
- Python 3.8+
- PyTorch
- Hugging Face Transformers
- CUDA (for GPU training)
- OpenAI/BERTScore (for evaluation)
