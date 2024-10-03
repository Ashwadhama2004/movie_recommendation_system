# movie_recommendation_system

Here’s a **funky** README for your **Movie Recommendation System** project, following a similar style:

---

# 🎬 Movie Recommendation System 🍿

Welcome to the **Movie Recommendation System**! 🎉 This project uses the magic of machine learning ✨ and cosine similarity 🧠 to recommend movies that match your tastes! Whether you're into action, romance, or sci-fi, we've got you covered! 🍕🎥

---

## 🎥 Project Overview

We’ve built a cool movie recommender system based on the movie metadata, like **genres**, **cast**, **crew**, and more! 🕵️‍♀️ We analyze movies and suggest similar ones using some data crunching and text vectorization magic 🧙‍♂️. All you have to do is tell us your favorite movie, and we'll show you others that you'll love!

### 📊 Dataset Features

Our dataset includes:

- **Title**: The name of the movie 🎞️
- **Genres**: Action, Comedy, Drama, etc. 🎭
- **Cast & Crew**: The amazing actors and directors behind your favorite films 🎬
- **Overview**: A brief plot summary 📝
- **Keywords**: Important themes or concepts 🔑

---

## 🛠️ How It Works

We use the **TF-IDF Vectorizer** to convert movie metadata into vectors (fancy math stuff 🧠), and then calculate the **cosine similarity** between the vectors to suggest similar movies. In other words, we find movies that are close to each other in terms of the data and recommend them!

---

## 🚀 How to Run the Project

Want to recommend some movies? Follow these simple steps:

### Prerequisites

First, you need to install the necessary Python libraries. You can do this by running:

```bash
pip install numpy pandas scikit-learn difflib
```

### Step-by-Step Guide

1. **Clone the Repo**: Download this project to your computer:

```bash
git clone https://github.com/Ashwadhama2004/movie-recommendation-system.git
cd movie-recommendation-system
```

2. **Get the Dataset**: The dataset (`movies.csv`) is already in the project, so you’re good to go! 🎉

3. **Run the Code**: You can run this project via a Jupyter notebook:

```bash
jupyter notebook movie_recommendation.ipynb
```

Or, if you're in a hurry, just run the Python script directly 🏃‍♂️:

```bash
python movie_recommendation.py
```

---

## 🔮 What’s Inside the Code?

Here's a breakdown of the steps inside the code:

1. **Data Preprocessing**:
   - We replace missing data with empty strings 🧼 so everything runs smoothly.
   - Combine relevant features like **genres**, **keywords**, **cast**, **crew**, and **overview** into one big text field. 🎩

2. **Vectorization**:
   - Use **TF-IDF** (Term Frequency-Inverse Document Frequency) to transform text data into numerical vectors so we can calculate similarity between movies.

3. **Cosine Similarity**:
   - Measure the **cosine similarity** between the movies to find out which ones are the most similar. The closer the angle, the more similar the movies are! 📐

4. **Movie Recommendations**:
   - When a user inputs their favorite movie, we find the closest match using **difflib** and recommend up to 20 similar movies! 🎉

---

## 🏆 Sample Prediction

Wanna try it out? Here's an example:

```python
movie_name = "The Matrix"
list_of_movies = dataset['title'].tolist()

# Get the closest match and recommend similar movies
close_match = difflib.get_close_matches(movie_name, list_of_movies)[0]
index_of_movie = dataset[dataset.title == close_match]['index'].values[0]

# Get recommended movies based on cosine similarity
similar_movies = sorted(list(enumerate(similarity[index_of_movie])), key=lambda x: x[1], reverse=True)

# Print the top 5 recommendations
for i, movie in enumerate(similar_movies[1:6]):
    print(f"{i+1}. {dataset.iloc[movie[0]]['title']}")
```

Output:
```
1. The Matrix Reloaded
2. The Matrix Revolutions
3. Inception
4. Terminator 2: Judgment Day
5. The Dark Knight
```

---

## 📈 Results

Our model successfully recommends similar movies based on user input. Test it out with different movie titles and see what comes up! 🌟

---

## 💡 Future Enhancements

Wanna make it even better? Here are some ideas:
- **Incorporate Ratings**: Suggest movies based on user ratings for a more personalized experience.
- **Use Collaborative Filtering**: Implement a recommendation system based on user preferences and behavior.
- **Try Deep Learning**: Experiment with neural networks for more advanced recommendations.

---

## 🛠️ Tech Stack

- **Language**: Python 🐍
- **Libraries**: `numpy`, `pandas`, `scikit-learn`, `difflib`
- **Jupyter Notebook**: For interactive development and data analysis.

---

## 📜 License

This project is licensed under the MIT License. Check the [LICENSE](LICENSE) file for more details.

---

## 👋 Connect with Me

Got questions or suggestions? Let’s connect!

- GitHub: [Ashwadhama2004](https://github.com/Ashwadhama2004)

---

Thanks for checking out my **Movie Recommendation System**! Enjoy finding new movies to watch! 🎬 🍿 😊

``` 
