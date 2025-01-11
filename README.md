# Steam-Game-recommendation-Engine
================================
This project implements a recommendation engine for Steam games using
collaborative filtering (ALS),
content-based filtering (TF-IDF), and graph-based analysis with NetworkX.
Features:
---------
1. Collaborative Filtering: Recommends games based on user gameplay
history.
2. Content-Based Filtering: Suggests similar games using game title
metadata.
3. Graph-Based Analysis: Uses NetworkX to visualize and analyze
relationships between games and users.
Setup:
------
1. Prerequisites:
- Databricks environment with Spark enabled.
- Python libraries: PySpark, NumPy, Matplotlib, SciPy, NetworkX.
2. Datasets:
- Upload the following CSV files to `/FileStore/tables/` in your
Databricks workspace:
- games.csv
- users.csv
- recommendations_1.csv
Steps to Run:
-------------
1. Create a Databricks cluster and initialize a Spark session.
2. Load the datasets into Spark DataFrames from the provided paths.
3. Perform data preprocessing:
- Handle missing values.
- Tokenize game titles and compute TF-IDF.
- One-hot encode categorical features and scale numerical features.
4. Train a collaborative filtering model using ALS and generate
recommendations.
5. Calculate cosine similarity for content-based filtering to find
similar games.
6. Build and visualize graphs:
- Create a game similarity graph based on cosine similarity.
- Create a user-game interaction graph based on collaborative
filtering results.
7. Display results:
- Top 5 game recommendations for each user.
- Most similar games based on title metadata.
- Visualizations and graph metrics (e.g., centrality, communities).
Requirements:
-------------
See requirements.txt for a list of required libraries.
