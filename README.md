# The Schizophrenia of Global Food Safety
**A Comparative Longitudinal Analysis of US-FDA and EU-RASFF Enforcement Personalities (2008-2025)**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python](https://img.shields.io/badge/python-3.13.3%2B-blue)](https://www.python.org/)
[![Status](https://img.shields.io/badge/Status-Submitted-green)](https://github.com/)
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.17931263.svg)](https://doi.org/10.5281/zenodo.17931263)

## 📄 Overview
This repository contains the source code, data processing pipelines, and statistical analysis for the research paper: **"The Schizophrenia of Global Food Safety."**

This study provides a comparative longitudinal analysis of **102,451 regulatory border actions** recorded by the US Food and Drug Administration (FDA) and the EU Rapid Alert System for Food and Feed (RASFF) over a seventeen-year period (2008-2025). By harmonizing rejection data across trade sectors and hazard categories, we identify a structural divergence in regulatory risk perception between the two global hegemons.

## 💾 Data Availability
Due to GitHub's file size limits, the raw and processed CSV datasets are hosted externally. 
**👉 [CLICK HERE TO DOWNLOAD THE FULL DATASET (ZIP)](https://drive.google.com/file/d/1lrvAOgKGiK5Mp0zWuzJSI2m7D1XmFv6W/view?usp=sharing)**

*The ZIP file contains:*
* `food_refusals_complete.csv` (Previously cleaned FDA Data)
* `RASFF_Alert_Notifications_Cleaned.csv` (Previously cleaned RASFF Data)
* `FDA_Import_Refusals_Human_Foods_harmonized.csv` (Processed)
* `RASFF_Alert_Notifications_harmonized.csv` (Processed)

---

## 📂 Repository Structure

The analytical framework is divided into two phases: **Individual System Assessment** (Phase 1) and **Comparative Harmonization** (Phase 2).

### 🔹 Phase 1: Individual System Analysis (Baseline)
*Foundational exploratory analysis of each regulatory system in isolation.*
* **`FDA_Import_Food_Refusals_Audit.ipynb`**: Detailed breakdown of FDA "Refusals" by product code, port of entry, and violation charge (2001–2025).
* **Repository Address**: **[FDA-Import-Refusal-Audit](https://github.com/shafinahamed9/.git)**
* **`RASFF_Alert_Analysis.ipynb`**: Detailed breakdown of RASFF "Notifications" by notification type (Alert/Border Rejection) and risk decision.
* **Repository Address**: **[RASFF-Food-Safety-Alerts-Analysis](https://github.com/shafinahamed9/.git)**

### 🔹 Phase 2: Comparative Analysis (The Paper)
*The core code used to generate the findings and figures in the manuscript.*

#### 1. `EU_US_Data_Harmonization.ipynb` (The Engine)
This notebook handles the ETL (Extract, Transform, Load) process to ensure functional equivalence between the systems.
* **Data Cleaning:** Filters FDA data to "Human Food" (Industry 02-42) and RASFF data to "Border Rejections" only.
* **Harmonization:** Maps disparate product codes (US Product Code vs. EU CN Codes) into unified Trade Sectors (e.g., Seafood, Nuts & Seeds).
* **Hazard Mapping:** Implements a "Many-to-One" dictionary to categorize violation charges into **7 Harmonized Hazard Classes** (separating "Natural Toxins" from generic "Chemicals").

#### 2. `EU_US_Data_Visualization.ipynb` (The Visuals)
This notebook generates the statistical tables and figures for the publication.
* **Sector Inversion (Table 2):** Calculates the procedural divergence in high-volume sectors.
* **Geopolitical Mapping (Figure 3):** Visualizes the "Neighborhood Bias" (Mexico/Turkey), the "India Paradox" and the Global Giant "China".
* **Hazard Distribution (Figure 4):** Plots the distribution of the 7 hazard categories to identify the "Toxicological Sentinel" vs. "Hygiene Police" dynamic.

---

## 🛠️ Dependencies
The analysis requires the following Python libraries:
* `pandas` (Data manipulation)
* `numpy` (Numerical operations)
* `matplotlib` & `seaborn` (Visualization)

## 📜 Citation
If you use this code or methodology in your research, please cite the accompanying paper:

> **Ahamed, M. S.** (2025). *The Hidden Borders of Global Trade: Divergent Regulatory Personalities in the US and EU Food Safety Systems (2008-2025)* [Journal Name - Under Review].

## 📧 Contact
**Md Shafin Ahamed, Dhaka Polytechnic Institute (DPI)**  
E-Mail: shafinahamedalif@gmail.com 
