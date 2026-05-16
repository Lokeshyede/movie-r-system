# 🎬 Movie Recommender System (MRS)

A professional, full-stack Movie Recommender System built using a **FastAPI** backend and a modern **Streamlit** frontend dashboard. The system leverages content-based filtering via **TF-IDF (Term Frequency-Inverse Document Frequency)** and integrates with the **TMDB (The Movie Database) API** to provide real-time metadata, posters, trending feeds, and multi-layered recommendations.

---

## 🚀 Features

- **Dynamic Home Feed:** Browse movies by categories like *Trending*, *Popular*, *Top Rated*, *Now Playing*, and *Upcoming*.
- **Smart Search & Auto-Suggestions:** Real-time dropdown suggestions as you type a movie keyword.
- **Hybrid Recommendation Engine:**
  - **TF-IDF Content-Based Filtering:** Analyzes local movie datasets to find similar storylines/metadata.
  - **Genre-Based Discovery:** Fetches top-performing movies sharing the same genre dynamically via TMDB.
- **Rich Media Representation:** Dynamic rendering of high-quality movie posters, release dates, genres, overviews, and backdrops.
- **Fully Asynchronous Backend:** High-performance routes handled asynchronously using `httpx` and `FastAPI`.

---

## 🛠️ Architecture & Tech Stack

### Backend (`MRS.py`)
- **FastAPI:** High-performance web framework for building APIs.
- **Scikit-Learn & Pandas:** For managing the movie dataset matrix and computing TF-IDF similarity vectors.
- **HTTPX:** Async HTTP client to make non-blocking requests to TMDB.
- **Pydantic:** Data validation and settings management using schemas.

### Frontend (`streamlit.py`)
- **Streamlit:** Interactive UI component structure with advanced state management (`st.session_state`) and dynamic URL query parameters.
- **Custom CSS:** Modern CSS Injection for responsive grids, hover effects, and crisp typography (`Inter` font).

---

## 📂 Project Structure

```text
├── MRS.py                  # FastAPI Backend Application
├── streamlit.py            # Streamlit Frontend Dashboard
├── require.txt             # Python Dependencies
├── .env                    # Environment Variables (To be created)
├── df.pkl                  # Pickled Pandas DataFrame containing movie data (Required)
├── indices.pkl             # Pickled Movie Index mapping (Required)
├── tfidf_matrix.pkl        # Pickled Pre-computed TF-IDF Matrix (Required)
└── tfidf.pkl               # Pickled TF-IDF Vectorizer object (Required)
