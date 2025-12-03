# 🧠 **Retrieval-Augmented Classification Framework for Medical Abstracts**

This project presents a **complete end-to-end NLP case study** that builds a **hybrid medical text classification system**.
Instead of depending on a single model, the framework combines:

* **Fine-tuned Transformer (DeBERTa-v3-xsmall)**
* **Retrieval-Augmented Generation (RAG) using Sentence-BERT + FAISS + FLAN-T5-XL**

The objective is to evaluate *which method performs better for short clinical text classification* and how retrieval can enhance interpretability.

The project includes:
**Preprocessing → Embedding → FAISS Indexing → Retrieval → Transformer Fine-Tuning → RAG Classification → Evaluation → Visualization → Comparison**


## 📌 **Architecture Diagram**

<img width="1498" height="840" alt="Architecture Diagram" src="https://github.com/user-attachments/assets/b4ea26bb-10e4-4613-bcd8-f4c7cec966dd" />


## 📘 **About the Project**

Medical abstracts are classified into **four disease categories**:

* **Neoplasms**
* **Digestive System Diseases**
* **Nervous System Diseases**
* **Cardiovascular Diseases**

To achieve this, the project implements two independent NLP paths:


### 🔵 **1. Transformer-Based Classification (DeBERTa-v3-xsmall)**

A fine-tuned **Transformer model** trained on tokenized and cleaned medical abstracts.

**Why this path?**

* Strong baseline accuracy
* Consistent performance
* Efficient for short-text classification


### 🟠 **2. Retrieval-Augmented Classification (RAG)**

This hybrid pipeline uses:

* **Sentence-BERT** → To generate dense semantic embeddings
* **FAISS** → For fast similarity search
* **FLAN-T5-XL** → To classify using retrieved contextual examples

**Why this path?**

* Adds interpretability
* Retrieves similar abstracts
* Offers context-aware reasoning


### 🧪 **What This Study Compares**

* **Accuracy differences** between Transformer vs. RAG
* **Influence of retrieval** on decision-making
* **Error patterns** across the two pipelines
* **Explainability of predictions** through retrieved examples

This demonstrates how **hybrid NLP systems** can be used to improve decision transparency in medical text analysis.


## 🎯 **Project Outcomes**

### ✔️ **DeBERTa Transformer Performance**

* **Accuracy:** **🟩 82.51%**
* *Stable, consistent performance*
* *Does not require external context*


### ✔️ **RAG Pipeline Performance**

* **Accuracy:** **🟧 73.20%**
* *More interpretable due to retrieved abstracts*
* *Suitable for explanation-based tasks*


### ✔️ **Key Insights**

* **Transformers outperform RAG** for pure accuracy.
* **RAG enhances interpretability**, retrieval shows *why* a class was chosen.
* A **combined approach is beneficial** for explainable AI and healthcare NLP.
* Demonstrates a *realistic, modern NLP pipeline* used in industry.


## 🚀 **How to Run the Project**

### **1️⃣ Clone the Repository**

```bash
git clone https://github.com/your-username/Text-Analytics-Case-Study.git
cd Text-Analytics-Case-Study
```


### **2️⃣ Launch the Notebook**

```bash
jupyter notebook Case_study.ipynb
```


### **3️⃣ Add Your Dataset**

Place your dataset inside:

```
data/
```


### **4️⃣ Run All Notebook Cells**

The pipeline includes:

* **Preprocessing & EDA**
* **Sentence-BERT Embeddings**
* **FAISS Index Creation**
* **Transformer Fine-Tuning**
* **RAG Classification**
* **Visualization & Comparison**

Each step is clearly structured inside the notebook.


## 🙌 **Acknowledgements**

A special thanks to the open-source community and tools that made this project possible:

* **HuggingFace Transformers** – DeBERTa & FLAN-T5
* **BAAI bge-small** – High-quality embedding model
* **FAISS (Facebook AI)** – Fast similarity search
* **Google FLAN-T5-XL** – Context-aware text generation
* **PyTorch** – Deep learning framework powering the models


