# Movie Recommendation System

## Overview
Content-based movie recommendation system built on a dataset of 4,760 movies.
Given a movie you like, the system recommends the 30 most similar movies based 
on genre, keywords, cast, director, and tagline.

## How It Works
1. Selected 5 key text features per movie — genre, keywords, tagline, cast, director
2. Combined them into a single text representation per movie
3. Converted text to numerical vectors using TF-IDF
4. Measured similarity between all movies using Cosine Similarity
5. Returns top 30 most similar movies for any input

## Example Output
Input: *"Finding Nemo"*

Top recommendations: Forrest Gump, The Green Mile, Rain Man, 
Cast Away, Silver Linings Playbook...

## Why TF-IDF?
Movie features are text-based — genre, cast, keywords etc. Machine learning 
models only understand numbers. TF-IDF converts text into numerical vectors, 
giving higher weight to unique and meaningful words (like a specific director's 
name) and lower weight to common words that appear across many movies.

## Why Cosine Similarity?
After TF-IDF, every movie is represented as a numerical vector. Cosine 
Similarity measures the angle between two vectors — the smaller the angle, 
the more similar the movies. This finds the closest matching movies to 
any input title.

## Tools and Libraries
- Python
- pandas, numpy
- scikit-learn (TfidfVectorizer, cosine_similarity)
- difflib (fuzzy movie title matching)

## Key Skills Demonstrated
- Natural Language Processing (NLP) with TF-IDF
- Content-based filtering
- Cosine Similarity for recommendation ranking
- Fuzzy string matching for user input handling
- Working with real-world messy text data

## Dataset
4,760 movies with 21 features including genre, cast, keywords, 
budget, revenue, and director.
[YBI Foundation Dataset](https://raw.githubusercontent.com/YBI-Foundation/Dataset/main/Movies%20Recommendation.csv)
