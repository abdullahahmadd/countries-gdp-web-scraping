# Global GDP Data Web Scraping
### IBM Data Engineering Specialization - Portfolio Project

![Web Scraping](https://img.shields.io/badge/Web%20Scraping-Data%20Extraction-orange?logo=webflow&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![Google Colab](https://img.shields.io/badge/Google%20Colab-F9AB00?logo=google-colab&logoColor=white)
![BeautifulSoup](https://img.shields.io/badge/BeautifulSoup-HTML%20Parsing-6DB33F?logo=leaflet&logoColor=white)

---

## Table of Contents

- [Overview](#overview)
- [Objectives](#objectives)
- [Data Source](#data-source)
- [Tools & Technologies](#tools--technologies)
- [Methodology](#methodology)
- [Final Output Summary](#final-output-summary)
- [Results](#results)
- [Key Performance Indicators](#key-performance-indicators)
- [Key Findings](#key-findings)
- [How to Use](#how-to-use)

---

## Overview

This project uses web scraping to extract nominal GDP data from an archived Wikipedia webpage, then cleans, structures, transforms, and analyzes it to identify the top 10 largest economies in the world. The focus is on working directly with raw HTML content, extracting meaningful information, and converting it into a usable analytical dataset - covering GDP share, ranking, and a normalized comparison score.

---

## Objectives

- Extract GDP data from an HTML table using manual web scraping
- Parse and structure raw HTML content into a Pandas DataFrame
- Clean and convert GDP values from millions to billions
- Select the top 10 economies based on nominal GDP
- Engineer analytical fields: GDP Share (%), GDP Ranking, Normalized GDP Score (0-1)
- Export a clean, structured dataset for further analysis

---

## Data Source

Archived Wikipedia Nominal GDP table:
https://web.archive.org/web/20230902185326/https://en.wikipedia.org/wiki/List_of_countries_by_GDP_(nominal)

---

## Tools & Technologies

| Category | Tools |
|---|---|
| Language | Python |
| Environment | Google Colab / Jupyter Notebook |
| Libraries | BeautifulSoup (bs4), urllib.request, pandas, numpy |

---

## Methodology

**1. Extraction**
Scraped the nominal GDP table directly from the archived Wikipedia HTML page using BeautifulSoup and urllib.request, working with raw HTML content rather than a pre-cleaned API or CSV source.

**2. Cleaning**
Removed non-country aggregate rows (e.g., world/regional totals) and cleaned numerical GDP values to prepare them for structured analysis.

**3. Structuring**
Parsed the cleaned HTML content into a Pandas DataFrame and converted GDP values from millions to billions USD for readability.

**4. Selection**
Filtered the dataset down to the top 10 economies by nominal GDP.

**5. Feature Engineering**
Calculated GDP Share (%) relative to the top 10, assigned a GDP Rank from largest to smallest, and computed a Normalized GDP Score (0-1) using NumPy for comparative analysis.

**6. Export**
Exported the final structured dataset (`Largest_economies.csv`) for downstream use or further analysis.

---

## Final Output Summary

The final processed dataset contains:

| Field | Description |
|---|---|
| Country | Country name |
| GDP (Million USD) | Original scraped GDP value |
| GDP (Billion USD) | Converted GDP value for readability |
| GDP Share (%) | Share of GDP relative to the top 10 economies |
| Rank | Rank from largest to smallest nominal GDP |
| GDP Normalized Score | Scaled GDP value (0-1) for comparative analysis |

---

## Results

All screenshots in [`web_scraping_results/`](./web_scraping_results).

| # | Result | Screenshot |
|---|--------|------------|
| 1 | Extracting nominal GDP data - initial extraction from the archived HTML table | ![Extracting GDP](web_scraping_results/Extracting_Nominal_GDP_Data.png) |
| 2 | Cleaning data & removing aggregates - non-country rows removed, values cleaned | ![Removing Aggregates](web_scraping_results/Removing_Aggregate_Rows.png) |
| 3 | Top 10 largest economies - filtered to the top 10 countries by nominal GDP | ![Top 10](web_scraping_results/Top_10_Largest_Economies.png) |
| 4 | Converting GDP to billions - values converted from millions for readability | ![GDP Billions](web_scraping_results/Converting_GDP_to_Billion_USD.png) |
| 5 | Adding GDP share (%) - each country's share relative to the top 10 | ![GDP Share](web_scraping_results/Adding_GDP_Share.png) |
| 6 | Ranking the economies - ranked from largest to smallest nominal GDP | ![Ranking](web_scraping_results/Adding_Ranking.png) |
| 7 | Normalized GDP score - GDP values scaled 0-1 for comparative analysis | ![Normalized Score](web_scraping_results/Adding_Normalized_Score.png) |

---

## Key Performance Indicators

| KPI | Result |
|---|---|
| Economies Analyzed | Top 10 by nominal GDP |
| Engineered Fields | 3 (GDP Share %, Rank, Normalized Score) |
| Value Conversion | Millions to Billions USD |
| Score Normalization Range | 0-1 |

---

## Key Findings

- Direct HTML scraping of an archived source produced a clean, reproducible top-10 GDP ranking without relying on a pre-built API or dataset.
- Converting GDP values from millions to billions materially improved dataset readability for comparative analysis.
- The engineered GDP Share (%) field makes it possible to see each economy's relative weight within the top 10, not just its absolute GDP value.
- The 0-1 normalized GDP score provides a consistent basis for comparing economies of very different absolute sizes on the same scale.

---

## How to Use

1. Open the `.ipynb` notebook in Google Colab or Jupyter Notebook.
2. Run all cells to reproduce the scraping and analysis pipeline.
3. View or download the processed dataset (`Largest_economies.csv`).
4. Refer to the `web_scraping_results` folder for result images and outputs.

---
