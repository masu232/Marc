import pandas as pd

# Load the movie ratings dataset
df = pd.read_csv('movie_ratings.csv')

# Sample dataset:
# Movie            Genre      Rating     User
# Movie A          Action     4.5        User1
# Movie B          Drama      3.8        User2
# ...              ...        ...        ...

# Perform data preprocessing if required (e.g., handle missing values)

# Create a user-item matrix for collaborative filtering
user_item_matrix = df.pivot_table(index='User', columns='Movie', values='Rating')

# Define a function to get movie recommendations for a user
def get_movie_recommendations(user, num_recommendations=5):
    user_ratings = user_item_matrix.loc[user]
    similar_users = user_item_matrix.corrwith(user_ratings)
    similar_users = similar_users.dropna()
    similar_users.sort_values(ascending=False, inplace=True)

    # Filter out movies the user has already rated
    rated_movies = user_item_matrix.loc[user].dropna().index
    recommended_movies = []
    for similar_user, similarity_score in similar_users.iteritems():
        similar_user_rated = user_item_matrix.loc[similar_user].dropna().index
        new_movies = set(similar_user_rated) - set(rated_movies)
        recommended_movies.extend(new_movies)
        if len(recommended_movies) >= num_recommendations:
            break

    return recommended_movies[:num_recommendations]

# Example usage:
user = 'User1'
recommendations = get_movie_recommendations(user, num_recommendations=5)

# Print the recommended movies for the user
print(f"Movie recommendations for {user}:")
for i, movie in enumerate(recommendations, 1):
    print(f"{i}. {movie}")

