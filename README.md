# Content-Based Movie Recommender System with Sentiment Analysis using AJAX

### Python Framework | Frontend | API

Updated version of this application can be found at: [The-Movie-Cinema](https://github.com/kishan0725/The-Movie-Cinema)

## Overview

This project implements a **Content-Based Recommender System** that recommends movies similar to the ones a user likes. Additionally, it analyzes sentiments on reviews provided by the user for that particular movie.

The movie details (title, genre, runtime, rating, poster, etc.) are fetched via the **TMDB API** ([The Movie Database API](https://www.themoviedb.org/documentation/api)). Using the movie's IMDB ID, the project performs **web scraping** using **BeautifulSoup4** to obtain user reviews from the IMDB site. Sentiment analysis is then performed on these reviews.

### Demo

Watch a demonstration on YouTube: [YouTube Demo](https://www.youtube.com/watch?v=dhVePtyECFw)

## The Movie Cinema

A similar application, **"The Movie Cinema,"** supports multi-language movies. Unlike this project, it uses the TMDB's recommendation engine. The recommendation part developed in this application doesn’t support multi-language movies, as generating the Count Vectorizer matrix for over 700,000 movies in TMDB consumes excessive RAM (200% even on Heroku).

Check out **"The Movie Cinema"** here: [The Movie Cinema Application](https://tmc.kishanlal.dev/)

Don’t worry if your movie isn’t auto-suggested. Just type the movie name and hit "enter" – it works even with typos.

### Source Code

- **GitHub Repository:** [The Movie Cinema Source Code](https://github.com/kishan0725/The-Movie-Cinema)

## Featured in Krish’s Live Session

The project was featured in a live session by Krish on YouTube.

## Getting Started

### How to Get the API Key?

1. Create an account at [TMDB](https://www.themoviedb.org/).
2. Navigate to the API section in your account settings.
3. Apply for an API key by filling in the required details. If asked for a website URL, you can enter "NA" if you don’t have one.
4. Once your request is approved, the API key will be visible in your API sidebar.

### How to Run the Project?

1. Clone or download this repository to your local machine.
2. Install the required libraries using: `pip install -r requirements.txt`
3. Get your API key from TMDB. (Refer to the steps above)
4. Replace `YOUR_API_KEY` in both places (line 15 and 29) of `static/recommend.js`.
5. Open a terminal or command prompt in your project directory and run the application with: `python main.py`.
6. Open your browser and navigate to: `http://127.0.0.1:5000/`.
7. That’s it! You’re ready to go.

## Architecture

### Similarity Score

The recommendation system relies on **similarity scores** to determine which items are most similar to the ones a user likes. This score ranges from 0 to 1, measuring the similarity between text details of different items. **Cosine similarity** is used to calculate these scores.

### How Cosine Similarity Works

Cosine similarity measures how similar documents are regardless of their size. It calculates the cosine of the angle between two vectors projected in a multi-dimensional space. Even if two similar documents are far apart in Euclidean distance, they may still be oriented closely together. The smaller the angle, the higher the cosine similarity.

For more on Cosine Similarity: [Understanding the Math behind Cosine Similarity](#)

## Datasets Used

- IMDB 5000 Movie Dataset
- The Movies Dataset
- List of Movies (2018, 2019, 2020)

---

**Star History**

Check the star history for this project here: [Star History Chart](#)

