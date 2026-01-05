# Trader Behavior Analysis in Crypto Markets

## 1. Project Overview

This repository contains a data science project analyzing the behavior of crypto perpetual futures traders in response to different market sentiment regimes, as defined by the Fear & Greed Index. The analysis leverages historical trading data to segment traders, explore behavioral patterns, and identify factors correlated with profitability. The primary goal is to understand how fear and greed influence trading decisions and outcomes.

## 2. Data Description

The analysis is based on two main sources of data:
- **Historical Trading Data:** A granular dataset of perpetual futures trades, including trader identifiers, trade size, direction (long/short), and realized Profit and Loss (PnL).
- **Fear & Greed Index:** A daily time series of market sentiment scores, classified into categories such as "Extreme Fear," "Fear," "Neutral," "Greed," and "Extreme Greed."

These datasets were preprocessed, cleaned, and merged by date to form a unified analytical dataset.

## 3. Analytical Approach

The analysis was conducted in a multi-step process:

1.  **Data Enrichment & EDA:** The core trading data was merged with the daily sentiment index. An extensive exploratory data analysis (EDA) was performed to uncover initial relationships between sentiment, trading volume, and PnL.
2.  **Feature Engineering:** A comprehensive set of features was engineered to capture trader behavior at a daily level. These include metrics such as win rate, PnL per trade, trade frequency, average position size, and holding duration.
3.  **Trader Segmentation (Clustering):** K-Means clustering was applied to the engineered features to segment traders into distinct behavioral archetypes (e.g., "High-Frequency Scalpers," "Low-Frequency Whales").
4.  **Behavioral Analysis:** The performance and trading patterns of each trader cluster were analyzed in depth. This involved comparing their profitability, risk tolerance, and strategic adjustments across different sentiment regimes (Fear vs. Greed).
5.  **Predictive Modeling:** A multiple linear regression model was developed to identify the key drivers of daily trading profitability, using sentiment, cluster identity, and other behavioral metrics as predictors.

## 4. Key Behavioral Questions Explored

This analysis sought to answer several key questions about trader behavior:

- How do aggregate trading volume, PnL, and frequency change with market sentiment?
- Can traders be segmented into distinct, meaningful profiles based on their trading patterns?
- Which trader profiles are the most profitable, and under which sentiment conditions do they excel or underperform?
- Does trading direction (long vs. short bias) systematically shift between "Fear" and "Greed" market phases?
- What are the most significant predictors of a trader's daily profitability?

## 5. Repository Structure

```
.
├── csv_files/              # Intermediate and final CSV datasets
│   ├── daily_features.csv
│   ├── cluster_profiles.csv
│   └── ...
├── notebook_1.ipynb        # Data loading, preprocessing, and EDA
├── notebook_2.ipynb        # Feature engineering, clustering, and modeling
├── outputs/                # Generated plots and figures
├── ds_report.pdf           # PDF summary of key findings
└── README.md               # This project overview
```

- **`notebook_1.ipynb`**: Focuses on data loading, cleaning, merging, and initial exploratory analysis.
- **`notebook_2.ipynb`**: Contains the advanced analysis, including feature engineering, K-Means clustering of traders, and predictive modeling.
- **`ds_report.pdf`**: A concise report summarizing the methodology, key insights, and conclusions.
- **`csv_files/`**: Stores all data generated during the analysis, allowing for quick validation and review without re-running the notebooks.
- **`outputs/`**: Contains all visualizations produced during the analysis.

## 6. How to View the Notebooks (Google Colab)

The notebooks are best viewed using Google Colab to ensure all interactive plots render correctly.

1.  Navigate to [Google Colab](https://colab.research.google.com/).
2.  Select the **"GitHub"** tab.
3.  Paste the URL of this repository into the search bar and press Enter.
4.  Click on `notebook_1.ipynb` or `notebook_2.ipynb` to open them.

## 7. Notes for the Reviewer

- The analysis is presented sequentially across the two notebooks. `notebook_1.ipynb` should be reviewed first.
- For a high-level summary of the project's findings, please refer to **`ds_report.pdf`**.
- The `csv_files` directory contains the final, cleaned datasets. The notebooks can be run from start to finish, but the pre-generated files are provided to facilitate a faster review of the analytical steps.