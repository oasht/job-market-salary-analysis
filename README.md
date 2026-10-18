
# Job Market Salary Analysis Using NLP and Machine Learning

---

## Project Overview

This project analyses 21,709 job vacancies from hh.ru in Moscow to identify factors associated with salary differences and evaluate how natural language processing (NLP) can improve salary prediction.

The analysis combines exploratory data analysis, statistical hypothesis testing, text mining, clustering and machine learning.

The main objective is to compare salary prediction models based on structured vacancy attributes, textual descriptions and their combination.

---

## Key Results

- Analysed **21,709 job vacancies**, including **14,131 records** in the cleaned salary dataset.
- Found substantial salary differences across experience levels and professional roles.
- Identified statistically significant salary differences between vacancies mentioning PostgreSQL and those without this skill.
- Applied TF-IDF and KMeans clustering to explore patterns in job descriptions.
- Improved salary prediction by combining structured and textual features, achieving **MAE of 29,877 RUB and MAPE of 23.79%** with the best Ridge Regression model.
- Reduced MAE by approximately **18.1%** compared with the structured-data baseline.

---

## Methods

- Data collection via public hh.ru API
- Data cleaning and preprocessing
- Exploratory Data Analysis (EDA)
- Hypothesis testing (Mann–Whitney U, Kruskal–Wallis)
- Natural Language Processing (lemmatization, TF-IDF, Bag-of-Words)
- Feature analysis using chi-square tests
- Unsupervised learning (KMeans clustering)
- Supervised learning (Ridge Regression)
- Model evaluation and comparison (MAE, RMSE, MAPE)

---

## Dataset

- **Source:** hh.ru public API
- **Location:** Moscow, Russia
- **Collected vacancies:** 21,709
- **Cleaned salary dataset:** 14,131 vacancies
- **Median salary:** 110,000 RUB
- **Salary range after filtering:** 30,000–500,000 RUB

The dataset includes structured features (experience, employment type, schedule, professional role) and textual features (job titles, descriptions and required skills).

Vacancies without usable salary information and records outside the selected salary range were excluded from salary modelling.

---

## What I Did

- Collected and cleaned real-world job market data using Python and pandas.
- Explored salary distributions across experience levels, professional roles and working conditions.
- Applied statistical tests to investigate salary differences between vacancy groups.
- Processed Russian-language job descriptions using lemmatization and TF-IDF.
- Identified terms and skill combinations associated with higher- and lower-paying vacancies.
- Applied KMeans clustering to explore similarities between job descriptions.
- Built and compared Ridge Regression models using structured features, textual features and their combination.

---

## Salary Prediction Results

Five Ridge Regression configurations were evaluated using cross-validation.

| Model | MAE (RUB) | MAPE |
|---|---:|---:|
| Structured features | 36,460 | 32.07% |
| Structured features (log target) | 35,489 | 28.71% |
| Text features (TF-IDF) | 33,359 | 29.47% |
| Structured + text features | 31,297 | 27.12% |
| **Structured + text (log target)** | **29,877** | **23.79%** |

The best-performing model combined structured vacancy attributes with TF-IDF features and a logarithmic transformation of salary.

Compared with the structured-data baseline, this configuration reduced MAE by approximately **18.1%** and MAPE by **8.28 percentage points**.

The results demonstrate that textual information provides useful predictive signals beyond structured vacancy attributes.

---

## Statistical Findings

### Experience and Salary

Median salaries increased with required experience:

| Experience | Median Salary (RUB) |
|---|---:|
| No experience | 84,825 |
| 1–3 years | 104,400 |
| 3–6 years | 150,000 |
| More than 6 years | 200,000 |

The Kruskal–Wallis test confirmed statistically significant differences across experience groups (p < 0.001).

### PostgreSQL and Salary

Vacancies mentioning PostgreSQL had a median salary of **180,000 RUB**, compared with **110,000 RUB** for vacancies without this skill.

The Mann–Whitney U test indicated a statistically significant difference (p ≈ 4.5 × 10⁻¹³).

This association does not establish a causal salary premium, as vacancies may differ in professional roles, experience requirements and other characteristics.

---

## NLP and Clustering Insights

- TF-IDF and chi-square analysis identified words and skill combinations associated with different salary groups.
- Higher-paying vacancies were more frequently associated with terms related to development, projects, management and technical responsibilities.
- KMeans clustering was applied to approximately 14,000 job descriptions, with 10 clusters selected based on the evaluated silhouette scores.
- The low silhouette scores indicated weak cluster separation, suggesting that job descriptions overlap substantially in their vocabulary and content.

These findings illustrate both the potential and limitations of unsupervised text analysis for heterogeneous job market data.

---

## Technologies

Python, pandas, NumPy, scikit-learn, matplotlib, NLP, lemmatization, TF-IDF, Bag-of-Words, KMeans, Ridge Regression, statistical hypothesis testing

---

## Limitations

- Only vacancies with usable salary information were included in salary modelling.
- Salary figures represent advertised compensation rather than actual employee earnings.
- The dataset covers vacancies in Moscow and may not generalise to other labour markets.
- Differences in professional roles and industries may influence observed salary associations.
- Text clustering produced weakly separated groups.
- Salary prediction errors remain substantial, reflecting the complexity of compensation patterns and the limitations of available vacancy data.

---

## Conclusion

This project demonstrates an end-to-end analytical workflow, from collecting and cleaning job market data to statistical testing, NLP and machine learning.

Experience requirements and professional roles showed substantial associations with advertised salaries. Adding textual features improved Ridge Regression performance, while combining structured and textual features with a log-transformed target achieved the lowest prediction errors.

The project highlights how structured and unstructured data can complement each other in salary analysis, while also illustrating the importance of model evaluation and cautious interpretation of statistical results.

---
