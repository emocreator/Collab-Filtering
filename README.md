# Collaborative Filtering Movie Recommender

This project implements a simple collaborative filtering movie recommender system using dummy user ratings data.

## Files

The main files are:

- Collaborative Filtering Dummy Dataset.ipynb - Jupyter notebook with the implementation
- toy_dataset.csv - Sample user ratings data 

## Approach

The recommender follows these steps:

1. Load user ratings data
2. Standardize the ratings data
3. Calculate similarity between movies using cosine similarity of rating vectors 
4. For a user, find similar movies based on their past highly rated movies

## Usage

To get recommendations for a user:

```python
user_preferences = [("Movie1", 5), ("Movie2", 4)] 

similar_scores = pd.DataFrame()

for movie, rating in user_preferences:
   similar_scores = similar_scores.append(get_similar(movie, rating))
   
print(similar_scores.sum().sort_values(descending=True))
```

This will print movies similar to the user's specified liked movies.
