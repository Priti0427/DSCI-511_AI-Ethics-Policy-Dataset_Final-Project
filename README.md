# 📘 **AI Ethics & Policy Dataset Project**

*A DSCI-511 Final Project*

This repository contains all notebooks, data, and documentation used to build a unified global dataset of AI policies and ethics initiatives.
The project integrates information from OECD, UNESCO, and the White House OSTP to support research and analysis of worldwide AI governance efforts.

---

## 📂 **Repository Contents**

### **1. Notebooks**

* **Data-formatting.ipynb** – Cleans and preprocesses the original OECD dataset; removes low-quality columns; normalizes fields; prepares dataset for enrichment. 
* **data-UNESCO-WhiteHouse.ipynb** – Scrapes and integrates UNESCO and OSTP policy documents; standardizes them to the OECD schema; saves final enriched dataset. 

### **2. Presentation**

* **Project-Presentation-FINAL.pptx** – Summary of project goals, methodology, data sources, workflow, and results. Includes team roles, access rights, issues and limitations, and future work. 

### **3. Data Folder**

Contains:

* Raw OECD CSV
* Cleaned `oecd_policies_clean.csv`
* Downloaded policy PDFs (UNESCO/OSTP)
* Generated metadata files

---

## 🎯 **Project Overview**

This project compiles and enriches a global dataset of AI policy and ethics documents to enable systematic comparison, visualization, and analysis of AI governance trends.

According to the *Overview* slide (page 2 of the presentation), the dataset:

* Integrates trusted global sources (OECD, UNESCO, White House OSTP)
* Provides a unified view of AI governance efforts
* Supports research into transparency, accountability, fairness, and responsible AI
* Helps analyze global AI policy approaches and trends 

---

## 🗂 **Data Sources**

Our dataset draws exclusively from publicly accessible and authoritative sources:

### **OECD AI Policy Observatory**

* Provides a structured catalog of national AI initiatives
* Downloaded directly as a CSV from OECD’s open data repository
* Forms the base dataset (52 columns before cleaning)

### **UNESCO – Recommendation on the Ethics of Artificial Intelligence**

* The UNESCO webpage blocked HTML scraping (403 Forbidden)
* We therefore used the **official UNESDOC Catalogue API** to retrieve clean metadata
* Extracted fields include title, publication year, languages, document code, and license information
* Standardized to OECD’s schema during merging
  (Document acquisition method described on page 9 of the presentation) 

### **White House OSTP – Blueprint for an AI Bill of Rights**

* Scraped directly from the Biden White House Archives HTML page
* Collected title, publication date, description, and metadata
* PDF version downloaded separately via official OSTP storage link

---

## 🔧 **Approach & Workflow**

### **1. Data Cleaning (OECD Dataset)**

As documented in *Data-formatting.ipynb* (pages 1–16):

* Inspected missing values
* Removed columns with >60% missing entries
* Standardized text fields and filled missing values
* Normalized date formats
* Removed duplicates
* Produced `oecd_policies_clean.csv` with 26 final columns 

### **2. Enrichment with UNESCO & OSTP**

Based on *data-UNESCO-WhiteHouse.ipynb*:

* Queried UNESCO via API
* Scraped OSTP HTML
* Created rows using **matching OECD schema**
* Deduped using `policy_initiative_id`
* Appended to the cleaned dataset
* Verified by loading updated CSV and checking final rows (UNESCO + OSTP appear at the bottom) 

### **3. Standardization**

Across all sources:

* Unified names (`english_name`, `original_name(s)`, `responsible_organisation(s)`)
* Converted publication years → `start_date`
* Added consistent theme categories
* Preserved traceability by storing official URLs

---

## 📊 **Final Output**

The final dataset includes:

* **OECD policies** (cleaned)
* **UNESCO AI Ethics Recommendation**
* **White House OSTP AI Bill of Rights**

It provides a unified, analysis-ready resource for:

* Exploratory data analysis
* Visualization
* NLP / topic modeling
* Comparative policy research
* AI governance benchmarking

---

## 🔐 **Usage & Access Rights**

All data sources are publicly accessible:

* OECD open data
* UNESCO Open Access policy
* U.S. government public domain policy documents
  (Referenced on page 10 of the presentation) 

---

## 🚀 **Future Improvements**

As suggested on page 12 of the presentation:

* Add EU, non-OECD, and private-sector policies
* Automate PDF text extraction for NLP
* Add language detection + translation
* Expand dataset filtering for multilingual research 


