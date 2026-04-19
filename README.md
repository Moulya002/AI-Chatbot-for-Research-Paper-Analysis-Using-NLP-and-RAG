# AI Chatbot for Research Paper Analysis using NLP and RAG

## 📌 Project Overview
This project builds an intelligent system to analyze research papers using Natural Language Processing (NLP) and Retrieval-Augmented Generation (RAG). The goal is to filter, retrieve, and interpret relevant academic papers efficiently.

The system acts as a **pre-filtering gate** before a RAG pipeline, ensuring that only relevant documents are used for downstream question answering and analysis.

---

## 🚀 Key Features
- 📄 Automated research paper collection (ArXiv API)
- 🧹 Text preprocessing and feature engineering
- 🤖 Machine Learning classifier for relevance detection
- 🔍 TF-IDF based feature extraction
- 📊 Explainable AI (Feature Importance & SHAP)
- ⚖️ Fairness and bias analysis
- 🌐 Simple interface using Gradio (for testing)

---

## 🧠 Methodology

### Data Collection
- Source: ArXiv API
- Total Papers: ~462
- Domains: NLP, RAG, Healthcare AI, Semantic Search

### Preprocessing
- Lowercasing
- Removing special characters
- Text cleaning using regex

### Feature Engineering
- TF-IDF Vectorization
  - `max_features = 5000`
  - `stop_words = 'english'`

### Model
- Logistic Regression
  - `max_iter = 1000`

### Train-Test Split
- 80% Training / 20% Testing
- `random_state = 42`

---

## 📊 Results

- Accuracy: **1.00**
- Precision: **1.00**
- Recall: **1.00**
- F1 Score: **1.00**

⚠️ **Important Insight**:  
The perfect performance is due to **feature-target leakage**, where keyword-based features are used to define the target variable (`is_rag_relevant`). When these features are removed, performance drops significantly (F1 ≈ 0.52), indicating limited generalization.

---

## ⚖️ Explainability & Fairness

- SHAP analysis identifies key features influencing predictions
- Keyword-based features (e.g., *RAG, grounding*) dominate decisions
- Structural features (e.g., number of authors) have minimal impact

Fairness audits show:
- Strong performance across query topics
- Limited evaluation for non-CS domains due to dataset imbalance

---

## ⚙️ Installation & Setup

### 1. Clone Repository
```bash
git clone https://github.com/Moulya002/AI-Chatbot-for-Research-Paper-Analysis-Using-NLP-and-RAG.git
cd AI-Chatbot-for-Research-Paper-Analysis-Using-NLP-and-RAG