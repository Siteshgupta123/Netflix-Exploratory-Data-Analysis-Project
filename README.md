![Logo](https://github.com/user-attachments/assets/89197a92-16bf-45c4-8454-6ac53b3f0586)
# Netflix Exploratory Data Analysis Project

Welcome to the Netflix Exploratory Data Analysis (EDA) project! This project showcases a comprehensive analysis of Netflix's content database using **Power BI**, **Python (Jupyter Notebook)**, and DAX measures. It offers valuable insights into streaming trends, content types, ratings, genres, and global distribution.

---

## 🧠 Objective

The goal of this project is to:
- Analyze the types and distribution of Netflix content.
- Identify genre-wise popularity and multi-genre trends.
- Evaluate the addition of content over time.
- Visualize average movie duration and TV show seasons.
- Segment content by global presence and content ratings.

---
## Project View:
<img width="1537" height="856" alt="image" src="https://github.com/user-attachments/assets/1e571916-fbf4-4f6c-8115-0328c1856ebb" />

https://github.com/user-attachments/assets/46976afa-e821-400b-a262-58e088070ebc



## 📌 Key Insights from Dashboard

### 🔢 High-Level Metrics:
| Metric | Value |
|--------|-------|
| 🎬 Total Movies | 11,492 |
| 📺 Total TV Shows | 367 |
| 🆔 Total Content IDs | 5,333 |
| 📦 Total Titles | 5,331 |
| ⏱️ Avg. Movie Duration | 106.16 mins |
| 📊 Avg. TV Show Seasons | 10 |
| 🎭 Multi-Genre Titles | 1.1K (9.28%) |
| 🎞️ Single Genre Titles | 10.76K (90.71%) |

---

### 🌐 Top Genre by Content ID:
- International Movies: ~2,300+
- Dramas: ~2,200+
- Action & Adventure, Romance, Thrillers, Sci-Fi, and Classic Movies follow.

---

### 🌍 Global Reach:
The dataset reflects content distribution across **North America, Europe, Asia, Australia, Africa, and South America** through location-based mapping.

---

### 📈 Content Addition Over Time:
- Massive growth between **2016–2019**
- Peak around **2018**, slight decline in **2020**

---

### 🏷️ Content Rating Breakdown:
Includes a wide range of categories:
`G`, `PG`, `TV-14`, `TV-MA`, `TV-G`, `UR`, `R`, `NR`, `TV-Y`, `TV-Y7`, `NC-17`, etc.

---
## 📁 Project Structure

| File/Folder | Description |
|------------|-------------|
| `Netflix Data Analysis Dashboard.pbix` | Power BI file containing the full interactive dashboard |
| `Netflix_data.ipynb` | Jupyter Notebook for initial EDA & data preprocessing |
| `clean_netflix_titles.csv` | Cleaned dataset used in dashboard |
| `netflix_titles.csv` | Raw dataset containing Netflix titles |
| `BG.png` | Gradient background used in the Power BI dashboard |
| `Logo.jpg` | Custom Netflix Data Analysis logo |
| `README.md` | Project overview & insights |

-----
## 🛠️ Tools & Technologies Used

- **Power BI** – Data visualization & dashboarding
- **DAX (Data Analysis Expressions)** – Custom metrics & KPIs
- **Python (Pandas, Matplotlib)** – EDA & data transformation
- **GitHub** – Version control & project documentation

---

## 📐 DAX Measures Used

```DAX
Total Movies = CALCULATE(COUNT('clean_netflix_titles (2)'[Content ID]), 'clean_netflix_titles (2)'[Content type] = "Movie")
```
```
Total TV Shows = CALCULATE(COUNT('clean_netflix_titles (2)'[Content Id]), 'clean_netflix_titles (2)'[Content type] = "TV Show")
```
```
Multi-Genre Titles = CALCULATE(COUNT('clean_netflix_titles (2)'[Content ID]), 'clean_netflix_titles (2)'[Is Multi-Genre] = TRUE())
```
```
Average Movie Duration = AVERAGEX(FILTER('clean_netflix_titles (2)', 'clean_netflix_titles (2)'[Content type] = "Movie"), 'clean_netflix_titles (2)'[Numerical Duration])
```
```
Average TV Show Seasons = AVERAGEX(FILTER('clean_netflix_titles (2)', 'clean_netflix_titles (2)'[Content type] = "TV Show"), 'clean_netflix_titles (2)'[Seasons])
```
---------------
## Thank You! 💙
Thanks for checking out my project! If you found it useful, please consider:  
[![GitHub stars]([https://github.com/Siteshgupta123/Netflix-Exploratory-Data-Analysis-Project])  
⭐ **Starring** the repo  
🐛 **Reporting** issues  
🛠 **Contributing** improvements  
