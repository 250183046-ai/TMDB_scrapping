E-Commerce Market Intelligence: Kaspi.kz Strategic Analysis
Table of Contents

About

Technical Pipeline

Data Structure

Key Insights

Repository Structure

Execution Guide

## About
This project provides a comprehensive analytical framework for the Kazakhstan e-commerce sector, specifically focusing on the Jewelry and Accessories market. It integrates advanced Browser Automation, automated data enrichment, and statistical modeling to transform raw marketplace data into actionable business insights.

## Technical Pipeline
The pipeline is designed to handle high-security, dynamic web environments:

Data Acquisition: Asynchronous scraping via Playwright and Asyncio. Implements Human-in-the-Loop logic (simulated scrolling and delays) to bypass anti-bot protections.

Preprocessing: Advanced Regex (Regular Expressions) for material detection and brand standardization across "noisy" seller-generated titles.

Exploratory Data Analysis (EDA): Price distribution analysis and anomaly detection using the Interquartile Range (IQR) method.

Predictive Modeling: Linear Regression analysis using scikit-learn to determine the correlation between product attributes and market success.

## Data Structure
The final processed dataset (kaspi_smart_data.csv) includes standardized features:

Feature	Description
Price	Sanitized numeric current price (KZT).
Material Tier	Categorized quality levels (Luxury, Silver, Alloy).
Product Type	Classification based on category (Tiara, Hairpin, etc.).
Success Score	Multi-dimensional metric based on ratings and engagement.
## Key Insights
Market Concentration: Statistical analysis reveals that Luxury items (Gold/Gems) capture 21.7% of the total market value despite lower volume.

Success Drivers: Machine Learning coefficients indicate that Customer Ratings have a 14% stronger impact on the Success Score than raw popularity or price discounts.

Material Influence: Silver and Alloy items dominate the "High Volume" segment, showing the highest turnover rate in the 2025-2026 period.

## Repository Structure
Bash
├── kaspi_scraper.py       # Asynchronous engine (Playwright + Anti-bot)
├── cleaning_regex.py      # Data enrichment and brand standardization
├── ml_analysis.py         # Linear Regression and hypothesis testing
├── visual_reporting.py    # Automated 12-chart reporting suite
├── app_dashboard.py       # Interactive Streamlit interface
└── requirements.txt       # Project dependencies
## Execution Guide
1. Environment Setup

Bash
pip install -r requirements.txt
playwright install
2. Workflow

Execute the modules in the following sequence to replicate the study:

Collection: python kaspi_scraper.py (Handles dynamic JS rendering)

Cleaning: python cleaning_regex.py (Applies Regex patterns)

Modeling: python ml_analysis.py (Runs Scikit-learn regression)

Reporting: python visual_reporting.py (Generates final charts)

Final Verdict

"By successfully navigating Kaspi’s dynamic content and anti-bot security, this project proves that even unstructured marketplace data can be transformed into a reliable predictor of consumer behavior and market trends."

REPORT END - AZIA 2026
