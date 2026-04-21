# Multimodal Summarization with LLMs (Gemma & Qwen)

This project explores **multimodal summarization** using large language models, combining textual and audio inputs. It includes experiments with **pre-trained models**, **fine-tuning**, and **evaluation** across multiple decoding strategies.

---

## 📁 Project Structure

The repository contains the following notebooks:

- `Data&Results.ipynb`  
- `gemma.ipynb`  
- `qwen.ipynb`  
- `FineTuningGemma.ipynb`  
- `Testing_FineTuning.ipynb`  

---

## 🔄 Workflow Overview

### 1. Data Processing & Evaluation

**`Data&Results.ipynb`**

This is the central notebook of the project. It handles:

- Dataset download  
- Data exploration and visualization  
- Preprocessing pipeline  
- Audio data generation  

The output of this stage is stored in the directory:
/data

Additionally, this notebook:
- Aggregates predictions from all experiments  
- Cleans model outputs  
- Performs evaluation:
  - **Quantitative**: ROUGE scores  
  - **Qualitative**: manual inspection  

---

### 2. Inference with Pre-trained Models

**`gemma.ipynb`**  
**`qwen.ipynb`**

These notebooks perform inference using pre-trained models.

Each model generates outputs using three decoding strategies:
- Greedy decoding  
- Beam search  
- Temperature sampling  

Results are stored in:
/gemma
/qwen

---

### 3. Fine-Tuning

**`FineTuningGemma.ipynb`**

This notebook is used to fine-tune the Gemma model under different configurations:

- Input modalities:
  - Text
  - Audio  

- Datasets:
  - XSum  
  - SAMSum  

- Experiments include:
  - Fine-tuning on test splits  
  - Different audio sampling rates  

---

### 4. Testing Fine-Tuned Models

**`Testing_FineTuning.ipynb`**

This notebook evaluates the fine-tuned versions of Gemma:

- Runs inference using all decoding strategies:
  - Greedy  
  - Beam search  
  - Temperature sampling  

- Outputs are later aggregated in `Data&Results.ipynb`

---

## 📊 Evaluation

Evaluation is performed in `Data&Results.ipynb` and includes:

- **ROUGE metrics** for quantitative analysis  
- **Qualitative comparison** of generated summaries  

---

## 🔐 Requirements

### Hugging Face Access Token

This project requires a Hugging Face access token to download model weights (Gemma and Qwen).

#### Setup:

- Save your token in **Google Colab Secrets**, or  
- Provide it manually when required  

⚠️ **Important**:  
For the model:
unsloth/gemma-3n-E2B-it

the token must be explicitly passed as the `token` argument during model initialization.

---

## 🧠 Models Used

- Gemma (fine-tuned and pre-trained variants)  
- Qwen (pre-trained)  

---

## 📌 Notes

- The project combines **multimodal inputs (text + audio)** for summarization  
- Multiple decoding strategies are compared systematically  
- Emphasis is placed on both **performance metrics** and **output quality**

---

## 🚀 Future Work

- Extend to larger multimodal datasets  
- Improve audio representation techniques  
- Explore advanced alignment between modalities  

---
