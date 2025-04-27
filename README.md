# 📚 Book Recommendation System using ML

An advanced web-based machine learning project designed to recommend books to users based on **popularity metrics** and **collaborative filtering techniques** using **Machine Learning (ML)** and **Natural Language Processing (NLP)** concepts. 

This system not only enhances user experience but also addresses the challenge of book discovery in an information-rich digital world.

---
## 📢 About the Project

In today’s world, readers are faced with an overwhelming number of book choices across platforms. Finding the right book that matches personal preferences becomes a significant challenge. The **Book Recommendation System** aims to bridge this gap by utilizing data-driven approaches to suggest books that users are most likely to enjoy.

This project uses **two primary recommendation strategies**:
- **Popularity-Based Recommendations:** Suggests books that are universally liked by a large audience.
- **Collaborative Filtering:** Recommends books based on similarities between users' tastes and behavior patterns.

The system is implemented as a **Flask web application** with a user-friendly **Bootstrap**-powered frontend, and it uses **Python libraries** for data processing and machine learning tasks.

---

## 🎯 Project Objectives

- To **develop a web application** that recommends books based on user preferences and book popularity.
- To **implement machine learning algorithms** for popularity-based and collaborative filtering-based recommendations.
- To **design an intuitive and responsive user interface** to ensure easy interaction and accessibility.
- To **serialize pre-trained models** to ensure fast, real-time recommendations.
- To **create a scalable and extendable system** capable of handling an increasing user base and larger datasets.

---

## 🧠 Problem Statement

With millions of books available globally, users struggle to find books aligned with their interests. Traditional search methods often fail to capture users' implicit tastes.  
This project addresses this problem by:
- Highlighting top-rated books (Popularity-based approach).
- Suggesting books based on the behavior and preferences of similar users (Collaborative filtering).

---

## 🛠️ Technologies and Tools Used

| Category                | Details                              |
|--------------------------|--------------------------------------|
| Programming Language     | Python 3.x                           |
| Backend Framework        | Flask                                |
| Frontend Technologies    | HTML5, CSS3, Bootstrap 3.3.7         |
| Machine Learning Libraries| scikit-learn, pandas, numpy          |
| Serialization            | Pickle (for model saving/loading)    |
| Database                 | CSV Files (books.csv, users.csv, ratings.csv) |
| IDE                      | Visual Studio Code         |
| Operating System         | Windows 11 |

---

## 🧩 System Architecture

The system architecture is divided into three main components:

1. **Data Layer:**  
   - CSV datasets containing book information, user details, and user-book ratings.
   
2. **Business Logic Layer:**  
   - ML models trained for popularity and collaborative filtering.
   - Data preprocessing, model building, and prediction mechanisms.

3. **Presentation Layer:**  
   - Flask web server handling routes.
   - Frontend templates displaying recommendations and search results.

