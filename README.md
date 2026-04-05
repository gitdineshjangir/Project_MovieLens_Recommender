# 🎬 MovieLens Recommender System

## 📌 Project Overview

This project develops an end-to-end **personalized recommendation system** using the MovieLens dataset as a proxy for an eCommerce recommendation engine.

It combines multiple approaches:
- **Collaborative Filtering (Item-KNN)**
- **Matrix Factorization (Truncated SVD)**
- **Content-Based Filtering (TF-IDF)**
- **Hybrid Ensemble Model**

The system generates **Top-N recommendations** while balancing:
- Accuracy
- Coverage
- Fairness

---

## 🎯 Problem Statement

Large-scale digital platforms struggle to surface relevant items efficiently.

> This project frames the challenge as a **Top-N recommendation problem**, predicting items a user is most likely to engage with.

### Success Metrics
- **Primary:** NDCG@K  
- **Secondary:** Precision@K, Recall@K, MAP@K  
- **Additional:** Coverage  
- **Supplementary:** RMSE & MAE (for SVD)

### Business Objective
- Improve recommendation relevance  
- Increase user engagement  
- Enhance catalog exploration  

---

## 📊 Dataset

### Source
MovieLens Latest Small Dataset  
https://grouplens.org/datasets/movielens/

### Data Components
- Ratings (user-item interactions)
- Movies (metadata, genres)
- Tags (user-generated features)

### Key Characteristics
- Highly **sparse matrix**
- Strong **long-tail distribution**
- **Temporal dynamics**

---

## ⚙️ Installation

```bash
pip install numpy pandas matplotlib scikit-learn scipy joblib
```

---

## ▶️ How to Run

1. Download dataset and place in:
   ```
   /data/raw/ml-latest-small.zip
   ```

2. Open notebook:
   ```
   Project_MovieLens_Recommender_V1.5.ipynb
   ```

3. Run all cells sequentially

---

## 🧠 Methodology

### Data Processing
- Chronological train/test split
- Sparse matrix construction (CSR)
- No zero-filling for missing ratings

### Models Implemented
- Popularity Baseline
- Item-Item KNN
- Truncated SVD
- Content-Based (TF-IDF)
- Hybrid Ensemble

### Evaluation Approach
- Top-N ranking evaluation
- Time-aware validation
- Hyperparameter tuning
- Fairness analysis

---

## 📈 Results Summary

*(Derived from notebook outputs)*

- Hybrid model achieved **best overall ranking performance**
- SVD captured strong latent relationships (best RMSE/MAE)
- Item-KNN performed well for active users
- Content-based model improved cold-start handling
- Popularity model showed strong head-item bias

### Key Observations
- Ranking metrics are more relevant than RMSE for recommendation
- Hybrid models provide best performance trade-offs
- Temporal split improves realism

---

## ⚖️ Fairness & Bias Insights

- High-activity users receive better recommendations
- Strong **popularity bias** observed
- Long-tail items underrepresented
- Hybrid model partially mitigates bias

### Recommended Mitigations
- Popularity-aware reranking
- Cold-start improvements
- Long-tail exposure balancing

---

## 🏗️ Architecture Overview

```text
User → Feature Engineering → Candidate Generation
     → Model Scoring (KNN / SVD / Content)
     → Hybrid Aggregation → Top-N Output
```

---

## 📂 Project Structure

```text
├── data/
├── models/
├── reports/
├── notebooks/
├── requirements.txt
└── README.md
```

---

## 🚀 Key Features

- Sparse matrix optimization
- Hybrid recommendation strategy
- Ranking-based evaluation
- Fairness analysis
- Exportable models (joblib/pickle)

---

## 👤 Author

**Dinesh Jangir**

---

## 📌 Notes

- MovieLens used as proxy for eCommerce systems
- Approach applicable to:
  - Product recommendation
  - Streaming platforms
  - Personalization engines
