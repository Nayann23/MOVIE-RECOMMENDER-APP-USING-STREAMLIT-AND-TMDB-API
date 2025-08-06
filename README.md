# 🎬 MOVIE RECOMMENDER APP USING STREAMLIT AND TMDB API

A **content-based movie recommendation system** built with **Python, Streamlit**, and the **TMDB API**. This app suggests movies similar to the one selected by the user, displaying their posters for an intuitive and visually appealing user experience.

---

## 🚀 Project Overview

This project uses:
- A **precomputed similarity matrix** to compare movies based on their content
- **Streamlit** to build a fast and interactive web UI
- **TMDB API** to fetch movie posters in real-time

When a user selects a movie, the app recommends **5 similar movies** and shows their **posters** fetched dynamically via the TMDB API.

---

## 🧠 How It Works

1. The similarity matrix (cosine similarity) is computed based on metadata like genres, keywords, overview, etc.
2. When a movie is selected, the top 5 most similar movies (excluding the original) are retrieved from the matrix.
3. TMDB API is used to get the poster image for each recommended movie.
4. Results are displayed neatly using **Streamlit columns**.

---

## 📁 Project Structure

```
📦 movie-recommender-app-using-streamlit-and-tmdb-api
├── app.py                  # Main Streamlit app
├── recommendation.ipynb   # Jupyter notebook for preprocessing and model
├── README.md               # Project documentation
├── requirements.txt        # Dependencies (optional)
```

---

## ⚠️ Missing Files & Why They're Not Included

To keep the repository lightweight and avoid GitHub’s file size restrictions, the following large files **are not pushed**:

| File Name          | Size     | Description                          |
|--------------------|----------|--------------------------------------|
| `movies_dict.pkl`  | ~43 MB   | Dictionary containing movie metadata |
| `similarity.pkl`   | ~174 MB  | Precomputed similarity matrix        |

### 🔍 Why?
- GitHub restricts file uploads over **100 MB**
- These files can be **regenerated** from the notebook or **hosted externally**

---

## 📥 How to Set Up the Project Locally

1. **Clone the repository**

```bash
git clone https://github.com/your-username/movie-recommender-app-using-streamlit-and-tmdb-api.git
cd movie-recommender-app-using-streamlit-and-tmdb-api
```

2. **Install dependencies**

```bash
pip install -r requirements.txt
```

> If `requirements.txt` is not available, install manually:

```bash
pip install streamlit pandas requests
```

3. **Add Missing Files**

- Either **run the notebook** to generate `movies_dict.pkl` and `similarity.pkl`
- Or **download from an external link** (e.g., Google Drive, Hugging Face)

4. **Run the app**

```bash
streamlit run app.py
```

---

## 🔑 TMDB API Key

The app uses a free TMDB API key to fetch posters. If you plan to use your own key:

1. Sign up at [TMDB](https://www.themoviedb.org/)
2. Get your API key from your account settings
3. Replace the API key in the `fetch_poster()` function inside `app.py`

---

## ✅ Features

- Fast recommendations based on content similarity
- Real-time movie poster fetching
- Clean UI built with Streamlit
- Modular, beginner-friendly codebase

---

## 🙌 Acknowledgements

- [TMDB API](https://www.themoviedb.org/documentation/api)
- [Streamlit](https://streamlit.io/)
- Open-source Python & Machine Learning community

---

## 📜 License

This project is open-source and free to use under the [MIT License](LICENSE).
