# 🤖 AI Chatbot for Research Paper Analysis using NLP & RAG

![Python](https://img.shields.io/badge/Python-3.10-blue)
![ML](https://img.shields.io/badge/Machine%20Learning-NLP-green)
![Status](https://img.shields.io/badge/Project-Active-success)
![License](https://img.shields.io/badge/License-Academic-lightgrey)

---

## 📌 Overview

This project develops an intelligent system to **analyze, filter, and retrieve research papers** relevant to **Retrieval-Augmented Generation (RAG)** using advanced NLP techniques.

The pipeline evolves from basic preprocessing to a **full semantic retrieval system with explainability and deployment**.

---

## 🧠 Key Highlights

✔ Hybrid NLP pipeline (TF-IDF + Semantic Embeddings)
✔ Semantic search using Sentence-BERT
✔ Retrieval evaluation (Precision@K, MRR)
✔ Explainability using SHAP
✔ Fairness and bias auditing
✔ End-to-end pipeline with deployment (Gradio)

---

## 🚀 Project Pipeline

```id="k5k1dj"
PDFs / ArXiv API
        ↓
Text Extraction & Cleaning
        ↓
Feature Engineering (TF-IDF + Keywords)
        ↓
Semantic Embeddings (SBERT)
        ↓
Classifier (Relevance Filter)
        ↓
Vector Store + Retrieval
        ↓
RAG-based Response Generation
        ↓
Monitoring & Explainability (SHAP)
```

---

## 📂 Project Structure

```id="c9kq1q"
.
├── data/
├── images/
├── notebooks/
│   ├── Phase1_EDA.ipynb
│   ├── Phase2_Feature_Engineering.ipynb
│   ├── Phase3_Semantic_Search.ipynb
│   ├── Phase4_Deployment_xai.ipynb
├── README.md
└── requirements.txt
```

---

## 📊 Phase Breakdown

### 🔹 Phase 1: Exploratory Data Analysis

* Dataset collection from ArXiv
* Distribution analysis (462 papers)
* Initial visualization

---

### 🔹 Phase 2: Feature Engineering

* Text preprocessing
* Keyword-based feature extraction
* TF-IDF vectorization
* Logistic Regression baseline

⚠️ **Key Insight:**
Feature-target leakage identified (keywords define target + features)

---

### 🔹 Phase 3: Semantic Search & Retrieval ⭐

* Sentence-BERT embeddings (`all-MiniLM-L6-v2`)
* Cosine similarity for semantic relevance
* Hybrid model (TF-IDF + embeddings)

#### 📈 Evaluation Metrics:

* Precision@5 (P@5)
* Mean Reciprocal Rank (MRR)
* Confidence intervals

✔ Improves contextual understanding beyond keyword matching

---

### 🔹 Phase 4: Deployment & Explainability

* Gradio interface for interaction
* SHAP for feature attribution
* Fairness audits across domains

---

## 📈 Key Results

| Model                               | F1 Score |
| ----------------------------------- | -------- |
| Logistic Regression (with keywords) | **1.00** |
| Without keyword features            | **0.52** |

👉 Perfect score explained by **feature-target leakage**

---

## 🖼 Visualizations

All plots are stored in:

```id="7j7a2g"
images/
```

Examples:

* Feature Importance
* Classification Metrics
* Correlation Matrix
* Embedding Space
* Fairness Analysis

---

## ⚠️ Critical Findings

### 🔴 Feature-Target Leakage

Keyword features directly define the target → leads to artificial performance.

### ⚖️ Bias & Fairness

* Dataset skewed toward CS domain (~78%)
* Potential bias against healthcare NLP papers

### 🔍 Model Behavior

* SHAP shows keyword dominance
* Structural features have minimal impact

---

## 🛠️ Tech Stack

* Python
* scikit-learn
* pandas, numpy
* matplotlib
* sentence-transformers
* SHAP
* Gradio

---

## ▶️ How to Run

### 1. Clone Repo

```id="d6v2qk"
git clone https://github.com/your-username/your-repo.git
cd your-repo
```

### 2. Install Dependencies

```id="ktz2gq"
pip install -r requirements.txt
```

### 3. Run Notebooks

Open in VS Code / Jupyter:

1. Phase1_EDA.ipynb
2. Phase2_Feature_Engineering.ipynb
3. Phase3_Semantic_Search.ipynb
4. Phase4_Deployment_xai.ipynb

---

## 🔮 Future Work

* Replace keyword features with full semantic pipeline
* Integrate vector databases (FAISS / Pinecone)
* Expand dataset diversity
* Build full RAG chatbot system

---

## 👥 Team

* Moulya Reddygari Bhupal
* Anisha Gehlot
* Sreyesh Varma Konduru
* Karthikeya Myneedu

---

## 📄 License

Academic project for coursework.

## ⚙️ Installation & Setup

### 1. Clone Repository
```bash
git clone https://github.com/Moulya002/AI-Chatbot-for-Research-Paper-Analysis-Using-NLP-and-RAG.git
cd AI-Chatbot-for-Research-Paper-Analysis-Using-NLP-and-RAG