# AI-Driven Location Recommendation System

## Overview
This repository contains an end-to-end Python-based recommendation engine that generates personalized venue suggestions based on user check-in history and semantic location data. Built using the FourSquare dataset, this system translates raw user behavior into actionable insights by combining collaborative filtering, natural language processing (TF-IDF), and geospatial optimization. 

The project demonstrates a scalable approach to solving complex business constraints, specifically focusing on data pipeline engineering, high-dimensional data analysis, and mathematical optimization for group logistics.

## Core Business Use Cases
1. **Personalized Venue Recommendations (AI/NLP):** Recommends 10 novel, unvisited locations for a user based on their historical preferences and semantic category matching using TF-IDF and collaborative filtering.
2. **User Similarity Clustering (Machine Learning):** Identifies the top 10 most similar users within the dataset by computing high-dimensional vector distances using K-Nearest Neighbors (KNN) and cosine similarity.
3. **Geospatial Group Optimization (Analytics):** Determines the optimal central meeting point for a group of 5 users. The algorithm calculates the geographic centroid of the users' most frequented locations and minimizes the collective travel distance to suggest the most efficient, fair meeting venue.

## Data Architecture & ETL Pipeline
To ensure efficient model performance on high-dimensional data, a robust ETL pipeline was developed:
* **Extraction:** Ingested raw FourSquare check-in datasets and location metadata.
* **Transformation:** 
  * Cleansed duplicate entries and standardized inconsistent venue category labels.
  * Engineered hierarchical category paths for semantic clarity.
  * Constructed user-location matrices and converted them into memory-efficient Compressed Sparse Row (CSR) formats to accelerate similarity computations.
* **Load:** Outputted a validated, structured dataset optimized for scalable machine learning queries.
* 
## Tech Stack
| Category | Tools |
|---|---|
| Language | Python |
| Data processing | Pandas, NumPy, SciPy (sparse CSR) |
| Machine learning | scikit-learn (KNN, TF-IDF, cosine similarity) |
| Geospatial & optimization | GeoPy, SciPy (optimize) |
| Visualization | Matplotlib |
