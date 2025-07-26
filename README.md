# IMDB Movie Analysis Report

## Objective
The goal of this project is to analyze the IMDB Movies dataset to understand genre popularity, rating trends, and the factors that influence a movie's success. The insights derived will help IMDB better understand its content and audience.

---

## 1. Project Setup and Data Loading

### Libraries Used
- **Pandas:** For data manipulation and analysis.
- **NumPy:** For numerical operations.
- **Matplotlib & Seaborn:** For data visualization.

### Initial Data Exploration
- The dataset was loaded into a Pandas DataFrame.
- **Shape of the dataset:** (10178, 12)  
  This means the dataset contains *10,178 rows* (movies) and *12 columns* (attributes).

---

## 2. Data Overview and Basic Exploration

### Data Structure
- The `.info()` method revealed that the `genre` and `crew` columns had missing values.
- The `date_x` column was of type `object`, needing conversion to `datetime`.

### Statistical Summary
- The `.describe()` method provided the following insights:
  - **Score:** The average movie score is 63.5, with a median of 65.
  - **Budget:** The average budget is approximately $65 million.
  - **Revenue:** The average revenue is approximately $253 million.

---

## 3. Data Cleaning

- **Missing Values:** Rows with missing `genre` or `date_x` were dropped. Missing `score` values were filled with the median.
- **Data Types:** The `date_x` column was converted to a `datetime` object to enable time-based analysis.
- **Feature Engineering:**  
  - `release_year` and `release_decade` columns were created from the `date_x` column.  
  - The `genre` column was split to handle movies with multiple genres.

---

## 4. Univariate Analysis

### Most Common Genres
- Drama, Comedy, and Action are the most frequent genres in the dataset.

---

## 5. Bivariate Analysis

### How do ratings vary by genre?
- History, War, and Animation movies tend to receive higher and more consistent ratings.
- Horror shows a much wider variance in scores.

### Is there a correlation between budget and revenue?
- Yes, a moderately strong positive correlation of 0.68 exists.
- Higher budget movies tend to have higher revenues.

---

## 6. Genre-Specific Analysis

### Which genre has the highest average rating?
- History has the highest average rating, followed closely by War and Animation.

### How does the popularity of genres vary over time?
- The number of movies released has increased across almost all genres, especially in recent years.

---

## 7. Year and Trend Analysis

### How has the average movie rating changed over the years?
- The average movie rating has seen fluctuations over the years but remained relatively stable without a distinct long-term trend.

### Which years had the highest and lowest number of movie releases?
- **Highest:** 2022  
- **Lowest:** 1903

---

## 8. Multivariate Analysis

### Which genres are most popular in each decade?
- Drama and Comedy have consistently been the most popular genres across different decades.

### Relationships between Budget, Revenue, and Score
- The heatmap confirms the strong positive correlation between budget and revenue.
- Correlations between score and budget/revenue are much weaker, indicating that financial success doesn't always equate to critical acclaim.

---

## 9. Insights and Summary

- **Dominant Genres:** Drama, Comedy, and Action are the most produced and likely most-watched genres, showing sustained market demand.
- **Budget vs. Quality:** While a larger budget often leads to higher revenue, it does not guarantee a higher rating. Movie quality (score) is influenced by factors beyond just the budget.
- **Industry Growth:** The film industry has seen exponential growth in the number of movies released annually, especially in the 21st century.

---

## 10. Further Exploration

- Analyze the impact of specific directors or actors on a movie's financial and critical success.
- Investigate how the country of origin affects movie performance.
- Use Natural Language Processing (NLP) on the `overview` column to analyze plot summaries and their relationship to genre and ratings.
