# 📓 Thesis Notebooks — Multilingual RAG & Economic Sentiment Analysis

> **ENSSEA Master's Thesis** | Si Tayeb Houari | 2025–2026  
> All Jupyter notebooks used in the research, experiments, and analysis.

---

## 📁 Notebooks Overview

| Notebook | Description | Key Output |
|----------|-------------|-----------|
| `thesis_main.ipynb` | Core research notebook — full pipeline | Sentiment index, forecasting results |
| `sentiment_analysis.ipynb` | Model comparison & ensemble calibration | F1 scores, confusion matrices |
| `forecasting.ipynb` | ARIMA vs SARIMAX + sentiment | RMSE, Granger, DM test |
| `rag_evaluation.ipynb` | RAG pipeline evaluation | Precision@k, MRR, faithfulness |

---

## 🔬 What's Inside

### 📊 Sentiment Analysis Pipeline

- **Data preprocessing** for Arabic, French, and English economic text
- **Model benchmarking**: FinBERT vs XLM-RoBERTa vs Economic Lexicon
- **Ensemble weighting** calibration
- **Yearly Sentiment Index** construction (2000–2025)
- Visual output: polarity trend chart with labeled economic events

### 📈 Economic Forecasting

- **ARIMA(1,1,1)** baseline model
- **SARIMAX** augmented with ensemble sentiment as exogenous variable
- **Granger causality test**: Does sentiment Granger-cause economic indicators?
- **Diebold-Mariano test**: Is SARIMAX statistically significantly better?
- Variables: Inflation (CPI %), GDP Growth, Unemployment, Exchange Rate
- Country: Algeria (DZ), data from World Bank / IMF

### 🔍 RAG Evaluation

- Automatic query generation from indexed documents
- Retrieval metrics: Precision@k, Recall@k, MRR, NDCG
- Faithfulness scoring using LLM-as-judge
- Comparison: FAISS-only vs FAISS + BM25 + CrossEncoder

---

## 🚀 How to Run

### Option 1: Google Colab (Recommended)

Click the badge below to open directly in Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/)

### Option 2: Local Environment

```bash
git clone https://github.com/YOUR_USERNAME/thesis-notebooks.git
cd thesis-notebooks
pip install -r requirements.txt
jupyter notebook
```

---

## 📦 Required Libraries

```bash
pip install transformers sentence-transformers faiss-cpu torch
pip install statsmodels scipy scikit-learn pandas numpy
pip install matplotlib langdetect groq
pip install rank-bm25 PyPDF2 python-docx
```

---

## 📊 Key Visualizations Generated

### Yearly Ensemble Sentiment Index (2000–2025)
![Sentiment Index](../figures/yearly_sentiment_index_line.png)

The chart captures major Algerian macroeconomic events:
- 🟢 **2004–2005** — Oil boom
- 🔴 **2008–2009** — Global financial crisis
- 🟢 **2011–2012** — Oil boom (peak sentiment)
- 🔴 **2014–2016** — Oil price shock
- 🔴 **2020** — COVID-19 pandemic
- 🟢 **2022–2025** — Recovery trend

---

## 📂 Data Sources Used

| Dataset | Language | Source |
|---------|----------|--------|
| LABR | Arabic | [mohamedadaly/labr](https://huggingface.co/datasets/mohamedadaly/labr) |
| Sentiment140 | English | [stanfordnlp/sentiment140](https://huggingface.co/datasets/stanfordnlp/sentiment140) |
| Bank of Algeria Reports | AR/FR | Bank of Algeria Official Website |
| IMF Article IV Reports | EN/FR | IMF.org |
| World Bank Indicators | — | data.worldbank.org |

---

## 🔗 Related Repositories

| Repo | Description |
|------|-------------|
| [thesis-multilingual-rag-sentiment](https://github.com/YOUR_USERNAME/thesis-multilingual-rag-sentiment) | Main thesis repository |
| [rag-sentiment-app](https://github.com/YOUR_USERNAME/rag-sentiment-app) | Deployed web application |
| [thesis-evaluation-data](https://github.com/YOUR_USERNAME/thesis-evaluation-data) | RAG evaluation queries & gold labels |

---

*© 2026 Si Tayeb Houari — ENSSEA Master's Thesis*
