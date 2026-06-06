# 🎬 Netflix Content EDA (Exploratory Data Analysis)

A comprehensive exploratory data analysis of Netflix's content library, uncovering trends in content type, genres, production countries, IMDb scores, and content growth over time.

---

## 📌 Project Overview

This project analyzes a Netflix dataset to understand what kind of content Netflix produces, which countries contribute most, how content has grown over the years, and what factors influence IMDb ratings.

---

## 📂 Dataset

- **File:** `netflixData.csv`
- **Source:** Netflix content dataset
- **Features include:** Title, Content Type, Genre, Release Date, Date Added, IMDb Score, Duration, Director, Cast, Production Country, Rating

---

## 🛠️ Technologies Used

| Tool | Purpose |
|------|---------|
| Python | Core programming language |
| Pandas | Data manipulation and cleaning |
| NumPy | Numerical operations |
| Matplotlib | Data visualization |
| Seaborn | Statistical visualizations |

---

## 🔧 Data Preprocessing

- Converted `Release Date` to datetime (year format)
- Parsed and cleaned `IMDb Score` (removed `/10` suffix)
- Extracted numeric values from `Duration` column
- Filled missing values:
  - `Director` and `Production Country` → filled with `0`
  - `Release Date` and `Duration` → filled with **median**
  - `Rating` → filled with **mode**
  - `IMDb Score` → filled with **median**
  - `Date Added` → filled with **mode**

---

## ⚙️ Feature Engineering

New columns created to improve analysis:

- `Release Year` — extracted from `Release Date`
- `Added Year` — extracted from `Date Added`
- `Cast Count` — number of cast members per title
- `Genre Count` — number of genres per title

---

## 📊 Analysis Performed

### Univariate Analysis
- Distribution of Content Type (Movies vs TV Shows)
- Top Genres by count
- Top Production Countries
- IMDb Score distribution (histogram)
- Duration distribution

### Bivariate Analysis
- IMDb Score by Content Type (boxplot)
- Average IMDb Score by Rating
- Average IMDb Score by Genre
- Correlation between Cast Count and IMDb Score

### Time-based Analysis
- Content released per year
- Content added to Netflix per year

### Correlation Analysis
- Heatmap of IMDb Score, Duration, Cast Count, and Genre Count

---

## 💡 Key Insights

- **Movies dominate** TV Shows in the Netflix dataset
- **USA produces the most** content on Netflix
- **Drama and International genres** are the most common
- **IMDb scores** mostly lie between **5 and 8**, with a mean around **6**
- Content production **increased significantly after 2010**
- **2019** had the highest number of content releases
- **2021** saw the most content added to Netflix
- **TV Shows score slightly higher** than Movies on IMDb
- **More cast members** have a slightly negative correlation with IMDb score
- Most correlations between features are weak — genres and cast size don't strongly influence ratings

---

## 📁 Project Structure

```
netflix-eda/
│
├── Final_EDA_Project.ipynb   # Main Jupyter Notebook
├── netflixData.csv           # Dataset (add manually)
└── README.md                 # Project documentation
```

---

## 🚀 How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/netflix-eda.git
   cd netflix-eda
   ```

2. Install required libraries:
   ```bash
   pip install pandas numpy matplotlib seaborn
   ```

3. Place `netflixData.csv` in the project folder

4. Open and run the notebook:
   ```bash
   jupyter notebook Final_EDA_Project.ipynb
   ```

---

## 👤 Author

**Your Name**
- GitHub: AminaAshfaqShareef(https://github.com/AminaAshfaqShareef)
- LinkedIn: [Amina Ashfaq](https://linkedin.com/in/amina-ashfaq12?)

---

## 📜 License

This project is open source and available under the [MIT License](LICENSE).
