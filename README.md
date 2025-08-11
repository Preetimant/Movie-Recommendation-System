# Movie Recommendation System

This **Python-based movie recommendation system** uses both **content-based filtering** and **collaborative filtering** to suggest films tailored to user preferences. It is built on the [MovieLens dataset](https://grouplens.org/datasets/movielens/), incorporating movie metadata, user ratings, and tags to predict preferences.

---

## **Core Features**
1. **Content-Based Filtering**:
   - Uses **TF-IDF vectorization** on movie tags and genres to numerically represent textual metadata.
   - Computes **cosine similarity** between movies based on tags and genres to recommend similar titles.

2. **Collaborative Filtering**:
   - Builds a **user–item ratings matrix** from user ratings.
   - Uses cosine similarity to find users with similar tastes.
   - Recommends movies enjoyed by similar users that the current user has not yet rated.

3. **Visualizations**:
   - Most popular genres.
   - Top 10 most-rated movies.
   - Top-rated movies (≥100 ratings).
   - Most common tags (by TF-IDF sum).
   - Individual user preferences by genre.

4. **Interactive Recommendation Functions**:
   - Recommend top movies for a given user.
   - Suggest movies based on similar users (**collaborative**).
   - Recommend movies similar to a given title (**content-based**).
   - Modular design for easy experimentation and extension.

---

## **Workflow**

1. **Data Loading**:
   - Imports movies, ratings, and tags datasets; merges and preprocesses data.

2. **Preprocessing**
   - Aggregates and cleans tags/genres.
   - Builds matrices required for both filtering approaches.

3. **Similarity Matrices**
   - Generates cosine similarity matrices for:
     - Tags (content-based)
     - Genres (content-based)
     - Users (collaborative filtering)

4. **Recommendation Execution**:
   - Enter a `user_id` to:
     - See top movies rated by that user.
     - Get collaborative recommendations.
     - Get content-based recommendations.
     - View the user’s genre preferences.

---

## **Components**
- `get_recommendations_by_movie()` → Content-based recommendations by tags/genres.
- `get_user_recommendations()` → Collaborative recommendations from the user’s own ratings.
- `get_user_user_recommendations()` → Collaborative recommendations from similar users’ ratings.
- `plot_*` functions → Generate dataset and user-specific visualizations.

---

## **Usage Example**
1. **Upload Dataset or Update Paths**:
   - In Google Colab or local Jupyter Notebook, upload the dataset or adjust file paths in the code.
2. **Run the Notebook**:
   - Execute all cells to preprocess and build the recommendation system.
3. **Enter a User ID**:
   - View top rated movies.
   - See content-based and collaborative recommendations.
   - Visualize genre preferences.

---
