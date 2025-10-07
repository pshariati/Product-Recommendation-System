# Product-Recommendation-System

A collaborative filtering system that recommends top-N products using user ratings data.

## Overview
Implements multiple recommendation models using the Surprise library:
- User–User Collaborative Filtering  
- Item–Item Collaborative Filtering  
- Matrix Factorization (SVD)

## Data
Dataset contains product ratings:
- `userId`, `productId`, `rating`, `timestamp`  
> **Note:** Data not included; adjust file paths as necessary.

## Methods
- **Library:** Surprise (`KNNBasic`, `SVD`)  
- **Similarity Metric:** Cosine similarity  
- **Evaluation:** Precision@10, Recall@10, F1@10  
- **Tuning:** GridSearchCV for SVD parameters (`n_factors`, `reg_*`, `lr_all`)  

## Reproducing Results
1. Load the dataset and prepare a Surprise `Dataset` object.  
2. Train and evaluate user–user, item–item, and SVD models.  
3. Compute ranking metrics (Precision@10, Recall@10, F1@10).  
4. Tune SVD hyperparameters for best performance.  

## Notes
- SVD achieved the best overall recommendation accuracy.  
- Ranking metrics are preferred to RMSE for evaluating recommender performance.  
- Modular notebook structure supports easy integration into larger pipelines.  

