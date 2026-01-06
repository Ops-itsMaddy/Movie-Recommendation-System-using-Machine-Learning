# Movie Recommendation System using Machine Learning

A Content-Based Movie Recommendation System built with Python. This system suggests movies to users by calculating the similarity between their favorite movies and others in the dataset using natural language processing (NLP) techniques.

## 📌 Project Overview
The system utilizes a "Content-Based" approach, focusing on movie metadata such as genres, keywords, taglines, cast, and directors to find similarities. It transforms text data into numerical vectors to identify which movies are most closely related to a user's input.

## 📊 Dataset Features
The model processes a dataset of movies with the following key attributes used for recommendations:
* **Genres**: The category of the movie (e.g., Action, Sci-Fi).
* **Keywords**: Specific themes or topics associated with the movie.
* **Tagline**: The promotional catchphrase of the movie.
* **Cast**: The lead actors in the film.
* **Director**: The person who directed the movie.

## 🛠️ Project Workflow
1.  **Data Preprocessing**: Handling null values by replacing them with empty strings to ensure the vectorizer functions correctly.
2.  **Feature Engineering**: Combining selected text features (genres, keywords, etc.) into a single combined string for each movie.
3.  **Vectorization**: Using `TfidfVectorizer` from Scikit-Learn to convert the combined text data into feature vectors.
4.  **Similarity Calculation**: Applying **Cosine Similarity** to compute the similarity score between all movie vectors.
5.  **Recommendation Engine**: 
    * User inputs their favorite movie name.
    * The system finds the closest match using `difflib`.
    * It retrieves a list of similar movies based on the highest similarity scores.

## 🚀 How to Run
1.  **Clone the repository** and ensure you have the movie dataset (e.g., `movies.csv`) in the same directory.
2.  **Install Dependencies**:
    ```bash
    pip install -r requirements.txt
    ```
3.  **Execute the Notebook**: Open `Movie Recommendation System using Machine Learning.ipynb` in Jupyter or Google Colab and run all cells.

## 🎬 Example Output
When a user enters a movie like "Iron Man", the system analyzes the similarity scores and outputs a ranked list of movies such as:
1. Iron Man 2
2. Iron Man 3
3. Avengers: Age of Ultron
... and so on.