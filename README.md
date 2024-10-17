# 🎬 Movie Recommendation System

This project is a **Content-Based Movie Recommendation System** that suggests movies similar to the one a user likes. By analyzing key features of the movies, such as the **overview** and **genre**, the model recommends similar films using **cosine similarity** on textual data.

## ✨ Features
- Recommends movies based on their **overview** and **genre**.
- Uses **CountVectorizer** to convert textual data into numerical vectors.
- Calculates **cosine similarity** between movies to find the most similar ones.
- Efficiently handles large datasets with **10000+ features**.
- Allows users to retrieve the **top 5 movie recommendations** based on any movie they choose.

## 🛠️ Libraries Used
- `Pandas` for data manipulation
- `Scikit-learn` for feature extraction and similarity calculation
- `Pickle` for model and data serialization

## 📂 Data
The dataset used in this project contains movie details including their:
- **ID**
- **Title**
- **Overview**
- **Genre**

### 📑 Selected Features:
- **ID**: Unique identifier for the movie.
- **Title**: The name of the movie.
- **Overview**: A brief description of the movie plot.
- **Genre**: The movie's genre.

### 🔀 Feature Engineering:
The **tags** feature is created by combining the **overview** and **genre** columns to generate more insightful textual data for similarity calculation.

## ⚙️ How It Works

1. **Data Preprocessing**:
    - Null values are handled, and only the required columns (`id`, `title`, `overview`, and `genre`) are selected.
    - A new column **tags** is created by combining **overview** and **genre**.

2. **Vectorization**:
    - The **CountVectorizer** is used to convert the textual **tags** into numerical vectors. A maximum of **10000 features** is extracted, and **stop words** (common English words) are removed to improve relevance.

3. **Similarity Calculation**:
    - The **cosine similarity** metric is computed between the movies based on their vectorized data, helping identify the movies that are closest in context to one another.

4. **Movie Recommendation**:
    - Based on a selected movie, the system calculates the top 5 most similar movies and returns them as recommendations.

## 📊 Visualization

The movie similarity is calculated using a matrix where each movie is compared with every other movie using cosine similarity. The higher the score, the more similar the movies are.

## 🚀 Getting Started

### Prerequisites
- Python 3.x
- Install the required libraries using:

```bash
pip install pandas scikit-learn
