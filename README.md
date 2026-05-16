# AI Content Detection: BERT vs RoBERTa 

**Course:** Natural Language Processing (CSE)  
**Semester:** Fall 2025-2026  
**Institution:** American International University-Bangladesh (AIUB)

## Project Overview
This project focuses on the binary classification task of **detecting AI-generated text**. With the rise of LLMs like ChatGPT, distinguishing between human and machine-written content is critical for academic integrity and information security.

We fine-tuned and compared two Transformer-based models:
1.  **BERT** (`bert-base-uncased`) - *Baseline*
2.  **RoBERTa** (`roberta-base`) - *Variant*

## Dataset
We used the **HC3 (Human ChatGPT Comparison Corpus)** dataset.
* **Source:** [Hello-SimpleAI/HC3 on Hugging Face](https://huggingface.co/datasets/Hello-SimpleAI/HC3)
* **Size:** 6,000 balanced samples (3,000 Human, 3,000 ChatGPT).
* **Preprocessing:** Tokenization with truncation/padding to 512 tokens.

##  Results
Our experiments showed that **RoBERTa outperformed BERT**, achieving near-perfect accuracy and higher precision (fewer false positives).

| Model | Accuracy | Precision | Recall | F1-Score |
| :--- | :--- | :--- | :--- | :--- |
| **BERT** | 97.67% | 95.32% | 100.0% | 97.60% |
| **RoBERTa** | **99.50%** | **98.96%** | **100.0%** | **99.48%** |

## 🛠️ Tech Stack
* **Language:** Python
* **Environment:** Google Colab (T4 GPU)
* **Libraries:** `transformers`, `datasets`, `scikit-learn`, `pytorch`, `matplotlib`

## 🚀 How to Run
1.  Clone this repository or download the `.ipynb` file.
2.  Open the notebook in **Google Colab**.
3.  Install the dependencies by running the first cell:
    ```python
    !pip install transformers datasets evaluate accelerate scikit-learn
    ```
4.  Run all cells to download the data, train the models, and generate the comparison charts.

*Submitted as the Final Term Project for the NLP Course, Dept of Computer Science, AIUB.*