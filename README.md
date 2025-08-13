# TMDB_Movie_Recommendation_Engine

## Project Overview
This project focuses on collecting, cleaning, and preparing a dataset of movies fetched via the **TMDB** and **YTS APIs** using Python.
The dataset contains essential movie metadata such as title, year, IMDb rating, runtime, genres, language, summary, and direct YTS links.

The goal of this project is to make the dataset ready for machine learning applications, especially movie recommendation engines (content-based, collaborative, or hybrid).
Key preprocessing steps included:

  -> Removing duplicates.
  -> Handling missing values in genres, language, runtime, and ratings.
**It can also be used for:**
  -> Predicting movie ratings.
  -> Identifying trends in genres and languages.
  -> Creating interactive dashboards for movie exploration.


## Potential Use Cases
  ->**Recommendation Engines** – Content-based, collaborative, or hybrid models.
  -> **Data Analysis** – Rating trends, popular genres, language distribution.

## Data Cleaning Performed
  -> Removed **31 duplicate rows**.
  -> Handled **missing values**:
  -> Filled missing Genres and Language with Unknown.
  -> Standardized column formats.


# Top 5 genres by count
df['Genres'].value_counts().head()

# Average rating by genre
df.groupby('Genres')['Rating'].mean().sort_values(ascending=False)
