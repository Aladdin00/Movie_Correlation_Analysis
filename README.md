<div align="center">

# 🎬 Movie Correlation Analysis

**What really drives a movie's box office success?**
An exploratory data analysis of 5,400+ films (1980–2020) using Python, pandas and Seaborn.

![Python](https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?logo=pandas&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-4c72b0)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557c)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?logo=jupyter&logoColor=white)

<img src="images/correlation_heatmap_numeric.png" alt="Correlation heatmap of numeric movie features" width="700">

</div>

---

## Table of Contents

- [Overview](#overview)
- [Key Findings](#key-findings)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [Visualizations](#visualizations)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
- [Project Structure](#project-structure)
- [Contact](#contact)

## Overview

Studios invest millions in each film, but which factors actually relate to how much a movie earns? This project cleans a dataset of movies released between **1980 and 2020** and applies correlation analysis to measure how **budget, audience votes, IMDb score, runtime, genre, rating and production company** relate to **gross earnings**.

The goal is to separate the features that matter from those that don't, using clear visualizations and reproducible steps.

## Key Findings

| Feature | Relationship with Gross Earnings | Takeaway |
|---------|----------------------------------|----------|
| **Budget** | Strong positive (r ≈ 0.74) | Higher-budget films tend to earn substantially more |
| **Votes** | Strong positive (r ≈ 0.63) | Films with larger audiences earn more, and vice versa |
| **Production company** | Weak | The studio name alone is a poor predictor of revenue |

> Budget and votes show the strongest correlation with gross earnings. Correlation does not imply causation.

## Dataset

| Property | Detail |
|----------|--------|
| File | `movies.csv` |
| Period | 1980 – 2020 |
| Rows after cleaning | 5,421 films |
| Columns | name, rating, genre, year, released, score, votes, director, writer, star, country, budget, gross, company, runtime |

## Methodology

**1. Data cleaning**
- Audited missing values for every column; `budget` was the most incomplete (about 28% missing)
- Dropped incomplete rows with `dropna()`
- Converted `budget` and `gross` from float to integer
- Extracted the release year from the `released` text field

**2. Exploratory analysis**
- Scatter plot and regression plot of budget vs. gross earnings

**3. Correlation analysis**
- Pearson correlation matrix and heatmap for numeric features
- Encoded categorical columns (genre, rating, company, etc.) as category codes so they could be included in the correlation matrix
- Unstacked and sorted all feature pairs to isolate the strongest correlations (r > 0.5)

## Visualizations

<table>
  <tr>
    <td align="center"><b>Budget vs. Gross Earnings</b></td>
    <td align="center"><b>Regression Fit</b></td>
  </tr>
  <tr>
    <td><img width="1038" height="703" alt="Scatter plot of budget vs gross" src="https://github.com/user-attachments/assets/85f2ac9b-06d5-423c-a715-5d0a3e66a1d1" /></td>
    <td><img width="1124" height="771" alt="Regression plot of budget vs gross" src="https://github.com/user-attachments/assets/1188dc40-014a-4b95-8e6d-64eedc0fcdc4"/></td>
  </tr>
  <tr>
    <td align="center"><b>Numeric Feature Correlations</b></td>
    <td align="center"><b>All Features (Encoded)</b></td>
  </tr>
  <tr>
    <td><img width="938" height="696" alt="Numeric correlation heatmap" src="https://github.com/user-attachments/assets/4bfbe240-8b9c-440e-b223-0ea880543fad"/>
   </td>
    <td><img width="1019" height="748" alt="Encoded correlation heatmap" src="https://github.com/user-attachments/assets/fb8652c6-96ad-4fe7-b2f6-47ac95c9276a"/>
  </td>
  </tr>
</table>

## Tech Stack

| Category | Tools |
|----------|-------|
| Language | Python |
| Data manipulation | pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Environment | Jupyter Notebook |

## Getting Started

**Prerequisites:** Python 3.8+ and Jupyter.
Excel file (movies.csv).

```bash
# 1. Clone the repository
git clone https://github.com/your-username/movie-correlation-analysis.git
cd movie-correlation-analysis

# 2. Install dependencies
pip install pandas numpy seaborn matplotlib jupyter

# 3. Launch the notebook
jupyter notebook Movie_Correlation_Project.ipynb
```

Place `movies.csv` in the `data/` folder and make sure the path in the first notebook cell points to it.

## Project Structure

```
├── Movie_Correlation_Project.ipynb   # Full analysis
├── data/
│   └── movies.csv                    # Dataset
├── images/                           # Charts used in this README
└── README.md
```


## Contact

Ali Eldin Mohamed · [LinkedIn](https://www.linkedin.com/in/alieldin190)  · alyshaker2004@gmail.com
