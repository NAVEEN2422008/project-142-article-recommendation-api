# C142 Article Recommendation API

A Flask-based article recommendation backend that serves news articles with like/dislike interaction and two recommendation strategies.

## Features
- `/get-articles` — returns the next article from the loaded dataset
- `/liked-articles` / `/disliked-articles` — record user feedback by moving the current article
- `/popular-articles` — demographic/top 20 popular articles by total events
- `/recommended-articles` — content-based recommendations built from liked articles

## Tech Stack
- Python
- Flask
- scikit-learn (CountVectorizer + cosine similarity)
- pandas, numpy
- CSV article dataset

## Project Structure
```
c142/
├── main.py                  # Flask routes
├── storage.py               # loads all_articles, liked/disliked lists
├── demographic_filtering.py # popular-articles logic
├── content_filtering.py     # cosine-similarity recommendations
├── articles.csv             # article dataset
└── README.md
```

## Installation
```
pip install flask pandas numpy scikit-learn
```

## Usage
```
python main.py
```
The Flask dev server starts (default port 5000). Interact via the HTTP routes above.