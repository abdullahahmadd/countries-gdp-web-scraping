# 🌍 Countries GDP Web Scraping & Data Analysis
### IBM Data Engineering Specialization – Portfolio Project

![Visitors](https://visitor-badge.laobi.icu/badge?page_id=yourusername.yourreponame)
![Web Scraping](https://img.shields.io/badge/Web%20Scraping-Data%20Extraction-orange?style=for-the-badge&logo=webflow&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Google Colab](https://img.shields.io/badge/Google%20Colab-F9AB00?style=for-the-badge&logo=google-colab&logoColor=white)
![BeautifulSoup](https://img.shields.io/badge/BeautifulSoup-HTML%20Parsing-6DB33F?style=for-the-badge&logo=leaflet&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)

---

# 📑 Table of Contents

- [📌 Overview](#-overview)  
- [🧠 Skills Demonstrated](#-skills-demonstrated)  
- [🛠️ Tools & Technologies](#️-tools--technologies)  
- [📚 Libraries Used](#-libraries-used)  
- [🌐 Data Source](#-data-source)  
- [📊 Final Output Summary](#-final-output-summary)  
- [🖼️ Results](#️-results)  
- [📥 How to Use](#-how-to-use)  
- [📎 Summary](#-summary)  

---

## 📌 Overview

This project demonstrates the use of **web scraping techniques** to extract nominal GDP data from an archived Wikipedia webpage. The scraped data is cleaned, structured, transformed, and analyzed to identify the top 10 largest economies in the world. The main focus is on working directly with **raw HTML content**, extracting meaningful information, and converting it into a usable analytical dataset.

The project workflow includes:

- Extracting GDP data from an HTML table using **manual web scraping**
- Parsing and structuring HTML content into a Pandas DataFrame
- Cleaning and converting GDP values from millions to billions
- Selecting the **top 10 economies** based on nominal GDP
- Engineering analytical fields:
  - GDP Share (%)
  - GDP Ranking
  - Normalized GDP Score (0–1)
- Exporting the final dataset for further analysis and use

---

## 🧠 Skills Demonstrated

- Web Scraping & HTML Parsing  
- Data Cleaning and Transformation  
- Exploratory Data Analysis  
- Feature Engineering  
- Tabular Data Analysis  

---

## 🛠️ Tools & Technologies

- Python  
- Google Colab / Jupyter Notebook  
- Web Scraping Techniques  

---

## 📚 Libraries Used

- **BeautifulSoup (bs4)** – HTML parsing and table extraction  
- **urllib.request** – Fetching webpage content  
- **Pandas** – Structuring and transforming tabular data  
- **NumPy** – Mathematical operations and normalization  

---

## 🌐 Data Source

Archived Wikipedia Nominal GDP Table:  
https://web.archive.org/web/20230902185326/https://en.wikipedia.org/wiki/List_of_countries_by_GDP_(nominal)

---

## 📊 Final Output Summary

The final processed dataset contains:

- Country  
- GDP (Million USD)  
- GDP (Billion USD)  
- GDP Share (%)  
- Rank  
- GDP Normalized Score  

This dataset provides a clear comparative view of the economic standing of the top 10 largest economies.

---

## 🖼️ Results

Below are visual snapshots of key stages from the analysis.  
*(All images are stored inside the `web_scraping_results/` folder.)*

### ✔ Extracting Nominal GDP Data  
![Extracting GDP](web_scraping_results/Extracting_Nominal_GDP_Data.png)

### ✔ Cleaning Data & Removing Aggregates  
![Removing Aggregates](web_scraping_results/Removing_Aggregate_Rows.png)

### ✔ Top 10 Largest Economies  
![Top 10](web_scraping_results/Top_10_Largest_Economies.png)

### ✔ Converting GDP to Billions  
![GDP Billions](web_scraping_results/Converting_GDP_to_Billion_USD.png)

### ✔ Adding GDP Share (%)  
![GDP Share](web_scraping_results/Adding_GDP_Share.png)

### ✔ Ranking the Economies  
![Ranking](web_scraping_results/Adding_Ranking.png)

### ✔ Normalized GDP Score  
![Normalized Score](web_scraping_results/Adding_Normalized_Score.png)

---

## 📥 How to Use

1. Open the `.ipynb` notebook in Google Colab or Jupyter Notebook.  
2. Run all cells to reproduce the scraping and analysis pipeline.  
3. View or download the processed dataset (`Largest_economies.csv`).  
4. Refer to the `web_scraping_results` folder for result images and outputs.

---

## 📎 Summary

This project demonstrates an end-to-end data workflow involving:

- Web scraping from an online source  
- Cleaning and transforming real-world economic data  
- Engineering additional insights  
- Exporting a structured and analytical dataset  

It serves as a professional portfolio example highlighting practical **web scraping**, **data preparation**, and **analytical** skills.

---
