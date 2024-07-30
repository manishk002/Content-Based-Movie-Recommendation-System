# Movie Recommendation System

This project implements a content-based movie recommendation system using machine learning techniques. It analyzes various features of movies such as genres, keywords, cast, and crew to suggest similar films based on user input.

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [Contributing](#contributing)
- [License](#license)

## Overview

In the age of streaming services and vast movie libraries, finding films that match a user's taste can be challenging. This movie recommendation system aims to solve this problem by suggesting movies similar to a given input film, based on content features rather than user ratings or behavior.

## Features

- Content-based movie recommendation
- Utilizes movie metadata including overview, genres, keywords, cast, and crew
- Text preprocessing and feature extraction using NLTK and scikit-learn
- Cosine similarity for finding movie similarities
- Easy-to-use recommendation function

## Installation

1. Clone this repository:
   ```
   git clone https://github.com/manishk002/Movie-Recommendation-System.git
   cd Movie-Recommendation-System
   ```

2. Install the required dependencies:
   ```
   pip install numpy pandas nltk scikit-learn
   ```

3. Download the necessary NLTK data:
   ```python
   import nltk
   nltk.download('punkt')
   ```

4. Ensure you have the dataset files (`tmdb_5000_movies.csv` and `tmdb_5000_credits.csv`) in the project directory.

## Usage

Run the script in a Python environment:

```python
python movie_recommendation_system.py
```

To get movie recommendations, use the `recommend` function:

```python
recommend('Spectre')
```

This will output a list of 5 movie recommendations similar to 'Spectre'.

## Dataset

The project uses the TMDB 5000 Movie Dataset, which includes two CSV files:
- `tmdb_5000_movies.csv`: Contains movie metadata
- `tmdb_5000_credits.csv`: Contains cast and crew information
- Dataset link:- https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata?select=tmdb_5000_movies.csv

Make sure these files are present in your project directory before running the script.

## Methodology

1. **Data Preprocessing**: 
   - Merge movie and credit data
   - Extract relevant features (overview, genres, keywords, cast, crew)
   - Clean and preprocess text data

2. **Feature Engineering**:
   - Convert list-like strings to actual lists
   - Combine all text features into a single 'tags' column

3. **Text Processing**:
   - Tokenization
   - Lowercasing
   - Stemming using Porter Stemmer

4. **Feature Extraction**:
   - Use CountVectorizer to convert text to a matrix of token counts

5. **Similarity Calculation**:
   - Compute cosine similarity between movies based on their feature vectors

6. **Recommendation**:
   - For a given movie, find the top 5 most similar movies based on cosine similarity scores

## Contributing

Contributions to improve the project are welcome. Please follow these steps:

1. Fork the repository
2. Create a new branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

Distributed under the MIT License. See `LICENSE` file for more information.

