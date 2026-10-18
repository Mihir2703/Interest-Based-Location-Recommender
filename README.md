# Interest-Based Location Recommendation System

A Python recommendation system that suggests venues based on user check-in history and semantic venue categories. Built on the Foursquare NYC check-in dataset as the final project of the *Data Science with Python* course.

## Overview

The Interest-Based Location Recommendation System analyzes user check-in history and venue categories to identify similar users, suggest relevant new venues and recommend a convenient meeting location for groups. It combines collaborative filtering, semantic category analysis and geospatial optimization, using machine learning techniques such as K-Nearest Neighbors (KNN), TF-IDF and cosine similarity. The system was developed and demonstrated on the Foursquare NYC check-in dataset.

## Use Cases

1. **Personalized recommendations (ML, text vectorization):** Suggests 10 new venues per user and category using TF-IDF category similarity and collaborative filtering, excluding venues already visited. *Value: relevant, novel suggestions instead of repeats.*
2. **User similarity (ML, data analysis):** Finds the 10 most similar users with KNN and cosine distance on sparse visit data. *Value: behavior-based user matching that supports peer-driven recommendations.*
3. **Group meeting point (data analysis, optimization):** Derives each user's location from check-in history and minimizes total travel distance for 5 users. *Value: a concrete, decision-ready venue recommendation.*

## Key Highlights

- **End-to-end workflow:** from raw data to ready-to-use recommendations in one Python project.
- **Data quality:** duplicate entries and inconsistent category labels were cleaned and standardized, so recommendations rest on reliable input.
- **Efficient on sparse data:** user-venue matrices stored in CSR format reduce memory use and speed up similarity computation.
- **Semantic understanding:** a hierarchical category structure lets the system recommend by venue type, not just by exact venue.
- **Personalization with novelty:** previously visited venues are filtered out, so every suggestion is new to the user.
- **Interpretable results:** outputs are simple ranked tables and a map visualization that non-technical users can read.

## Data Pipeline (ETL)

| Step | What was done |
|---|---|
| **Extract** | Ingested the raw Foursquare NYC check-ins and the cleaned category metadata. Checked column structure, data types and missing values. |
| **Transform** | Removed duplicate entries, standardized inconsistent venue category labels, added descriptive category names and hierarchical category paths, and merged them with the check-ins. |
| **Load** | Loaded the cleaned dataset into Pandas DataFrames and built user-venue matrices in Compressed Sparse Row (CSR) format for memory-efficient similarity computation. |

## Skills Demonstrated

- **Data engineering:** ETL, data cleaning, data validation, feature engineering
- **Data analysis:** user behavior analysis, aggregation, similarity analysis
- **Machine learning:** K-Nearest Neighbors, TF-IDF, cosine similarity, collaborative filtering
- **Optimization:** mathematical optimization, geospatial distance computation
  
## Tech Stack

| Category | Tools |
|---|---|
| Language | Python |
| Data processing | Pandas, NumPy, SciPy (sparse CSR) |
| Machine learning | scikit-learn (KNN, TF-IDF, cosine similarity) |
| Geospatial and optimization | GeoPy, SciPy (optimize) |
| Visualization | Matplotlib |
