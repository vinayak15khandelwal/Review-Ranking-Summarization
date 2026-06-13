# Intelligent Review Ranking System Using Ant Colony Optimization with NLP-Based Feature Extraction


## Project Overview

This project implements a review ranking system using Ant Colony Optimization (ACO) combined with Natural Language Processing (NLP). The objective is to rank product reviews based on importance using multiple extracted features.

---

## Technologies Used

* Python 3.x
* Pandas
* NumPy
* Matplotlib
* NLTK (VADER Sentiment Analyzer)
* OpenPyXL

---

## Project Structure

```
project/
│
├── notebooks/
│   ├── 01_data_loading.ipynb
│   ├── 02_feature_extraction.ipynb
│   ├── 03_aco_ranking.ipynb
│
├── data/
│   ├── raw_reviews.csv
│   ├── processed_reviews.csv
│
├── results/
│   ├── aco_ranked_reviews.csv
│   ├── aco_feature_importance.csv
│   ├── top_aco_reviews.csv
│   ├── aco_full_report.xlsx
│   ├── convergence_curve.png
│
└── README.md
```

---

## How to Run the Code

Step 1: Install dependencies

```
pip install pandas numpy matplotlib nltk openpyxl
```

Step 2: Download dataset
Use Amazon Reviews dataset (Electronics category)

Step 3: Run notebooks in sequence:

1. 01_data_loading.ipynb
2. 02_feature_extraction.ipynb
3. 03_aco_ranking.ipynb

---

## Input Format

The system takes review data in JSON format and converts it into CSV.

Important columns:

* reviewText
* overall rating
* helpful votes
* reviewTime

---

<img width="581" height="417" alt="image" src="https://github.com/user-attachments/assets/2a6a9f38-6f82-4ea6-8631-f179495e781a" />


## Output Format

The system generates:

* Ranked reviews (CSV)
* Feature importance (CSV)
* Top reviews (CSV)
* Excel report containing:

  * Model comparison
  * Accuracy metrics
  * Sentiment distribution
  * Keywords
  * Graphs
 
<img width="722" height="566" alt="image" src="https://github.com/user-attachments/assets/fa43f4ab-6e4f-48f2-af13-4bb64b3ad009" />


---

## Methodology

1. Feature Extraction

   * Sentiment using VADER
   * Review length
   * Helpfulness ratio
   * Freshness

2. Feature normalization

3. ACO optimization

   * Ants generate candidate weight vectors
   * Fitness evaluated using correlation
   * Pheromone updated iteratively

4. Ranking

   * Final score = weighted combination of features

---

<img width="691" height="470" alt="convergence_curve" src="https://github.com/user-attachments/assets/9cfbdb7c-717b-4847-a42e-db1f57c47329" />


## Evaluation Metrics

* Pearson Correlation
* Precision@K
* NDCG

---

## Notes

* Ensure Excel file is closed before writing output
* Dataset size can be adjusted in the loading script

---

### Author

ANMOL VIRMANI \
VINAYAK KHANDELWAL 
---

