# 🎮 Content-Based Game Recommendation System
This project, developed for a Machine Learning course in my 3rd-semester, focuses on building a **game recommendation system**. The goal is to help users discover new games they might like based on the attributes of games they already enjoy.

This system utilizes a **content-based filtering** approach. Unlike collaborative filtering, which relies on user ratings, this method recommends games by analyzing their inherent features. It identifies similarities between games based on a combination of their metadata, including genre, platform, publisher, developer, and even sales data.

---

### ⚙️ Methodology
1. Combined Feature Creation
* To create a rich profile for each game, the key features listed above were combined into a single string. This approach allows the model to find similarities across a wide range of game attributes.
2. Vectorization with TF-IDF
* The combined feature text for each game was transformed into numerical vectors using the **TF-IDF (Term Frequency-Inverse Document Frequency)** technique. TF-IDF evaluates how relevant a term (e.g., a specific genre, developer, or platform) is to a game within the entire dataset. This step converts the mixed feature data into a quantitative format that can be measured for similarity.
3. Similarity Measurement with Cosine Similarity
* To determine how "similar" two games are, **Cosine Similarity** was calculated between all TF-IDF vectors. This generated a similarity matrix containing a score between 0 (not similar) and 1 (identical) for every pair of games in the dataset.
4. Recommendation Logic
A function was created to generate recommendations. When a user provides a game title:
* The system finds the game in the dataset.
* It retrieves the pre-computed cosine similarity scores for that game against all other games.
* It sorts these scores in descending order.
* Finally, it returns the **top 5 games** with the highest similarity scores as recommendations.

---

## 🛠️ Concepts
* **Language:** Python
* **Core Concepts:**
    * Recommender Systems
    * Content-Based Filtering
    * TF-IDF (Term Frequency-Inverse Document Frequency)
    * Cosine Similarity

---

### 🖋 Author
Laurel Evelina Widjaja
