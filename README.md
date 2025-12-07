# **📘 App Review Sentiment Analysis — NLP Pipeline**

This repository delivers a focused, insight-driven sentiment-analysis workflow engineered to transform raw application reviews into structured intelligence. The architecture is intentionally lean—no wasted motion, no unnecessary components—just a disciplined pipeline crafted for clarity, reproducibility, and operational impact.

---

# **🚀 Executive Summary**

In a digital environment where user feedback grows faster than teams can interpret it, this project provides a lightweight yet enterprise-ready NLP solution.
The pipeline captures reviews automatically, cleans and vectorizes the text, and trains multiple deep-learning models to classify sentiments into **Positive**, **Neutral**, and **Negative** categories.

The mission is concise:
**convert raw opinions into strategic signals—accurate, measurable, and deployment-ready.**

---

# **📂 Project Structure**

```bash
app-review-sentiment-analysis-nlp/
│
├── Scraping_Dataset.ipynb
│      Review scraper (Tokopedia) with automated extraction workflow.
│
├── Pelatihan_Model_Analisis_Sentimen.ipynb
│      NLP preprocessing, deep-learning training, and evaluation notebook.
│
├── ulasan_aplikasi_tokped.xlsx
│      Raw dataset generated from the scraping phase.
│
├── requirement.txt
│      Python dependency list for environment reproduction.
│
└── README.md
       Project documentation.
```

The structure is intentionally minimalistic, enabling rapid iteration and long-term maintainability.

---

# **🧩 Core Features**

### **✓ Automated Web Scraping**

Fetches user reviews directly from the platform, ensuring fresh and authentic sentiment data.

### **✓ End-to-End Preprocessing Pipeline**

Cleaning, tokenization, normalization, padding, class balancing, and sequence vectorization.

### **✓ Multi-Model Deep Learning Training**

Three architectures were deployed and evaluated:

* **Bidirectional LSTM**
* **CNN + LSTM Hybrid**
* **GRU Network**

### **✓ Metric-Driven Evaluation**

Precision, recall, F1-score, confusion matrix, and training/testing accuracy.

### **✓ Scalable Design**

The pipeline is ready for expansion into BERT, IndoBERT, or full transformer stacks.

---

# **⚙️ Installation**

Install dependencies:

```bash
pip install -r requirement.txt
```

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Run the pipeline in order:

1. **Scraping_Dataset.ipynb**
2. **Pelatihan_Model_Analisis_Sentimen.ipynb**

---

# **📊 Full Workflow Overview**

```
[Scraper]
      ↓
[Raw Dataset]
      ↓
[Text Cleaning & Normalization]
      ↓
[Tokenization → Padding → Encoding]
      ↓
[Deep Learning Model Training]
      ↓
[Evaluation & Reporting]
```

Each step is completely annotated inside the notebooks.

---

# **🤖 Deep Learning Model Performance**

The sentiment classifier was trained on thousands of real application reviews.
Three architectures were benchmarked using the same preprocessing pipeline and identical train/test splits.

## **1️⃣ Bidirectional LSTM**

| Metric                | Score      |
| --------------------- | ---------- |
| **Training Accuracy** | **97.92%** |
| **Testing Accuracy**  | **94.13%** |

Key Notes:
Strong contextual understanding; excels in semantic depth. Slight performance dip on minority classes due to dataset imbalance.

---

## **2️⃣ CNN + LSTM Hybrid (Best Model)**

| Metric                | Score                    |
| --------------------- | ------------------------ |
| **Training Accuracy** | **97.53%**               |
| **Testing Accuracy**  | **94.21%** ⭐ *(Highest)* |

Key Notes:
Combines convolutional pattern extraction with sequence modelling.
Consistently outperforms others in generalization—this architecture is selected as the **final recommended model**.

---

## **3️⃣ GRU Model**

| Metric                | Score      |
| --------------------- | ---------- |
| **Training Accuracy** | **97.47%** |
| **Testing Accuracy**  | **94.19%** |

Key Notes:
Lightweight and efficient; nearly identical performance to LSTM but with lower computational cost.

---

## **📈 Model Comparison Summary**

| Model              | Train Acc | Test Acc   |
| ------------------ | --------- | ---------- |
| Bidirectional LSTM | 97.92%    | 94.13%     |
| **CNN + LSTM**     | 97.53%    | **94.21%** |
| GRU                | 97.47%    | 94.19%     |

**Conclusion:**
The **CNN + LSTM hybrid** delivers the strongest balance of precision, generalization, and sequence understanding—making it the recommended production candidate.

---
