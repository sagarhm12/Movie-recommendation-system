# 🎬 Movie Recommender System

A simple **Content-Based Movie Recommendation System** built with **Python**, **Pandas**, **Scikit-learn**, and **Streamlit**. This application suggests similar movies based on user input using movie metadata like cast, genres, keywords, and crew.

## 🚀 Features

* Recommends 5 similar movies based on your selected input
* Uses **cosine similarity** on vectorized movie "tags"
* Built using **Streamlit** for a clean and interactive UI
* Preprocessed using **NLTK**, **Pandas**, and **Sklearn**
* Option to add TMDB API to fetch movie posters (currently commented)

---

## 📁 Dataset Used

* [TMDB 5000 Movies Dataset](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata)

Files:

* `tmdb_5000_movies.csv`
* `tmdb_5000_credits.csv`

---

## 🧠 How It Works

1. **Preprocessing**

   * Merges `movies` and `credits` datasets on title
   * Extracts and cleans relevant metadata: genres, keywords, cast (top 3), director
   * Combines all metadata into a single text string (`tags`)
   * Applies stemming using `PorterStemmer` from NLTK

2. **Vectorization**

   * Uses `CountVectorizer` to convert text into numerical vectors
   * Calculates **cosine similarity** between movie vectors

3. **Recommendation**

   * Finds the top 5 most similar movies based on cosine similarity

---

## 🖥️ Streamlit UI

* Built using `streamlit`
* Interactive dropdown to select a movie
* Click "Show Recommendation" to display 5 similar movies

---

## 📦 Requirements

Install dependencies using:

```bash
pip install -r requirements.txt
```

**`requirements.txt`**:

```txt
pandas
numpy
nltk
scikit-learn
streamlit
requests
```

---

## ▶️ Run the App

```bash
streamlit run app.py
```

Then open the link provided by Streamlit in your browser.

---

## 🔧 Optional: Enable Movie Posters

If you'd like to display movie posters using TMDB API:

1. Uncomment the `fetch_poster` function in `app.py`
2. Replace `"YOUR_API_KEY"` with your actual TMDB API key
3. Uncomment the `st.image()` lines in the columns

---

## 📌 File Structure

```
├── app.py                  # Streamlit app
├── tmdb_5000_movies.csv    # Movie metadata
├── tmdb_5000_credits.csv   # Cast and crew data
├── movie_list1.pkl         # Pickled DataFrame of processed movies
├── similarity1.pkl         # Pickled similarity matrix
├── README.md               # Project overview
```

---

## 🙋‍♂️ Author

**Sagar H M**

---

