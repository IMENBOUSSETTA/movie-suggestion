# 🎬 Movie Recommendation System — Collaborative Filtering (Cosine Similarity)

A clean, reproducible baseline recommender built with **pandas**, **NumPy**, and **scikit-learn** (cosine similarity on a user–movie matrix).

## 📦 Project Structure
```
.
├── main_pro.ipynb     # Polished, well-documented notebook
├── data/              # <-- Put movies.csv & ratings.csv here (not tracked)
└── README.md
```

## 🚀 Getting Started
1. Create and activate a Python 3.10+ environment.
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Add MovieLens CSVs to `./data/`:
   - `movies.csv` (columns: movieId, title, genres)
   - `ratings.csv` (columns: userId, movieId, rating, timestamp)
4. Open the notebook:
   ```bash
   jupyter notebook main_pro.ipynb
   ```

## 🧠 Approach
- Filter to well-rated items to reduce sparsity/noise (e.g., ≥500 ratings).
- Build a **user–movie** ratings matrix (users as rows, movies as columns).
- Compute **item–item cosine similarity**.
- Provide `recommend(title, k)` to return top-*k* similar titles.

## 🖼️ Optional: Posters via OMDb
Set an API key:
```bash
export OMDB_API_KEY="YOUR_KEY"
```
Then enable the optional cell to fetch posters for the recommendations.

## 📈 Ideas to Improve
- Rating normalization (mean-centering per user).
- Model-based recommenders: SVD/ALS/implicit.
- Hybrid content + collaborative features.
- Streamlit front-end for interactive search.

## 📝 License
MIT — feel free to use and adapt.
