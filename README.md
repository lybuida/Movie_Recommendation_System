### 🎬 Movie Recommendation System

A data-driven recommendation system that predicts user preferences and suggests movies using Content-Based Filtering, User-User Collaborative Filtering, and Item-Item Collaborative Filtering.

This project was built as part of the Data Analysis course at Ho Chi Minh City Open University (OU).

---

### 📌 Overview

In the digital era, streaming platforms like Netflix or Amazon Prime have millions of movies, making it difficult for users to choose content they like.
A Recommendation System personalizes user experience, increases satisfaction, and helps businesses retain customers.

This project applies machine learning techniques to build a movie recommendation system based on the MovieLens dataset.

---

### 🎯 Objectives

Apply data analysis & machine learning knowledge into practice.

Explore preprocessing, visualization, and model evaluation for recommender systems.

Compare different algorithms:

- Content-Based Filtering (CBF)

- User-User Collaborative Filtering (UCF)

- Item-Item Collaborative Filtering (ICF)

---

### 📂 Dataset

Source: MovieLens ml-latest-small

Files used:

- movies.csv → 9,743 movies (ID, title, genres).

- ratings.csv → 100,837 ratings (610 users, 1–5 scale).

---

### ⚙️ Data Processing

Cleaning: Handle nulls, duplicates, lowercase formatting.

Merging: Combine movies & ratings into a single dataframe.

Feature Engineering: Extract genres, encode categorical values.

Outlier Handling: Apply Bayesian Average & weighted rating.

Index Encoding: Normalize userId and movieId for sparse matrix representation.


### 📊 Visualization Insights

Most ratings lie between 3.0–4.5, showing positive bias.

Majority of users provide fewer than 100 ratings.

Most movies have fewer than 50 ratings.

Popular movies tend to have higher average ratings.


### 🤖 Models Implemented
1. Content-Based Filtering (CBF)

- Uses TF-IDF vectorization of genres.

- Predict ratings with Ridge Regression.

- RMSE = 0.9119

2. User-User Collaborative Filtering (UCF)

- Builds a user-user similarity matrix using Cosine Similarity.

- Predicts ratings from k-nearest neighbors.

- RMSE = 0.1021 (best performance)

3. Item-Item Collaborative Filtering (ICF)

- Builds an item similarity matrix.

- Recommends movies similar to user’s history.

- RMSE = 0.3893


### 📈 Evaluation

Metric: Root Mean Squared Error (RMSE).

Best model: User-User Collaborative Filtering (lowest RMSE, most consistent).

Limitations: Content-based lacks diversity, Item-based suffers from data sparsity.

Future Improvement: Hybrid model combining multiple approaches.

---

### 🗂️ Project Structure
Movie_Recommendation_System/
- Movie_Recommendation_System.ipynb   # Main notebook
- movies.csv                          # Movie dataset
- ratings.csv                         # Ratings dataset
- README.md                           # Project documentation

---

### 🚀 How to Run

#### Clone this repository:

- git clone https://github.com/lybuida/Movie_Recommendation_System.git

- cd Movie_Recommendation_System


#### Install dependencies:

- pip install -r requirements.txt


#### Run Jupyter Notebook:

- jupyter notebook Movie_Recommendation_System.ipynb

---

### 👨‍💻 Authors

Bùi Dạ Lý 

Huỳnh Lệ Giang

Võ Thị Ngọc Chi

---

### 📚 References

MovieLens Dataset

Machine Learning Cơ Bản (Nguyễn Trọng Hiếu)

Stanford – Mining of Massive Datasets (Chapter 9: Recommender Systems)

Simplilearn – Recommendation Systems Tutorials
