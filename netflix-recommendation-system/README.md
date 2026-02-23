Project Overview

This project builds a personalized movie recommendation system using collaborative filtering with matrix factorization (Funk SVD) implemented via the Surprise library.

The model learns hidden user preferences and item characteristics from historical rating data and predicts unseen ratings to generate Top-N personalized recommendations.

Problem Statement

Streaming platforms host thousands of movies and TV shows, making content discovery challenging for users. Without personalization, users may struggle to find relevant content, leading to reduced engagement and increased churn risk.
This project aims to design a recommendation system that:
Learns from user rating behavior
Handles sparse user–item interaction data
Predicts unseen ratings
Provides personalized recommendation

Objective

Build a collaborative filtering recommendation system using matrix factorization
Learn latent user and item representations
Predict missing ratings in the interaction matrix
Evaluate performance using RMSE
Generate Top-N personalized recommendations

DataSet:
The dataset is available here:

Google Drive Link:

https://drive.google.com/drive/folders/13bpXsnmp9ihpimiHJCTaD9madUQNPkYo?usp=sharing

Due to file size limitations, it is not included in this repository.

Results:
Achieved competitive RMSE on the test dataset
Successfully generated personalized recommendations
Latent factors captured hidden preference patterns

Tech Stack:
Python
Surprise Library
NumPy
Pandas
Scikit-learn (for evaluation utilities)
