# 🎬  Movie Recommendation System

A Content-Based Movie Recommendation System built using **Sentence Transformers (SBERT)** and **Cosine Similarity**. This CLI-based application suggests movies based on natural language queries, analyzing movie titles, genres, user tags, and ratings to find semantically similar results.

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![PyTorch](https://img.shields.io/badge/PyTorch-Deep%20Learning-orange)
![SBERT](https://img.shields.io/badge/SBERT-Transformer-yellow)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458)

## 📌 Project Overview
This project moves beyond simple keyword matching. By leveraging the `all-MiniLM-L6-v2` transformer model, the system understands the "context" or "vibe" of a search query. It combines semantic similarity with movie popularity to ensure recommendations are not only relevant but also well-rated.

**Goal:** To build a real-world recommender system that understands user-based queries and item-based features.

## ✨ Key Features
* **Natural Language Search:** Search by genre, specific title, or abstract concepts (e.g., *"sad but beautiful"* or *"Animated Children Movies"*).
* **Hybrid Ranking Algorithm:** Recommendations are ranked by a combination of:
    1.  **Semantic Similarity:** How close the movie metadata is to your query.
    2.  **User Ratings:** Weighs suggestions by average user rating to prioritize high-quality films.
* **Interactive CLI:** A user-friendly command-line interface for continuous searching.
* **Data Visualization:** Includes PCA visualization of movie embeddings and a Confusion Matrix for evaluation.

## 🛠️ Tech Stack
* **Language:** Python
* **NLP Model:** `sentence-transformers` (Hugging Face)
* **Data Manipulation:** `pandas`, `numpy`
* **Machine Learning:** `scikit-learn` (PCA, Metrics), `torch`
* **Visualization:** `matplotlib`, `seaborn`

## 📂 Dataset
The project uses the **MovieLens** dataset containing:
* `movies.csv`: Titles and Genres.
* `ratings.csv`: User ratings (used for popularity filtering).
* `tags.csv`: User-generated tags (crucial for context).

*> Note: The data is pre-processed to merge genres, tags, and ratings into a single "metadata" string for vectorization.*

## ⚙️ How It Works (Methodology)

1.  **Data Preprocessing:** * Merged Movies, Tags, and Ratings.
    * Calculated "Popularity Stats" (Average Rating & Vote Count).
    * Filtered out noise (movies with < 10 votes).
2.  **Vectorization (Embedding):**
    * Constructed a `metadata` field: `Title + Genres + Tags + Rating`.
    * Encoded this metadata using the pre-trained **SBERT model** (`all-MiniLM-L6-v2`) into high-dimensional vectors.
3.  **Search & Retrieval:**
    * The user's query is encoded into the same vector space.
    * **Cosine Similarity** is calculated between the query vector and all movie vectors.
4.  **Scoring Logic:**
    * The final rank is determined by:
      $$Score = Similarity \times (\frac{AvgRating}{5.0})$$
    * This ensures that a movie that matches the query *perfectly* but is rated 1/5 appears lower than a movie that matches *well* and is rated 5/5.


## 📊 Visualization

### PCA Projection
The high-dimensional embeddings are reduced to 2D using PCA to visualize how movies cluster together based on similarity.
*(Visualization code included in the notebook)*

### Performance Evaluation
A confusion matrix is used to compare specific search intents (e.g., "Action") against the actual genre of the returned top results.

## 📸 Usage Example

```text
==================================================
🌟 NEURAL MOVIE RECOMMENDER SYSTEM 🌟
Built with: SBERT (Transformer) & Cosine Similarity
==================================================

👉 Enter search query: Animated Children Movies

 Results for 'Animated Children Movies'
--------------------
🎬 Partly Cloudy (2009) | Score: 0.46
🎬 Monsters, Inc. (2001) | Score: 0.45
🎬 Kung Fu Panda (2011) | Score: 0.45
🎬 Toy Story 2 (1999)   | Score: 0.45
