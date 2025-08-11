# TMDB_Movie_Recommendation_Engine

## 📌 Overview
This dataset is a collection of **4,800+ movies** retrieved from **TMDB** and **YTS APIs** using Python’s `requests` library.  
It contains detailed metadata for each movie, including title, release year, genres, primary language, IMDb rating, runtime, summary, and direct YTS links.  

The data has been **cleaned and preprocessed** to make it ready for analysis and machine learning tasks:
- Removed duplicates and standardized formats.
- Handled missing values in genres, languages, ratings, and runtimes.
- Ensured compatibility for recommendation system development.

This dataset is suitable for **content-based filtering**, **collaborative filtering**, and **hybrid recommendation engines**, as well as **exploratory data analysis** and **visualization**.

It can also be used for:
- Predicting movie ratings.
- Identifying trends in genres and languages.
- Creating interactive dashboards for movie exploration.

---

## 📂 Dataset Features

| Column Name        | Description |
|--------------------|-------------|
| **Title**          | Name of the movie |
| **Year**           | Year of release |
| **Rating**         | IMDb rating (0–10) |
| **Runtime (min)**  | Duration of the movie in minutes |
| **Genres**         | Movie genres (comma-separated) |
| **Language**       | Primary spoken language (ISO code) |
| **IMDb Code**      | Unique IMDb identifier |
| **Summary**        | Short description of the plot |
| **URL**            | YTS link with torrent info (if available) |

---

## 📊 Potential Use Cases
- 🎯 **Recommendation Engines** – Content-based, collaborative, or hybrid models.
- 📈 **Data Analysis** – Rating trends, popular genres, language distribution.
- 🛠 **Machine Learning Projects** – Clustering, classification, regression.
- 📉 **Visualization Dashboards** – Genre heatmaps, year-wise rating trends.

---

## 🛠 Data Cleaning Performed
- Removed **31 duplicate rows**.
- Handled **missing values**:
  - Filled missing `Genres` and `Language` with `"Unknown"`.
- Standardized column formats.

---

## 💡 Example Analysis
python
import pandas as pd

df = pd.read_csv("Movies_Metadata.csv")

# Top 5 genres by count
df['Genres'].value_counts().head()

# Average rating by genre
df.groupby('Genres')['Rating'].mean().sort_values(ascending=False)
