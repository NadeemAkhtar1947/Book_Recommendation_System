# 📚 Book Recommendation System

## 📝 Overview
This project implements a **Book Recommendation System** using **Popularity-Based** and **Collaborative Filtering-Based** techniques. It leverages a dataset containing book ratings, user information, and book details to provide personalized book recommendations.

## 📂 Dataset
- **📌 Source:** Book Recommendation Dataset
- **📑 Files:**
  - `Books.csv`: Contains book details (Title, Author, ISBN, Image URLs, etc.).
  - `Ratings.csv`: User ratings for various books.
  - `Users.csv`: User demographic information.
- **📊 Data Preprocessing:**
  - Removed missing values.
  - Eliminated duplicate entries.
  - Filtered books with at least **50 ratings** and users with more than **200 ratings**.

## 🏆 Recommendation Techniques
### 🔹 **Popularity-Based Recommendation**
- Recommends the **top 50 most popular books** based on:
  - **Number of Ratings** (books rated at least 250 times)
  - **Average Rating** (sorted in descending order)
- **Example Output:**
  ```bash
  Book Title: The Hobbit
  Author: J.R.R. Tolkien
  Average Rating: 4.5
  Number of Ratings: 1200
  ```

### 🔹 **Collaborative Filtering-Based Recommendation**
- **User-Item Interaction Matrix** created via pivot table.
- Used **Cosine Similarity** to find books similar to a given book.
- **Example Output:**
  ```bash
  Recommendations for '1984':
  - Brave New World
  - Fahrenheit 451
  - Animal Farm
  ```

## 🔬 Implementation Steps
1. **Load and Preprocess Data**
2. **Popularity-Based Model:** Compute top-rated books.
3. **Collaborative Filtering:**
   - Create **pivot table** (Book-User matrix).
   - Compute **Cosine Similarity**.
   - Generate **Top-N Book Recommendations**.
4. **Save Models Using Pickle**
   ```python
   import pickle
   pickle.dump(final_ratings, open('final_ratings.pkl', 'wb'))
   pickle.dump(pt, open('pt.pkl', 'wb'))
   pickle.dump(book, open('book.pkl', 'wb'))
   pickle.dump(similarity, open('similarity.pkl', 'wb'))
   ```

## 🛠️ Installation & Usage
### **📌 Requirements**
Ensure you have the following Python libraries installed:
```bash
pip install pandas numpy seaborn matplotlib scikit-learn
```

### **▶️ Running the Code**
```bash
python recommend.py
```

## 🎯 Future Enhancements
- Integrate **Deep Learning Models** (Neural Collaborative Filtering, Autoencoders).
- Deploy the system as a **Web App using Streamlit or Flask**.
- Enhance recommendations with **Hybrid Models**.

## 📬 Contact & Support
Connect with me for feedback or contributions:

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/nadeem-akhtar-/) | [![GitHub](https://img.shields.io/badge/GitHub-333?style=for-the-badge&logo=github&logoColor=white)](https://github.com/NadeemAkhtar1947) | [![Kaggle](https://img.shields.io/badge/Kaggle-00A65A?style=for-the-badge&logo=Kaggle&logoColor=white)](https://www.kaggle.com/mdnadeemakhtar/code)
| [![Portfolio](https://img.shields.io/badge/Portfolio-FF5733?style=for-the-badge&logo=Google-chrome&logoColor=white)](https://nsde.netlify.app/)

🚀 **Developed by Nadeem Akhtar** | 📅 **Copyright © 2024**

