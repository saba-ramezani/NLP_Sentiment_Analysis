# Sentiment Analysis of Movie Reviews using VADER

This project applies **VADER Sentiment Analysis** to movie reviews, focusing on extracting overall sentiment polarity from the textual descriptions of films. The analysis categorizes reviews into **positive, negative, or neutral** sentiments and identifies the most positive and negative movies.

---

## Dataset

- **File**: `movie_reviews.csv`  
- **Size**: 166 rows, 10 columns  
- **Columns**:  
  - `movie_title`: Title of the movie  
  - `rating`: Audience rating  
  - `genre`: Movie genre(s)  
  - `in_theaters_date`: Release date  
  - `movie_info`: Textual description of the movie  
  - `directors`: Director(s) of the movie  
  - `director_gender`: Gender of the director(s)  
  - `tomatometer_rating`: Critics' score  
  - `audience_rating`: Audience score  
  - `critics_consensus`: Critics’ summary  

---

## Methodology

1. **Sentiment Analysis Tool**: [VADER Sentiment Analyzer](https://github.com/cjhutto/vaderSentiment)  
   - Calculates polarity scores (`pos`, `neu`, `neg`) and a **compound score**.  
   - Compound score ranges from `-1` (most negative) to `+1` (most positive).  

2. **Pipeline**:
   - Extracted sentiment scores for each `movie_info`.  
   - Classified reviews as **positive**, **negative**, or **neutral** based on compound scores.  
   - Ranked movies to identify the **Top 10 Most Positive** and **Top 10 Most Negative**.  

---

## Results

### Sentiment Distribution
A pie chart summarizing the proportions of positive, negative, and neutral reviews:  

<img width="455" height="409" alt="image" src="https://github.com/user-attachments/assets/b6626a9f-6e29-42ca-a5bc-38eaf4091b7d" />


- **Positive**: 92 movies (≈55%)  
- **Negative**: 74 movies (≈45%)  
- **Neutral**: 0 movies (0%)  

---

### Most Positive Movies
The top 10 movies with the highest compound sentiment scores were identified as strongly **positive**, reflecting uplifting or joyful narratives.  
<img width="978" height="657" alt="image" src="https://github.com/user-attachments/assets/bcd7d085-a50d-4dd1-a553-352d0e792c14" />


---

### Most Negative Movies
The top 10 movies with the lowest compound sentiment scores were identified as strongly **negative**, reflecting darker or more somber narratives.  
<img width="975" height="683" alt="image" src="https://github.com/user-attachments/assets/59a361b7-5acb-41de-9601-32abf18015c9" />


---

## Key Observations

- The dataset contains **no neutral reviews** — each description leaned either positive or negative.  
- A slight majority of movies (≈55%) were classified as positive.  
- VADER effectively captures sentiment polarity even in relatively short movie descriptions.  

---

## Output

- Final dataset with sentiment scores saved as:  
  `movie_reviews_with_sentiment.pkl`  

---

## Conclusion

This project demonstrates how **lexicon-based sentiment analysis (VADER)** can provide quick, interpretable insights into text-heavy datasets. While simple, VADER is effective for datasets with short and informal text (like movie descriptions).  

Potential extensions include:  
- Comparing results with transformer-based models (e.g., BERT).  
- Incorporating critics’ and audience ratings for multi-modal sentiment analysis.  
