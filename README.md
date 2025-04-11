# 🎬 Amazon Prime Video Content Analysis

A data-driven analysis of Amazon Prime Video's content library in the United States using publicly available metadata. The project explores trends in content types, genres, popularity, ratings, and regional production to derive actionable insights for strategic decision-making in the streaming industry.

---

## 📌 Project Objectives

This project aims to:
- Analyze the diversity and distribution of content on Amazon Prime Video
- Understand trends over time in content releases and audience engagement
- Explore the relationship between content attributes and popularity/ratings
- Provide business recommendations based on data-driven insights

---

## 📁 Dataset Overview

This project uses two CSV files:

### **1. titles.csv**  
Contains metadata for 9,871 Amazon Prime titles:
- `id`: Unique identifier
- `title`: Name of the movie/show
- `type`: 'MOVIE' or 'SHOW'
- `description`: Short plot summary
- `release_year`: Year of release
- `age_certification`: Rating (e.g., PG-13, R)
- `runtime`: Duration in minutes
- `genres`: List of genres (as strings)
- `production_countries`: List of countries
- `seasons`: Number of seasons (for shows)
- `imdb_id`: IMDb identifier
- `imdb_score`, `imdb_votes`: IMDb metrics
- `tmdb_score`, `tmdb_popularity`: TMDB metrics

### **2. credits.csv**  
Contains 124,000+ records of actors/directors:
- `person_id`: Unique person identifier
- `id`: Title ID (foreign key)
- `name`: Actor or director name
- `character`: Character name (if actor)
- `role`: ACTOR or DIRECTOR

---

## 🧹 Data Wrangling Summary

- Handled missing values across all columns (e.g., filled age ratings, scores, characters).
- Converted list-like columns (`genres`, `production_countries`) from string to Python lists.
- Created new features like `decade`, `is_show`.
- Removed duplicates and normalized text formatting.
- Merged datasets for combined content + cast analysis.

---

## 📊 Exploratory Data Analysis (EDA)

Visualizations include:

- 📈 Line plot of content released per year
- 📊 Genre distribution (bar chart)
- 🥧 Content type share (pie chart)
- 📉 IMDb and TMDB score distributions (boxplot, violin plot)
- 🔥 Top-rated and most popular titles (lollipop chart)
- 🌍 Top 10 production countries (bar chart)
- 🎭 Age certification counts
- 🔄 Correlation heatmap and pairplot
- 👨‍💼 Top 10 directors by content count

---

## 🔍 Key Insights

- **Drama, Comedy, and Action** are the most dominant genres.
- A significant growth in content began post-2015.
- IMDb and TMDB ratings are generally moderate (avg ~6.0), with a few outliers.
- Most content is **movie-based** (~85%).
- The **USA, UK, and India** are top-producing countries.
- A small number of directors and actors appear repeatedly — hinting at strong content partnerships.

---

## 🧠 Business Recommendations

- Invest more in top-performing genres and high-rated content.
- Expand regional content creation, especially in India and Latin America.
- Improve visibility of top-rated but less popular titles.
- Use age certification segmentation for content hubs (family, mature, teen).
- Leverage high-performing directors and actors for future projects.

---

## 📂 Project Structure

