# Book Recommender System
## View the Project
You can view the project here: [Book Recommender System on Render](https://book-recommeder-system.onrender.com/)


## Project Overview

The **Book Recommender System** is a web-based application built using Flask and Python that provides personalized book recommendations to users. The app utilizes machine learning models to suggest books based on user input, specifically focusing on content-based filtering. The system displays a list of popular books with ratings and authors, and allows users to search for similar books based on their chosen book.

This project uses multiple datasets containing book details, users, ratings, and similarity scores calculated using machine learning algorithms.

## Features

- **View Top 50 Popular Books**  
  Displays a list of the top 50 books based on user ratings and popularity. Shows details including the book's title, author, rating, and number of votes.

- **Get Book Recommendations**  
  Users can input the name of a book, and the system will provide 4 similar books based on content-based filtering. Each recommendation includes the book’s title, author, and an image of the book's cover.

- **Responsive Design**  
  The application is designed using Bootstrap, making it responsive and easy to use.

## Tech Stack

### Backend:
- **Flask**: A lightweight WSGI web application framework in Python, used to build the API and handle requests.
- **Python**: The primary programming language used for building the application and machine learning models.

### Frontend:
- **HTML**: The standard markup language used for structuring the web pages.
- **CSS**: Used to style the web pages, with Bootstrap for responsive layouts.

### Machine Learning:
- **Content-Based Filtering**: The recommendation engine uses content-based filtering to suggest books similar to a given book.
- **Pandas** and **NumPy**: Used for handling datasets and numerical operations.
- **Pickle**: Used for saving pre-trained machine learning models and datasets.

### Others:
- **Git LFS (Large File Storage)**: Used to handle large files, such as the books.pkl file which is large in size.
- **Gunicorn**: WSGI server for running the Flask application in production.

## How It Works

### Popular Books Page
When users visit the homepage (`/` route), they see a list of the top 50 books fetched from the `popular.pkl` dataset. Each book's title, author, number of votes, and average rating are displayed, giving users a sense of popular options.

### Recommendation System
Users can enter the name of a book on the `/recommend` page. The app identifies the book in the dataset and calculates similarity between it and other books using content-based filtering. It then recommends the top 4 most similar books based on this similarity, showing their titles, authors, and images.

### Machine Learning Model
The recommendation engine uses a pre-trained model stored in `pt.pkl` and `similarity_scores.pkl`. The model computes similarity scores between books based on their features (e.g., titles and authors) to make tailored recommendations.

