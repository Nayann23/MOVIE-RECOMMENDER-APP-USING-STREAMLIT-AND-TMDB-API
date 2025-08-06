# 🎬 MOVIE RECOMMENDER APP USING STREAMLIT AND TMDB API

A **content-based movie recommendation system** built with **Python**, **Streamlit**, and the **TMDB API**. This app suggests similar movies based on content similarity and dynamically fetches movie posters.

---

## 🚀 Project Overview

This app leverages:
- A **precomputed similarity matrix** to find content-based matches between movies
- **Streamlit** to provide a quick and interactive user interface
- **TMDB API** to fetch real-time movie posters for recommendations

Upon selecting a movie, the app displays **5 similar movies** along with their **poster images** fetched dynamically.

---

## 🧠 How It Works

1. Preprocessing merges metadata features such as genres, keywords, overview, cast, and crew.
2. A **cosine similarity matrix** is computed from the combined feature set.
3. The app uses this matrix to retrieve the 5 most similar movies (excluding the selected one).
4. Poster images for recommendations are fetched using the **TMDB API**.
5. All content is displayed using **Streamlit columns**, offering a clean UI.

---

## 📁 Repository Structure

```
MOVIE-RECOMMENDER-APP-USING-STREAMLIT-AND-TMDB-API/
├── app.py                  # Main Streamlit application
├── recommendation.ipynb    # Notebook to preprocess data and build the similarity matrix
├── README.md               # This documentation
├── requirements.txt        # Dependency list (optional)
```

---

## ⚠️ Large Files Omitted

To keep the repo lightweight and within GitHub’s limits, the following files **are NOT included**:

| File Name          | Size     | Description                          |
|--------------------|----------|--------------------------------------|
| `movies_dict.pkl`  | ~43 MB   | Contains movie metadata              |
| `similarity.pkl`   | ~174 MB  | Precomputed cosine similarity matrix |

**Why exclude them?**
- GitHub imposes a **100 MB** file size limit per file.
- These files can be regenerated via the notebook or downloaded externally.

---

## 📥 Setup Instructions

1. **Clone the repository**  
```bash
git clone https://github.com/Nayann23/MOVIE-RECOMMENDER-APP-USING-STREAMLIT-AND-TMDB-API.git
cd MOVIE-RECOMMENDER-APP-USING-STREAMLIT-AND-TMDB-API
```

2. **Install dependencies**  
```bash
pip install -r requirements.txt
```  
If `requirements.txt` is unavailable:  
```bash
pip install streamlit pandas requests
```

3. **Obtain missing files**  
- Run `recommendation.ipynb` to generate `movies_dict.pkl` and `similarity.pkl`, **or**  
- Download them from an external link (e.g. Google Drive, Hugging Face)

4. **Place the `.pkl` files** in the same folder as `app.py`.

5. **Run the app**  
```bash
streamlit run app.py
```

---

## 🔑 TMDB API Key Configuration

The app uses TMDB API to fetch movie posters. To use your own API key:
1. Register at https://www.themoviedb.org/ and generate an API key.
2. Replace the existing key in the `fetch_poster()` function inside `app.py`.

---

## ✅ Features

- Content-based recommendation of top 5 similar movies
- Real-time movie poster display via TMDB
- Clean, responsive UI using Streamlit
- Modular structure for ease of understanding and modification

---

## 🌱 Future Enhancements

- Include movie overviews, ratings, and release date
- Add filtering by genre or year
- Incorporate collaborative filtering or hybrid recommendation models
- Enhance UI with improved layout or animations
- Deploy on platforms like Streamlit Cloud or Hugging Face Spaces

---

## 🙌 Acknowledgements

- **TMDB API** for metadata and poster images  
- **Streamlit** for rapid UI prototyping  
- **Python**, **Pandas**, **Scikit-learn**, and the open-source ML community

---

## 📜 License

Project is open-source under the **MIT License**. See the `LICENSE` file for details.
