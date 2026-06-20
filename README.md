# 🎬 Movies Data Analysis (EDA Project)

A beginner-friendly **Exploratory Data Analysis (EDA)** project on a movies dataset, built using **Python, Pandas, Matplotlib, and Seaborn**. This project cleans raw movie data and answers real questions like *"Which genre is most popular?"* and *"Which movie got the highest popularity?"*

---

## 📌 Project Overview

This project takes a raw movies dataset (`mymoviedb.csv`) containing details like release date, title, popularity, votes, and genre — and:

1. Cleans and prepares the data
2. Transforms columns into more useful formats
3. Visualizes patterns and trends
4. Answers specific business-style questions about the dataset

---

## 🛠️ Tools & Libraries Used

| Library | Purpose |
|---|---|
| **Pandas** | Reading, cleaning, and transforming the dataset |
| **NumPy** | Numerical operations |
| **Matplotlib** | Plotting graphs |
| **Seaborn** | Statistical, prettier visualizations |

---

## 📂 Dataset

**File:** `mymoviedb.csv`

**Original Columns:**
| Column | Description |
|---|---|
| Release_Date | Date the movie was released |
| Title | Movie name |
| Overview | Short description (dropped later) |
| Popularity | Popularity score |
| Vote_Count | Number of votes |
| Vote_Average | Average rating |
| Original_Language | Movie's language (dropped later) |
| Genre | One or more genres (comma-separated) |
| Poster_Url | Image link (dropped later) |

---

## 🧹 Data Cleaning Steps

1. **Checked for duplicates** → found `0` duplicate rows ✅
2. **Converted `Release_Date`** from text to a proper date format, then kept only the **year**
3. **Dropped unnecessary columns**: `Overview`, `Original_Language`, `Poster_Url`
4. **Categorized `Vote_Average`** into 4 easy-to-understand labels using quartiles:
   - `not_popular`
   - `below_avg`
   - `average`
   - `popular`
5. **Removed missing values** (if any)
6. **Split the `Genre` column** (e.g. `"Action, Adventure"`) into multiple rows — one genre per row — using `explode()`, so each movie can be counted correctly per genre
7. **Converted `Genre` and `Vote_Average`** into category data type for memory efficiency

➡️ Final cleaned dataset: **25,552 rows** (after genre split) and **6 columns**.

---

## 📊 Key Questions Answered (with Visuals)

### 1️⃣ What is the most frequent movie genre?
A count plot was used to rank genres by frequency.
**Answer:** 🎭 **Drama** is the most common genre (3,715 movies).

### 2️⃣ How are votes distributed across categories?
A count plot shows how many movies fall into each rating category (`popular`, `average`, `below_avg`, `not_popular`) — turns out they're fairly evenly split (~2,400 each).

### 3️⃣ Which movie has the highest popularity, and its genre?
**Answer:** 🕷️ **Spider-Man: No Way Home** (Popularity: 5083.95) — Genres: *Action, Adventure, Science Fiction*

### 4️⃣ Which movie has the lowest popularity, and its genre?
**Answer:** Tied between **The United States vs. Billie Holiday** and **Threads** (Popularity: 13.354)

### 5️⃣ Which year had the most movies released?
A histogram of `Release_Date` shows the distribution of movies by year — most movies in the dataset are from recent years.

---

## 🚀 How to Run This Project

1. Clone/download this repository
2. Make sure `mymoviedb.csv` is in the same folder as the notebook
3. Install the required libraries:
   ```bash
   pip install pandas numpy matplotlib seaborn
   ```
4. Open the notebook in Jupyter:
   ```bash
   jupyter notebook
   ```
5. Run all cells from top to bottom 🎉

---

## 📈 Sample Insights at a Glance

- 🎭 **Drama** dominates as the most common genre
- 🕷️ **Spider-Man: No Way Home** is the most popular movie in this dataset
- 📅 Movie releases are skewed toward recent years
- ⭐ Vote average ratings are evenly distributed across 4 categories

---

## 👩‍💻 Author

Made with ❤️ by **Aditi Gupta**

---

⭐ If you found this project helpful, give it a star!
