# 🎬 Movie Recommender System — TMDB 5000 Dataset

## 🧠 Project Overview

**Title:** Movie Recommender System  
**Objective:** Build a content-based movie recommender system using the TMDB 5000 dataset to suggest movies similar to a given title.

This project leverages natural language processing (NLP) techniques to analyze movie descriptions and compute similarity scores between movies, enabling personalized recommendations.

---

## 📌 Problem Statement

In the modern digital age, viewers have access to a massive library of movies and shows. The challenge is to help users discover content they are likely to enjoy. This project aims to build a **content-based movie recommendation system** that uses metadata (such as overview, cast, crew, and popularity) to recommend similar movies.

---

## 📊 Dataset Description

The project uses two datasets from TMDB:

- `tmdb_5000_movie.csv`: Contains movie metadata like title, overview, vote average, vote count, and popularity.
- `tmdb_5000_credit.csv`: Contains cast and crew information for each movie.

These datasets are merged using a common `id` column to form a complete dataset.

---

## ⚙️ Methodology

### Steps Performed:
1. Loaded and merged the `movie` and `credit` datasets using `pandas`.
2. Calculated a **weighted rating** for each movie using the IMDB formula based on vote count and vote average.
3. Visualized the most **popular movies** using Matplotlib.
4. Cleaned and processed the **overview** text column.
5. Used **TF-IDF vectorization** to convert movie descriptions into numerical vectors.
6. Calculated **cosine similarity** between movie descriptions.
7. Built a **recommendation function** that returns the top 10 most similar movies for a given input.

---

## 🧪 Machine Learning / NLP Techniques

### ✅ Techniques Used:
- **TF-IDF Vectorization:** Converts text to a weighted term-document matrix.
- **Cosine Similarity:** Measures similarity between two vectors (movie overviews).
- **IMDB Weighted Rating Formula:** Adjusts for movies with low vote counts.

### ✅ Pros:
- Simple, interpretable, and fast.
- Works well for descriptive content-based filtering.
- No need for user history or ratings.

### ❌ Cons:
- Can't handle cold-start problems well (e.g., new movies).
- Doesn't consider user preferences or behavior (no collaborative filtering).
- Recommends similar content only by textual similarity, not taste.

---

## 🔁 Alternatives You Can Explore

- **CountVectorizer + Cosine Similarity** – Simpler than TF-IDF.
- **Word2Vec/Doc2Vec** – Semantic vector embeddings.
- **Collaborative Filtering (SVD, ALS)** – Based on user-item interactions.
- **Hybrid Models** – Combine content and collaborative filtering.
- **Deep Learning Models** – Neural networks for textual embeddings and recommendations.

---

## 💻 How to Run Locally

## ✅ Prerequisites:

- Python 3.x installed on your system
- Install required Python packages:
- Clone or download this project directory.

```bash
pip install pandas numpy scikit-learn matplotlib
```
- Run the script using:

```bash
python Stock_DT_algo.py
```

## 🖥️ You Should See:
- A list of the top 10 recommended movies for the input title (e.g., Avatar).
- A horizontal bar chart showing the most popular movies by popularity.
- 
## Conclusion
This project provides a foundational example of how to build a content-based movie recommender system using movie metadata and natural language processing. It demonstrates how TF-IDF and cosine similarity can be used to suggest similar movies based on descriptions. While effective for basic use cases, there are many opportunities to enhance this system:
- Try collaborative filtering for user-personalized recommendations.
- Use word embeddings (Word2Vec, BERT) for more semantic understanding of descriptions.
- Incorporate user ratings and preferences for hybrid recommendations.
- Improve performance using dimensionality reduction or model optimization.
- Add a web interface or deploy it using Flask or Streamlit.

This system is a great starting point for building more sophisticated and personalized movie recommendation platforms.
