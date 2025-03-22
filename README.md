# TMDB-Movie-Recommendation-System

![Screenshot 2025-03-22 234909](https://github.com/user-attachments/assets/835cb04c-46ef-48a8-b1d2-f34271d11d60)

# Overview

This project builds a movie recommendation system using the TMDB dataset containing over 930,000 (640,000 after preprocessing) movies. The system focuses on content-based filtering, utilizing movie metadata such as genres, production companies, and release information. It leverages efficient Euclidean similarity search techniques, sparse matrix vector indexing, and fuzzy string matching to provide personalized movie recommendations based on similarity.

# Key Features

**Dataset:**

TMDB movie dataset (2023) containing metadata like titles, genres, release dates, popularity, etc.

https://www.kaggle.com/datasets/asaniczka/tmdb-movies-dataset-2023-930k-movies/data

**Preprocessing:**

* Cleans unnecessary columns and focuses on relevant metadata.

* Processes multi-valued fields like genres using multi-label binarization.

* Column selection only key columns from the TMDB dataset are retained to reduce noise, including attributes like title, vote_average, etc...

* Missing value handling movies missing titles are dropped.

* For multi-valued fields like genres, any missing entries are filled with an unknown label to maintain consistency.

**Similarity Calculation:**

* Uses FAISS (Facebook AI Similarity Search) to perform efficient similarity searches on movie features.

* Employs FAISS indexing using Euclidean (L2) distance for scalable nearest neighbor search.

**Fuzzy Matching:**

* Implements FuzzyWuzzy to handle non-exact title matches, ensuring robust querying.

**Recommendation Generation:**

* Retrieves top-N (10) similar movies based on features similarity.

**Technologies Used:**

* Python,Pandas,NumPy,FAISS,FuzzyWuzzy,Scikit-learn,Matplotlib,Seaborn,KaggleHub

![Screenshot 2025-03-22 234349](https://github.com/user-attachments/assets/04a29703-1e3d-4364-9d15-e5740fd7095e)

