🎬 Movie Recommendation System — Item-Based Collaborative Filtering
This project implements an item-based collaborative filtering approach to recommend movies based on user ratings. It leverages the stability of movie features over time, making it ideal for periodic retraining. The system uses cosine similarity to identify similar movies and returns top recommendations for a given title.
📌 Why Item-Based Filtering?
- Movies don’t change often, so item-based filtering is more stable than user-based filtering.
- Requires less frequent retraining (e.g., weekly vs. daily).
- Scales better with large datasets due to sparsity optimization.
📁 Dataset
- movies.csv: Contains movie metadata (movieId, title, genres).
- ratings.csv: Contains user ratings (userId, movieId, rating).
🧠 Workflow Overview
- Data Loading & Exploration
- Load movie and rating datasets.
- Inspect structure and key features.
- Pivot Ratings Table
- Transform ratings into a matrix with movieId as rows and userId as columns.
- Fill missing values with 0.
- Filtering Criteria
- Keep movies rated by at least 10 users.
- Keep users who rated at least 50 movies.
- Sparsity Reduction
- Convert the filtered matrix to a compressed sparse row (CSR) format using scipy.
- Model Training
- Use NearestNeighbors from sklearn with cosine similarity.
- Fit the model on the sparse matrix.
- Recommendation Function
- Input: Partial or full movie title.
- Output: Top 10 similar movies with similarity scores.
🔍 Example Usage
get_movie_recommendation('Iron Man')
get_movie_recommendation('Memento')


📊 Visualization
- Scatter plots show:
- Number of users per movie.
- Number of movies rated per user.
- Threshold lines help filter noisy data.
⚙️ Technologies Used
- Python
- Pandas, NumPy
- Scikit-learn
- SciPy (CSR matrix)
- Matplotlib, Seaborn
🚀 How to Run
- Clone the repository.
- Place movies.csv and ratings.csv in a data/ folder.
- Run the notebook or script to train and test the recommender.
✅ Output
- Returns a DataFrame of recommended movies with similarity distances.
- Handles partial title matches and missing inputs gracefully.
📌 Notes
- Cosine similarity is preferred over Euclidean or Pearson for sparse data.
- Genres are not used in this filtering approach.
- For large datasets, CSR format significantly improves performance.
🙌 Acknowledgments
Inspired by collaborative filtering techniques and optimized for educational clarity and performance.

