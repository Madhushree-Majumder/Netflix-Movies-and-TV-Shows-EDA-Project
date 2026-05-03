# 🎬 Netflix Movies & TV Shows — Exploratory Data Analysis

![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-11557C)
![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-4c72b0)
![License](https://img.shields.io/badge/License-CC0%20Public%20Domain-green)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

An end-to-end exploratory data analysis of Netflix's content library — uncovering trends in content type, genre distribution, global production, ratings, and release patterns using Python.

> 📊 **Dataset:** [Netflix Movies and TV Shows — Kaggle](https://www.kaggle.com/datasets/zafarali27/netflix-movies-and-tv-shows/data)

---

## 📁 Project Structure

```
netflix-eda/
│
├── data/
│   └── netflix_titles.csv          # Raw dataset from Kaggle
│
├── notebooks/
│   └── netflix_eda.ipynb           # Main analysis notebook
│
├── visuals/
│   └── *.png                       # Exported charts and plots
│
├── README.md
└── requirements.txt
```

---

## 📌 Dataset Overview

The dataset contains metadata for **8,000+ titles** available on Netflix, with the following columns:

| Column | Description |
|---|---|
| `show_id` | Unique identifier for each title |
| `type` | Movie or TV Show |
| `title` | Name of the title |
| `director` | Director(s) of the content |
| `cast` | Lead cast members |
| `country` | Country of production |
| `date_added` | Date added to Netflix |
| `release_year` | Original release year |
| `rating` | Content rating (e.g., TV-MA, PG-13, TV-14) |
| `duration` | Duration in minutes (Movies) or number of seasons (TV Shows) |
| `listed_in` | Genre(s) / categories |
| `description` | Short synopsis |

---

## 🎯 Objectives

- Understand the split between Movies and TV Shows on Netflix
- Identify the most prolific content-producing countries
- Analyse genre trends and content rating distributions
- Explore year-on-year content growth and addition patterns
- Surface top directors and recurring cast members
- Detect and handle missing values across key columns

---

## 🔍 Key Insights

### 1. Content Type Split
Movies dominate Netflix's catalogue, making up approximately **70%** of all titles, while TV Shows account for the remaining **30%**.

### 2. Top Content-Producing Countries
The **United States**, **India**, and the **United Kingdom** are the top three content-producing countries. India ranks as Netflix's largest non-English content contributor, reflecting the platform's major investment in regional content.

### 3. Genre Distribution
The most common genres are **Dramas**, **International Movies**, and **Comedies**. TV Shows skew heavily toward **International TV Shows**, **Crime TV Shows**, and **Docuseries**.

### 4. Content Ratings
**TV-MA** (Mature Audiences) is the most frequent rating, followed by **TV-14** — indicating that Netflix's catalogue is largely targeted at adult and teenage audiences rather than family or children segments.

### 5. Release Year Trends
Content additions to Netflix accelerated sharply between **2015 and 2019**, with a notable peak around **2018–2019**. Post-2020 additions show a slight dip, likely influenced by production slowdowns during the pandemic.

### 6. Movie Duration
The majority of Netflix movies fall in the **80–120 minute** range, consistent with standard theatrical runtime norms.

### 7. Top Directors
Directors such as **Rajiv Chilaka** (India) and **Jan Suter** appear frequently, primarily through animated and children's content. For English-language content, key directors vary widely across genres.

---

## 🛠️ Tools & Libraries

| Tool | Purpose |
|---|---|
| `Python 3.10+` | Core programming language |
| `Pandas` | Data loading, cleaning, transformation |
| `NumPy` | Numerical operations |
| `Matplotlib` | Static visualisations |
| `Seaborn` | Statistical plots and heatmaps |
| `Jupyter Notebook` | Interactive analysis environment |

---

## ⚙️ Setup & Usage

### 1. Clone the repository
```bash
git clone https://github.com/yourusername/netflix-eda.git
cd netflix-eda
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Download the dataset
Download `netflix_titles.csv` from [Kaggle](https://www.kaggle.com/datasets/zafarali27/netflix-movies-and-tv-shows/data) and place it in the `data/` folder.

### 4. Run the notebook
```bash
jupyter notebook notebooks/netflix_eda.ipynb
```

---

## 📦 requirements.txt

```
pandas>=1.5.0
numpy>=1.23.0
matplotlib>=3.6.0
seaborn>=0.12.0
jupyter>=1.0.0
```

---

## 🧹 Data Cleaning Steps

- Removed duplicate entries based on `show_id` and `title`
- Imputed missing `director` and `cast` values with `"Not Available"`
- Converted `date_added` from string to datetime format
- Extracted `month_added` and `year_added` as separate features for time-series analysis
- Split multi-value columns (`listed_in`, `country`, `cast`) using `str.split()` and `explode()` for granular analysis

---

## 📊 Sample Visualisations

> *(Generated charts are saved in the `visuals/` folder)*

- 📈 Content added to Netflix by year (line chart)
- 🍩 Movie vs TV Show split (donut chart)
- 🌍 Top 10 content-producing countries (horizontal bar chart)
- 🎭 Top 15 genres across Movies and TV Shows (bar chart)
- 🔞 Rating distribution (count plot)
- ⏱️ Movie duration distribution (histogram)
- 🗓️ Monthly content addition heatmap (year × month)

---

## 💡 Business Use Cases

This analysis is relevant to:
- **Content strategy teams** evaluating genre saturation and gaps
- **Regional expansion planning** — identifying underrepresented countries
- **Audience segmentation** — aligning content ratings to target demographics
- **OTT platform benchmarking** for competitive analysis in the streaming industry

---

## 📄 License

The dataset is published under the [CC0: Public Domain](https://creativecommons.org/publicdomain/zero/1.0/) licence. This project and all associated code are available under the [MIT Licence](LICENSE).

---

## 🙋 Author

**Madhushree Majumder**
Data Analyst | Power BI · SQL · Python · Alteryx (Advanced Certified)

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?logo=linkedin)](https://www.linkedin.com/in/madhushree-data-analyst)
[![Kaggle](https://img.shields.io/badge/Kaggle-Profile-20BEFF?logo=kaggle)](https://www.kaggle.com/code/madhushreemajumder97)

---

*If you find this project useful, please ⭐ the repository!*
