# cosmo-semantic-audit

# Semantic Gap Analysis: Cosmo Intent Classifier

**Author:** Niha Salman  
**Date:** July 2025

---

## 📌 Overview

This repository contains a Jupyter notebook that systematically identifies semantic blind spots in Cosmo's exact-match retrieval engine by applying TF-IDF vectorization, Latent Semantic Analysis (LSA), and cosine similarity.

**[🌌 Meet Cosmo →](https://[cosmo-the-chatbot.web.app/cosmo.html])** – Live conversational interface  
**[📖 Learn more about Cosmo →](./cosmo-background.md)**

Cosmo is an intentionally imperfect, handcrafted conversational interface built to explore the balance between transparency and capability in AI. However, users ask the same question in many different ways, and Cosmo's exact-match engine often fails to recognize semantically equivalent queries. This analysis quantifies that gap and demonstrates how LSA can dramatically improve retrieval accuracy.

---

## 📊 Key Findings

| Method | Average Score | Strong Alignment | Improvement |
|--------|---------------|------------------|-------------|
| Random Baseline | 0.1074 | — | — |
| Cosmo (Current System) | 0.8290 | — | Precision-focused |
| TF Baseline | 0.7967 | 78.9% | Secondary reference |
| **LSA (k=13)** | **0.9665** | **98.6%** | **+21.3% vs TF** |

**Key Insight:** LSA with just 13 latent dimensions (capturing only 9.6% of variance) achieves near-perfect retrieval alignment. Additional dimensions introduce noise rather than signal.

---

## 🔍 What This Analysis Does

1. **Extracts** 680 variations from 139 Firestore documents
2. **Generates** 7,800 experimental queries from 794 unique topics
3. **Compares** three methods: Random, TF, and LSA (TF-IDF + SVD)
4. **Validates** results with confidence intervals and paired t-tests
5. **Identifies** actionable gaps in the knowledge base

---

## 📁 Repository Structure

```
├── cosmo_semantic_audit.ipynb # Main Jupyter notebook
├── cosmo_audit_technical_report.pdf # Full technical report
├── cosmo-background.md # Background on Cosmo
└── README.md
```

---

## 🔒 Data Privacy Notice

**The `cosmo_baseline_data.json` file is NOT included in this repository.**

The notebook displays all pre-computed results when viewed on GitHub.

---

## 📈 Results Summary

### Cosmo Baseline vs. LSA

| Method | Average Score | Strong Alignment |
|--------|---------------|------------------|
| Cosmo | 0.8290 | Precision-focused |
| TF | 0.7967 | 78.9% |
| **LSA** | **0.9665** | **98.6%** |

### Performance by Query Type

| Query Type | TF Score | LSA Score | Improvement |
|------------|----------|-----------|-------------|
| Synonym-heavy | 0.7525 | 0.9667 | **+28.5%** |
| Direct | 0.8264 | 0.9664 | **+16.9%** |

### Performance by Topic Category

| Category | TF Score | LSA Score | Improvement |
|----------|----------|-----------|-------------|
| Management | 0.7417 | 0.9708 | **+30.9%** |
| Career | 0.7580 | 0.9722 | **+28.3%** |
| Projects | 0.7540 | 0.9630 | **+27.7%** |
| Skills | 0.7583 | 0.9668 | **+27.5%** |
| Education | 0.7821 | 0.9658 | **+23.5%** |

---

## 🛠️ Methodology

1. **Data Extraction:** 139 documents from Firebase Firestore
2. **Preprocessing:** Lowercasing, removing possessives, stripping punctuation, removing stopwords
3. **Query Generation:** 7,800 queries from 794 topics using templates and synonyms
4. **Vectorization:** TF, TF-IDF, and LSA (with auto-selected k=13)
5. **Similarity Measurement:** Cosine similarity with statistical validation
6. **Analysis:** Confidence intervals, paired t-tests, query type analysis, topic category analysis

---

## 📖 Technical Report

A full technical report is available as `cosmo_audit_technical_report.pdf` in this repository. It provides a detailed explanation of the methodology, results, and implications for Cosmo.

---

## 🤝 Contributing

This project is part of my portfolio. While I'm not actively seeking contributions, feel free to fork and adapt for your own use.

---

## 📧 Contact

Niha Salman  
Email: niha.salman@gmail.com  
LinkedIn: [linkedin.com/in/niha-salman-b304a912b](https://linkedin.com/in/niha-salman-b304a912b)

---

## 🙏 Acknowledgments

This analysis was built as part of my journey exploring the balance between transparency and capability in AI systems. Cosmo was designed to be intentionally imperfect—this research validates that philosophy while showing a path forward.

---
