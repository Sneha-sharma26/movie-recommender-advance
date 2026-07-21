# 🎬 Movie Recommender

> A hybrid movie recommendation system built with **Streamlit**, **FastAPI**, **TF-IDF**, and the **TMDB API**.

## 🌐 Live Demo
https://movie-recommender-advance-ygstcrbvf5ev5lppcywga6.streamlit.app/

## 📖 Overview
This Movie Recommender is a full-stack recommendation system that combines a Streamlit frontend with a FastAPI backend. It delivers content-based recommendations using a precomputed TF-IDF matrix while enriching results with live TMDB movie details, posters, backdrops, and genre-based recommendations.

## ✨ Features
- 🔍 Keyword search with autocomplete
- 🎬 Trending, Popular, Top Rated, Upcoming & Now Playing home feeds
- 📄 Dedicated movie details page
- 🤖 TF-IDF content-based recommendations
- 🎭 Genre-based recommendations using TMDB Discover
- 🖼️ High-quality posters and backdrops
- ⚡ FastAPI REST API backend
- 🚀 Async HTTP requests using HTTPX
- 💾 Cached API responses in Streamlit
- 🔗 URL routing with query parameters

## 🏗 Architecture
```text
User
 │
 ▼
Streamlit Frontend
 │ REST API
 ▼
FastAPI Backend
 ├── TF-IDF Recommendation Engine
 ├── Genre Recommendation Engine
 ├── Local Pickle Models
 └── TMDB API
```

## 🛠 Tech Stack
### Frontend
- Streamlit
- Custom CSS

### Backend
- FastAPI
- Pydantic
- HTTPX
- CORS Middleware

### Machine Learning
- TF-IDF Vectorizer
- Cosine Similarity
- Content-Based Filtering

### Data
- Pandas
- NumPy
- Pickle

### External API
- TMDB API

## 📁 Project Structure
```text
.
├── app.py                 # Streamlit frontend
├── main.py                # FastAPI backend
├── movies.ipynb           # Data preprocessing
├── df.pkl
├── tfidf.pkl
├── tfidf_matrix.pkl
├── indices.pkl
├── movies_metadata.csv
└── requirements.txt
```

## 🚀 Installation
```bash
git clone https://github.com/Sneha-sharma26/movie-recommender-advance.git
cd movie-recommender-advance
pip install -r requirements.txt
```

Create a `.env` file:

```env
TMDB_API_KEY=your_api_key
```

Run the backend:

```bash
uvicorn main:app --reload
```

Run the frontend:

```bash
streamlit run app.py
```

## 📡 API Endpoints

| Endpoint | Description |
|----------|-------------|
| `/health` | Health check |
| `/home` | Home movie feed |
| `/tmdb/search` | Search movies |
| `/movie/id/{tmdb_id}` | Movie details |
| `/recommend/tfidf` | TF-IDF recommendations |
| `/recommend/genre` | Genre recommendations |
| `/movie/search` | Hybrid recommendation bundle |

## 🔮 Future Improvements
- Collaborative filtering
- User authentication
- Watchlist
- Personalized recommendations
- Trailer integration

## 👩‍💻 Author
**Sneha Sharma**

GitHub: https://github.com/Sneha-sharma26

If you found this project useful, consider giving it a ⭐.