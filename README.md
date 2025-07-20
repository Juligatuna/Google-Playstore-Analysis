# 📱 Google Play Store Data Analysis Dashboard

This project explores and visualizes the Google Play Store dataset, focusing on app ratings, reviews, pricing, and install trends using **Python for data cleaning** and **Power BI for interactive dashboards**.

---

## 📊 Dashboard Overview

Built in **Power BI**, the dashboard consists of multiple pages designed for insights on:

### 🟦 Page 1: App Category Overview
- **Pie Chart**: Distribution of apps by category
- **Stacked Bar**: Number of apps by content rating per category
- **Card**: Total number of apps, unique categories
- **Legend**: Content Rating

### 🟨 Page 2: Price and Install Analysis
- **Bar Chart**: Top 10 most expensive apps
- **Scatter Plot**: Price vs. Installs (with category color legend)
- **Donut Chart**: Free vs. Paid apps distribution
- **Legend**: App Type

### 🟩 Page 3: Ratings & Reviews
- **Histogram**: Count of apps by `Rating_Bin` (rounded to 1 decimal place)
- **Bubble Chart**: Ratings vs. Reviews
- **Slicers**: Category, Type, Content Rating

> 📸 Screenshots of each page can be found in the [`dashboard/screenshots/`](dashboard/screenshots/) folder.

---

## 🧹 Data Cleaning (Python Notebook)

Data preparation was done in Jupyter using a Pandas-based notebook:

- Removed duplicates & nulls
- Converted `Installs`, `Size`, `Price` to numeric formats
- Created `Rating_Bin` column using:  
  ```python
  df["Rating_Bin"] = round(df["Rating"], 1)
Exported cleaned dataset to CSV for use in Power BI

📄 See notebook: notebooks/01_data_cleaning_googleplay.ipynb

📁 Project Structure
plaintext
Copy
Edit
📁 Google-Playstore-Analysis/
├── data/
│   └── cleaned_googleplay.csv
├── notebooks/
│   └── 01_data_cleaning_googleplay.ipynb
├── dashboard/
│   ├── GooglePlayDashboard.pbix
│   └── screenshots/
│       ├── overview.png
│       ├── category_insights.png
│       ├── ratings_reviews.png
│       ├── pricing_analysis.png
├── README.md
└── .gitignore
🔍 Insights Gained
Free apps dominate, but paid apps still exist in niche categories.

Highly rated apps tend to receive more reviews.

Certain categories (e.g., "Family", "Tools") are overrepresented.

Price does not correlate directly with installs or rating.

🛠️ Tools Used
Python (Pandas, NumPy, Matplotlib) – for data cleaning

Power BI – for dashboard creation

Git & GitHub – for version control and sharing