## Manipulative Review Detection on the Qpon Application  
Semi-Supervised Learning with Mean Teacher and UST

This repository contains code, datasets, and analysis results for the final project of the **Statistical Machine Learning** course. The study focuses on detecting manipulative reviews (*buzzer* or *soft promotion*) in the **Qpon** mobile application on Google Play Store using a **semi-supervised learning** approach based on neural networks.

---

## Research Objectives
- Detect manipulative reviews in the Qpon application with limited labeled data.
- Compare two semi-supervised learning methods, Mean Teacher and Uncertainty-aware Self-Training (UST).
- Analyze the characteristics of manipulative reviews through descriptive analysis.

---

## Dataset

- **qpon_review.xlsx**  
  Raw dataset obtained from scraping Google Play Store, containing 3,312 reviews of the Qpon application.

- **qpon_review2.xlsx**  
  Preprocessed dataset with additional engineered features:
  - `word_count`: number of words in a review  
  - `length_cat`: review length category  
  - `has_promo`: indicator of promotional keywords  
  - `score_cat`: rating score represented as a categorical variable  

- **qpon_sample_600_for_manual_labeling.xlsx**  
  Subset of reviews selected via stratified sampling for manual annotation.

- **final_df.csv**  
  Final dataset combining manual labels and UST model predictions, used for descriptive analysis.

---

## Notebooks Description

- **Sampling_for_Manual_Labeling.ipynb**  
  Implements stratified sampling to select 600 reviews for manual labeling.

- **Mean_Teacher.ipynb**  
  Implementation of the Mean Teacher semi-supervised learning method using IndoBERTweet and review metadata.

- **UST.ipynb**  
  Implementation of Unsupervised Self-Training with high-confidence pseudo-labeling.

- **Descriptive.ipynb**  
  Descriptive analysis of manipulative and non-manipulative reviews, including label distribution, rating distribution, word clouds, text length, and interaction statistics.

---

## Methods
- Text Encoder: **IndoBERTweet**
- Approach: **Semi-Supervised Learning**
  - Mean Teacher
  - Unsupervised Self-Training (UST)
- Evaluation Metric: **Weighted F1-score**

---

## Academic Context
This repository was developed as part of the **Statistical Machine Learning** course  
Department of Statistics  
Sepuluh Nopember Institute of Technology

---

## Notes
- All code and data are intended for academic use only.
- The dataset is derived from publicly available sources and is not used for commercial purposes.
- Automatically generated labels do not represent absolute ground truth.