![](https://github.com/MrHAM17/Book_Recommendation_System_using_ML/blob/ML/2.%20Rough%20Work%20%26%20Data/Img%201.png)
---

![](https://github.com/MrHAM17/Book_Recommendation_System_using_ML/blob/ML/2.%20Rough%20Work%20%26%20Data/Flowchart.png)
---

![](https://github.com/MrHAM17/Book_Recommendation_System_using_ML/blob/ML/2.%20Rough%20Work%20%26%20Data/Block%20Diagram.png)
---

![](https://github.com/MrHAM17/Book_Recommendation_System_using_ML/blob/ML/2.%20Rough%20Work%20%26%20Data/Img%204.png)
---


---

## 📚 Datasets Used

The system relies on three datasets sourced from Kaggle:

- **Books Dataset:** Metadata about books (title, author, ISBN, image URL).
- **Users Dataset:** Information about the users.
- **Ratings Dataset:** User ratings for books.

---

## 🔎 Algorithms and Methodologies

### 1. Popularity-Based Recommendation

- **Concept:**  
  Books are recommended based on their overall acceptance and rating among the community.

- **Steps:**
  1. **Aggregate ratings** by counting the number of reviews and calculating the mean rating for each book.
  2. **Filter** books that have received fewer than **250 reviews** (to ensure reliability).
  3. **Sort** books by descending average ratings.
  4. **Display Top 50** books to users.

- **Advantages:**
  - Fast and simple.
  - No requirement for personalized user data.
  - Highlights universally popular content.

- **Limitations:**
  - No personalization; assumes all users have similar preferences.

---

### 2. Collaborative Filtering-Based Recommendation (Item-Based)

- **Concept:**  
  Recommends books based on the principle: "**Users who liked this book also liked these books**".

- **Techniques Used:**
  - **Cosine Similarity**: Measures similarity between book rating vectors.

- **Steps:**
  1. **Create a pivot table**: Rows = Book titles, Columns = User IDs, Cells = User ratings.
  2. **Compute cosine similarity** between the rating vectors of books.
  3. **Identify and recommend** books that have the highest similarity score to a given book input.

- **Advantages:**
  - Personalized recommendations based on similar taste.
  - Uncovers hidden patterns in user preferences.

- **Limitations:**
  - Cold Start Problem: New books or users with no history might not get recommendations.

---

## 🔥 Project Implementation Details

### 1. Data Preprocessing
- Removal of duplicates and null values.
- Merging datasets to form meaningful relationships.
- Creation of models based on cleaned datasets.

### 2. Model Training
- **Popularity Model:**  
  Aggregation and filtering based on user ratings.

- **Collaborative Filtering Model:**  
  Construction of similarity matrices using pivot tables and cosine similarity.

### 3. Model Serialization
- **Pickle Files:**
  - `popular.pkl`: Stores top 50 popular books.
  - `similarity_scores.pkl`: Stores cosine similarity matrix.
  - `pt.pkl`: Stores pivot table.

### 4. Flask Web Application
- **Routes:**
  - `/` - Homepage displaying top books.
  - `/recommend` - Page for personalized recommendations.

- **Templates:**
  - `index.html` - Top books display page.
  - `recommend.html` - Book search and recommendation page.

---


## 📸 Output Screenshots

| View | Description |
|:---|:---|
| **Homepage** | Displays Top 50 Popular Books with images and ratings |
| **Recommendation Page** | Search for a book and receive similar recommendations |
| **Recommendation Results** | List of recommended books with cover images |

![](https://github.com/MrHAM17/Book_Recommendation_System_using_ML/blob/ML/2.%20Rough%20Work%20%26%20Data/Output%201.png)
---

![](https://github.com/MrHAM17/Book_Recommendation_System_using_ML/blob/ML/2.%20Rough%20Work%20%26%20Data/Output%202.png)
---

![](https://github.com/MrHAM17/Book_Recommendation_System_using_ML/blob/ML/2.%20Rough%20Work%20%26%20Data/Output%203.png)
---

![](https://github.com/MrHAM17/Book_Recommendation_System_using_ML/blob/ML/2.%20Rough%20Work%20%26%20Data/Output%204.png)
---

---

## 🚀 Key Features

- 📚 **Top 50 Books Showcase:** Instant display of the most highly rated books.
- 🧠 **Intelligent Book Recommendations:** Personalized results using collaborative filtering.
- ⚡ **High Performance:** Quick responses through pre-trained serialized models.
- 🎨 **Responsive UI:** Bootstrap-based design compatible with mobiles, tablets, and desktops.
- 🔄 **Scalable Architecture:** Easy to extend with additional features like user login, real-time ratings, etc.

---

## 🛠️ Future Scope and Enhancements

- **User Authentication System:** Personalized dashboard and favorite book list.
- **Real-Time Recommendations:** Update recommendations dynamically with live feedback.
- **API Integration:** Integration with external APIs like Google Books API.
- **Advanced ML Techniques:** Incorporating Deep Learning for complex patterns.
- **Dynamic Data Updates:** Continuous ingestion of new books and user preferences.

---

## 📚 References

- Kaggle Dataset: [Book Recommendation Dataset](https://www.kaggle.com/datasets/arashnic/book-recommendation-dataset)
- Scikit-learn Documentation
- Flask Framework Documentation
- Machine Learning and NLP resources

---

## 📂 Reports & Docs

- **Project Report**:   [Click here to view project reort](https://github.com/MrHAM17/Book_Recommendation_System_using_ML/blob/ML/1.%20Project%20All%20IMP%20Docs/BE_COMP_C_28_ML_Mini_Project_Report.pdf)
- **All Pics**: [Click here to view all](https://github.com/MrHAM17/Book_Recommendation_System_using_ML/tree/ML/2.%20Rough%20Work%20%26%20Data)
---

