# Job Market Salary Analysis Using NLP and Machine Learning

---

## Project Overview

This project analyzes job vacancies and salary patterns using a combination of statistical analysis, natural language processing, and machine learning.

The goal is to identify key factors influencing salary levels and evaluate how textual job descriptions improve salary prediction compared to structured data alone.

---

## Key Results

- Experience level is the strongest predictor of salary.
- Job roles significantly influence salary differences.
- Textual features improve salary prediction models.
- High-paying jobs are associated with managerial and technical responsibilities.
- Salary is primarily determined by job complexity and level of responsibility rather than the volume of job description.

---

## Methods

- Data collection via public job API  
- Data cleaning and preprocessing  
- Exploratory Data Analysis (EDA)  
- Hypothesis testing (Mann–Whitney U, Kruskal–Wallis tests)  
- Natural Language Processing (lemmatization, TF-IDF)  
- Unsupervised learning (KMeans clustering)  
- Supervised learning (Ridge Regression)  

---

## Dataset

- Source: Job vacancies from a public job platform (hh.ru)  
- Location: Moscow  
- Data includes structured features (experience, employment type, schedule, role) and textual data (job titles, descriptions, and skills)

---

## What I Did

- Built an end-to-end data analysis pipeline  
- Collected and processed real-world job market data  
- Performed statistical analysis to identify significant factors affecting salary  
- Applied NLP techniques to extract insights from job descriptions  
- Developed and compared multiple machine learning models  
- Evaluated the impact of textual features on salary prediction  

---

## Technologies

Python, pandas, NumPy, scikit-learn, NLP, TF-IDF, statistical testing, machine learning

---

## Insights

- Salaries increase with experience, but with overlapping distributions across levels  
- Professional roles significantly differentiate salary levels  
- Technical and managerial skills are associated with higher salaries  
- Job descriptions contain meaningful signals about compensation and job complexity  
- Combining structured and textual data improves model performance  

---

## Limitations

- Only vacancies with specified salaries were included in the analysis  
- Data reflects employer expectations, not actual salary outcomes  
- Potential imbalance across industries  
- Text analysis does not capture implicit context or nuances in job descriptions  

---

## Conclusion

This project demonstrates how combining structured data with NLP techniques can significantly improve salary analysis and prediction. The results show that job characteristics, professional roles, and textual descriptions all contribute to explaining salary differences in the job market.

---
