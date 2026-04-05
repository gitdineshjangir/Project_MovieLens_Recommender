# Project 🎬 MovieLens Recommender System Capstone
📌 Project Overview
This project builds an end-to-end personalized recommendation system using the MovieLens dataset as a proxy for an eCommerce product recommendation problem.
The solution combines:
Collaborative Filtering (Item-KNN)
Matrix Factorization (Truncated SVD)
Content-Based Filtering
Hybrid Ensemble Model
The system recommends the Top-N most relevant items for each user while balancing accuracy, coverage, and fairness.
---
🎯 Problem Statement
Digital platforms with large catalogs often struggle to surface relevant items to users, leading to low engagement and missed opportunities.
This project frames the problem as a Top-N recommendation task, where the goal is to predict which items a user is most likely to engage with.
Success Metrics:
Primary: NDCG@K
Secondary: Precision@K, Recall@K, MAP@K
Additional: Coverage
Supplementary: RMSE & MAE (for SVD)
Business Objective:
Improve recommendation relevance, increase engagement, and broaden catalog exposure.
---
📊 Dataset
Source
MovieLens Latest Small Dataset  
https://grouplens.org/datasets/movielens/
Description
Ratings: User ratings (0.5–5.0)
Movies: Titles and genres
Tags: User-generated metadata
Characteristics:
High sparsity
Long-tail distribution
Temporal interactions
---
⚙️ Installation
```bash
pip install numpy pandas matplotlib scikit-learn scipy joblib
```
---
▶️ How to Run
Place dataset in:
/data/raw/ml-latest-small.zip
Open notebook:
Project_MovieLens_Recommender_V1.5.ipynb
Run all cells sequentially
---
📈 Results Summary
Hybrid model achieved best ranking performance
SVD captured latent user-item relationships effectively
Item-KNN worked well for active users
Content-based improved cold-start
Popularity baseline showed strong bias
---
⚖️ Fairness Insights
High-activity users perform better
Popularity bias toward head items
Hybrid reduces bias partially
---
👤 Author
Dinesh Jangir
