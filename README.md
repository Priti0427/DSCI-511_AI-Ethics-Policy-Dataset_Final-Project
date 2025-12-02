# **AI Ethics & Policy Dataset Scrapping**

This repository contains all notebooks, data, and documentation used to build a unified global dataset of AI policies and ethics initiatives.
The project integrates information from OECD, UNESCO, and the White House OSTP to support research and analysis of worldwide AI governance efforts.

---

## **Repository Contents**

### **1. Notebooks**

- **Part_1_Data_scrapping_OECD.ipynb** – Scrapes, Cleans and preprocesses the original OECD dataset; removes low-quality columns; normalizes fields; prepares dataset for enrichment.
- **Part_2_data_scrapping_UNESCO_WhiteHouse.ipynb** – Scrapes and integrates UNESCO and OSTP policy documents; standardizes them to the OECD schema; saves final enriched dataset.

### **2. Presentation**

- **Project-Presentation-FINAL.pptx** – Summary of project goals, methodology, data sources, workflow, and results. Includes team roles, access rights, issues and limitations, and future work.

---

## **Project Overview**

This project compiles and enriches a global dataset of AI policy and ethics documents to enable systematic comparison, visualization, and analysis of AI governance trends.

The dataset:

- Integrates trusted global sources (OECD, UNESCO, White House OSTP)
- Provides a unified view of AI governance efforts
- Supports research into transparency, accountability, fairness, and responsible AI
- Helps analyze global AI policy approaches and trends

---

## **Data Sources**

Our dataset draws exclusively from publicly accessible and authoritative sources:

### **OECD AI Policy Observatory**

- Provides a structured catalog of national AI initiatives
- Downloaded directly as a CSV from OECD’s open data repository
- Forms the base dataset (52 columns before cleaning)

### **UNESCO – Recommendation on the Ethics of Artificial Intelligence**

- The UNESCO webpage blocked HTML scraping (403 Forbidden)
- We therefore used the **official UNESDOC Catalogue API** to retrieve clean metadata
- Extracted fields include title, publication year, languages, document code, and license information
- Standardized to OECD’s schema during merging

### **White House OSTP – Blueprint for an AI Bill of Rights**

- Scraped directly from the Biden White House Archives HTML page
- Collected title, publication date, description, and metadata
- PDF version downloaded separately via official OSTP storage link

---
## **Technologies Used** :
- Python for data collection and processing
- Web APIs for automated data retrieval
- Beautiful Soup (Python library) for web scraping and HTML parsing

## **Approach & Workflow**

### **1. Data Scrapping and Cleaning (OECD Dataset)**
Documented in Part_1_Data_scrapping_OECD.ipynb:

- Inspected missing values
- Removed columns with >60% missing entries
- Standardized text fields and filled missing values
- Normalized date formats
- Removed duplicates
- Produced `oecd_policies_clean.csv` with 26 final columns

### **2. Enrichment with UNESCO & OSTP**

Documented in Part_2_Data_scrapping_UNESCO_WhiteHouse.ipynb:

- Queried UNESCO via API
- Scraped OSTP HTML
- Created rows using **matching OECD schema**
- Deduped using `policy_initiative_id`
- Appended to the cleaned dataset
- Verified by loading updated CSV and checking final rows (UNESCO + OSTP appear at the bottom)

### **3. Standardization**

Across all sources:

- Unified names (`english_name`, `original_name(s)`, `responsible_organisation(s)`)
- Converted publication years → `start_date`
- Added consistent theme categories
- Preserved traceability by storing official URLs

---

## **Final Output**

The final dataset includes:

- Combination of the data scrapped from three sources

It provides a unified, analysis-ready resource for:

- Exploratory data analysis
- Visualization
- NLP / topic modeling
- Comparative policy research
- AI governance benchmarking

---

## **Usage & Access Rights**

All data sources are publicly accessible:

- OECD open data
- UNESCO Open Access policy
- U.S. government public domain policy documents

---

## **Future Improvements**

- Add EU, non-OECD, and private-sector policies
- Automate PDF text extraction for NLP
- Add language detection + translation
- Expand dataset filtering for multilingual research

## Team Members:
- Priti Sagar(pp693@drexel.edu)
- Leili Massoum Zadeh (lm3662@drexel.edu)
- Mohammad Husnain Sikandar (ms5875@drexel.edu)
- Nikhil Anil(na3236@drexel.edu)
