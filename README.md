# 🎬 Movie Recommendation System

A simple Python-based Movie Recommendation System that suggests movies to users based on **User-Based Collaborative Filtering** using cosine similarity.

---

## 🚀 Features

- Reads movie rating data from CSV
- Uses user-based collaborative filtering
- Calculates similarity using cosine similarity
- Recommends unseen movies
- Simple command-line interface

---

## 🛠️ Requirements

- Python 3.x
- pandas
- scikit-learn

Install required libraries:

```bash
pip install pandas scikit-learn
📂 Project Structure
Movie_Recommendation_App.py
movie_ratings.csv
README.md
📊 Dataset Format
The movie_ratings.csv file should contain:

user	movie	rating
1	Inception	5
1	Titanic	4
2	Inception	4
2	Avatar	5
user → User ID (integer)

movie → Movie name

rating → Rating given by the user

▶️ How to Run
Place movie_ratings.csv in the same directory.

Run the program:

python Movie_Recommendation_App.py
Enter the user ID when prompted:

Enter the user id for recommendations: 1
The system will display recommended movies.

🧠 How It Works
1️⃣ Load Dataset
Reads CSV file using pandas.

pd.read_csv(file_path)
2️⃣ Create Ratings Matrix
Converts dataset into a pivot table:

Rows → Users

Columns → Movies

Values → Ratings

Missing values are replaced with 0.

3️⃣ Calculate User Similarity
Uses cosine similarity:

cosine_similarity(matrix)
This calculates how similar users are based on their ratings.

4️⃣ Recommend Movies
Finds similar users

Checks movies they rated

Filters movies not watched by the target user

Ranks movies based on aggregated scores

📌 Example Output
Recommendations for user 1:
Avatar: 5.0
Interstellar: 4.5
⚙️ Key Functions
load_dataset() → Loads CSV file

calculate_similarity() → Computes similarity matrix

recommend_movies() → Generates recommendations

main() → Controls application flow
