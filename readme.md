# 🎬 Hybrid Movie Recommender System

A production-ready hybrid movie recommendation system that combines:

- 📊 Content-Based Filtering (TF-IDF + Cosine Similarity)
- 🎭 Genre-Based Recommendations (TMDB Discover API)
- ⚡ FastAPI Backend
- 🎨 Streamlit Frontend
- 🌍 Live Movie Metadata from TMDB API

---

## 🚀 Features

### 🔎 Smart Search
- Keyword-based movie search
- Autocomplete suggestions
- Real-time TMDB integration

### 📄 Movie Details Page
- Poster
- Backdrop
- Overview
- Genres
- Release date

### 🎯 Hybrid Recommendations

1. **TF-IDF Similar Movies**
   - Content similarity based on movie metadata
   - Cosine similarity over TF-IDF matrix
   - Top-N similar titles returned

2. **Genre-Based Recommendations**
   - Uses TMDB discover endpoint
   - Popular movies from the same genre

### 🏠 Home Feed
- Trending
- Popular
- Top Rated
- Upcoming
- Now Playing

---

## 🏗️ Tech Stack

### Backend
- Python
- FastAPI
- HTTPX (async API calls)
- Pandas
- NumPy
- Scikit-learn (TF-IDF)
- TMDB API

### Frontend
- Streamlit

---

## 📸 Screenshots

### 🔹 FastAPI Backend – Interactive API Docs
Swagger UI documentation generated automatically by FastAPI (`/docs` endpoint).

![FastAPI Docs](assets/Screenshot%202026-02-21%20193437.png)

---

### 🔹 Backend Code Structure (VS Code)
Project structure and implementation of the FastAPI backend with TF-IDF integration.

![Backend Code](assets/Screenshot%202026-02-21%20193859.png)

---

### 🔹 Streamlit Frontend – Running Application
Live Streamlit application connected to the FastAPI backend.

![Streamlit Running](assets/Screenshot%202026-02-21%20194246.png)

---

### 🔹 Movie Search with Autocomplete
Keyword-based movie search with dynamic suggestions powered by TMDB API.

![Search Movie](assets/Screenshot%202026-02-21%20194308.png)

---

### 🔹 Movie Details & Recommendations
Detailed movie view with:
- Poster
- Overview
- Genre information
- TF-IDF similar movies
- Genre-based recommendations

![Movie Details](assets/Screenshot%202026-02-21%20194358.png)

---

### 🔹 Complete Frontend Interface
Full UI layout including home feed, search, and recommendation sections.

![Full Frontend](assets/Screenshot%202026-02-21%20194434.png)

## 🧠 Recommendation Architecture

### 1️⃣ Content-Based Filtering

- Preprocessed movie metadata
- TF-IDF vectorization
- Cosine similarity computation
- Sorted similarity scores
- Top-N results returned

### 2️⃣ Genre-Based Recommendation

- Fetch movie genres via TMDB
- Use `/discover/movie`
- Sort by popularity

---

## 📁 Project Structure


├── main.py # FastAPI backend
├── app.py # Streamlit frontend
├── df.pkl # Cleaned movie dataframe
├── indices.pkl # Title-to-index mapping
├── tfidf_matrix.pkl # TF-IDF sparse matrix
├── tfidf.pkl # TF-IDF vectorizer
├── movies_metadata.csv # Raw dataset
├── api key file
├── .gitignore


---

## 🔐 Environment Setup

Create a `.env` file in the root directory:


TMDB_API_KEY=your_api_key_here


Get your API key from:
https://www.themoviedb.org/

---

## ▶️ How to Run

### 1️⃣ Install dependencies


pip install -r requirements.txt


### 2️⃣ Start FastAPI backend


uvicorn main:app --reload


Backend runs at:


http://127.0.0.1:8000


### 3️⃣ Start Streamlit frontend


streamlit run app.py


---

## 🧪 API Endpoints

| Endpoint | Description |
|----------|------------|
| `/health` | Health check |
| `/home` | Home feed (popular, trending, etc.) |
| `/tmdb/search` | TMDB keyword search |
| `/movie/id/{id}` | Get movie details |
| `/recommend/tfidf` | Local TF-IDF recommendations |
| `/recommend/genre` | Genre-based recommendations |
| `/movie/search` | Hybrid bundle (details + recommendations) |

---

## 🌟 Why This Project Stands Out

- Hybrid recommendation system
- Async API architecture
- Clean backend/frontend separation
- Production-style error handling
- Real-world API integration
- Portfolio-ready structure

---

## 🔮 Future Improvements

- Add collaborative filtering
- Add user accounts & watch history
- Deploy backend (Render / Railway)
- Deploy frontend (Streamlit Cloud)
- Add Docker support
- Add Redis caching
- Add rating prediction

---

## 📜 License

MIT License