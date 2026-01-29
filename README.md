# naive-bayes-sentiment-model  
Local sentiment analysis model based on Naive Bayes, designed for privacy, efficiency and real-world product reviews.

---

## Project Overview

This project presents the development and evaluation of a **local AI model for sentiment analysis** of product reviews using the **Multinomial Naive Bayes algorithm**.

The goal was to design a **compact, resource-efficient NLP model** that:

- runs locally (no cloud required)
- is privacy-friendly
- works across different product domains
- achieves competitive performance compared to more complex AI models

The model classifies product reviews into **sentiment categories (positive / negative)** and is evaluated using standard machine learning metrics.

---

## Why This Project Matters

Many modern NLP systems rely on large cloud-based models.  
This project demonstrates that **simple, lightweight ML models** can still deliver strong performance while:

- protecting user data
- reducing computational cost
- remaining deployable on low-resource devices

---

## Libraries

- **scikit-learn** — ML pipeline, TF-IDF, Naive Bayes, evaluation  
- **NLTK** — Text preprocessing (tokenization, lemmatization, stopwords)  
- **pandas** — Data handling  
- **NumPy** — Numerical operations  

---

## Dataset

**Source:** Amazon Reviews Dataset (Kaggle)

A large dataset with labeled reviews was used. For performance and experimentation:

- 10000 training samples  
- 2000 test samples  

The dataset was preprocessed to ensure:

- balanced class distribution  
- clean and structured text data  

---

## Text Processing Pipeline

- Text cleaning (lowercase, remove special characters, links, numbers)
- Tokenization
- Stopword removal
- Lemmatization (NLTK)
- TF-IDF vectorization

---

## Feature Engineering (TF-IDF)

Key optimized parameters:

- `max_features`
- `ngram_range`
- `stop_words`
- `min_df`, `max_df`
- `use_idf`, `smooth_idf`, `sublinear_tf`
- `norm`

These parameters were tuned using **Grid Search** and later **5-Fold Cross Validation**.

---

## Model

**Classifier:** Multinomial Naive Bayes

**Why Naive Bayes?**

- Low computational requirements  
- Fast training  
- Works well for text classification  
- Suitable for local deployment  
- Robust against overfitting in small models  

---

## Evaluation Metrics

Model performance was measured using:

- Accuracy  
- Precision  
- Recall  
- F1-Score  
- Confusion Matrix  
- Training & prediction time  

---

## Limitations

- Limited ability to understand context, irony, or sarcasm  
- Assumes word independence  
- Less expressive than deep neural networks  

---

## Thesis Context

This repository is part of a **Bachelor thesis project** in Technical Communication at Hochschule München.
