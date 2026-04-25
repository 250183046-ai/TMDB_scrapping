Movie Industry Intelligence: Global Trends Analysis (TMDB)
Table of Contents

About

Technical Pipeline

Data Structure

Key Insights

Repository Structure

Execution Guide

## About
This project presents a comprehensive study of the global film industry using data extracted from The Movie Database (TMDB). The primary objective is to analyze the correlation between audience engagement, critical ratings, and a movie's overall success in the 2023–2026 market period.

## Technical Pipeline
The project follows a modular architecture to ensure scalability and data integrity:

Data Acquisition: Automated REST API integration using Requests and BeautifulSoup to handle paginated responses (7,000+ records).

Preprocessing: Statistical imputation of missing ratings and localization of genre/language labels from Russian to English.

Feature Engineering: Implementation of a custom Success Score metric using logarithmic scaling:

Success Score=Rating×ln(1+Vote Count)
Predictive Modeling: Linear Regression analysis to determine the weight of popularity vs. rating in predicting success.

## Data Structure
The processed dataset (cleaned_movie_data_final.csv) contains standardized features for analytical depth:

Feature	Description
Title	Standardized movie names.
Success Score	Multi-dimensional success metric (Rating + Engagement).
Popularity Category	Quantile-based segmentation (Low, Medium, High).
Release Year	Extracted temporal feature for trend analysis.
## Key Insights
Quality vs. Hype: Linear Regression coefficients confirmed that Average Rating has a statistically higher impact on the Success Score than raw popularity.

Genre Performance: Animation and Sci-Fi genres demonstrated the highest rating stability across the 2024-2026 period.

NLP Trends: Word Cloud analysis of titles revealed a significant prevalence of action-oriented keywords in high-budget productions.

## Repository Structure
Bash
├── scraping_api.py            # High-speed TMDB API extractor
├── data_cleaning.py           # Localization and feature engineering
├── statistical_analysis.py    # Hypothesis testing and ML modeling
├── visualization_dashboard.py # Matplotlib/Seaborn/Plotly reporting suite
├── app.py                     # Interactive Streamlit Dashboard (+0.5 Bonus)
└── requirements.txt           # Project dependencies
## Execution Guide
1. Environment Setup

Bash
pip install -r requirements.txt
2. Workflow

To replicate the analysis, execute the scripts in the following order:

Data Collection: python scraping_api.py

Transformation: python data_cleaning.py

Analytics & ML: python statistical_analysis.py

Reporting: python visualization_dashboard.py

Final Verdict

"Our data-driven approach demonstrates that in a saturated 2026 market, content quality (Rating) remains the primary driver of long-term cinematic success, outperforming temporary marketing hype (Popularity)."

REPORT END - AZIA 2026
