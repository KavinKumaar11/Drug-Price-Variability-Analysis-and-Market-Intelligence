# 💊 Drug Price Variability Analysis & Market Intelligence

A healthcare data analytics project that investigates the root causes of prescription drug price variation across the U.S., leveraging manual web scraping, Google Gemini-powered OCR extraction, and advanced data analysis techniques. 

This project identifies **pricing disparities** for 15 high-impact medications across **pharmacies** and **ZIP codes**, with a particular emphasis on **Type 2 Diabetes** treatments. The goal is to support healthcare transparency initiatives and enable smarter pharmaceutical policy and purchasing decisions.

---

## 🔍 Project Overview

Prescription drug prices in the U.S. are notoriously inconsistent. Even within a single ZIP code, two pharmacies may charge drastically different prices for the same medication. This project answers:

> 💡 **What drives drug price variability more — geographic location or pharmacy choice?**

To explore this, we:
- Collected pharmacy pricing data for 15 top-selling and clinically significant medications.
- Used GenAI (Gemini Flash 2.0) to extract structured pricing data from screenshots.
- Performed pharmacy-level and region-level statistical analysis.
- Outlined a data model for a future interactive dashboard.

---

## 📦 Dataset Creation

### ✅ Drug Selection Criteria
Selected 15 high-impact drugs by analyzing:
- **AARP Top Drugs by U.S. Spending**
- **PharmaShots Prescription Revenue Rankings**
- **Drug Discovery Trends Blockbusters**

These drugs include:  
**Semaglutide, Tirzepatide, Dulaglutide, Empagliflozin, Dapagliflozin, Insulin Glargine, Sitagliptin**, and more.

> Over 50% of the selected drugs treat **Type 2 Diabetes** and **obesity-related conditions**, driven by prevalence, chronic nature, limited generics, and media attention.

---

### 🖼️ Manual Data Collection (Scraping via Screenshots)

- Captured **150+ screenshots** from **GoodRx.com** across 5 ZIP codes:
  - `10001` (NYC), `30301` (Atlanta), `60601` (Chicago), `77001` (Houston), `90001` (Los Angeles)
- Screenshots organized per drug in the `goodrx_screenshots/` folder

---

### 🤖 Structured Data Extraction using GenAI

- Screenshots processed using **Google Gemini Flash 2.0**
- Extracted pharmacy names, ZIP codes, price, drug names
- Post-processed and normalized with custom Python scripts
- Final datasets:
  - `goodrx_full_output.xlsx` – raw extraction  
  - `goodrx_clean_output.xlsx` – cleaned, structured for analysis

---

## 📊 Analytical Workflow

Performed exploratory and statistical analysis using **Pandas**, **NumPy**, and **Matplotlib/Seaborn**:

- ✅ Calculated average and standard deviation per drug, pharmacy, and ZIP
- 📉 Identified **price outliers** using Z-score normalization
- 🏷️ Grouped by drug categories and region for insight clustering
- 📈 Drafted schema for Power BI dashboard with dynamic filters

---

## 📈 Key Insights

- **Pharmacy choice** (e.g., Walmart vs. Walgreens) affects price more than ZIP code.
- **Diabetes drugs** have the widest pricing variation — driven by brand protection, supply chain concentration, and lack of generics.
- In some ZIPs, independent pharmacies were cheaper than national chains.
- Urban areas did not consistently offer better affordability.

---

## 🗂️ Project Structure

```
Drug_Price_Variability_Analysis_and_Market_Intelligence/
├── Drug_Price_Variability_Analysis_and_Market_Intelligence.ipynb # Core notebook
├── Data/
│ ├── goodrx_full_output.xlsx # Raw output from Gemini
│ └── goodrx_clean_output.xlsx # Cleaned and analysis-ready
├── goodrx_screenshots/
│ ├── semaglutide/
│ ├── tirzepatide/
│ └── ... (13 other folders by drug name)
├── requirements.txt # Python package dependencies
├── LICENSE # MIT License
└── Readme.md
```
---

## 📊 Optional Power BI Dashboard (Design-Ready)

> Although the dashboard isn’t built in this repo, the analysis outlines a relational model with key metrics like:
- **Average price per ZIP**
- **Price disparity index**
- **Outlier pharmacy flags**
- Filters by drug, ZIP, and chain

---

## 💼 Skills Demonstrated

- 📌 **Data Collection** (Manual scraping strategy via screenshots)
- 🧠 **AI Integration** (OCR extraction via Gemini Flash 2.0)
- 🧹 **Data Cleaning & Normalization** (Excel + Python pipeline)
- 📊 **Statistical Analysis** (Z-score, descriptive stats)
- 📈 **Visualization + Reporting** (Matplotlib, Power BI schema)
- 🩺 **Domain Relevance** (Healthcare affordability + policy insight)

---

## 🚀 How to Reproduce

1. Clone the repo:
```bash
git clone https://github.com/yourusername/Drug_Price_Variability_Analysis.git
cd Drug_Price_Variability_Analysis
```
2. Open the Jupyter notebook:
```bash
jupyter notebook Drug_Price_Variability_Analysis_and_Market_Intelligence.ipynb
```
3. Follow each section step by step — or customize the drugs/ZIPs as needed.

---

## 📜 License

This project is released under the **MIT License**.

---

## 👨‍💼 Author

**Kavin Kumaar**  
Graduate Student – MS in Business Analytics & Project Management  
University of Connecticut  
[LinkedIn](https://www.linkedin.com/in/rtkavinkumaar22/) | [Github](https://github.com/KavinKumaar11) | [Email](mailto:rtkavinkumaar112219@gmail.com)

---

## 🙌 Acknowledgments

- **Data Source**: [GoodRx.com](https://www.goodrx.com/)
- **AI Extraction**: Google Gemini Flash 2.0
- **Visualization Tools**: Matplotlib, Power BI (Design Phase)

> *“In healthcare, transparency isn't optional — it's life-changing. This project is my contribution toward data-driven advocacy.”*

---

