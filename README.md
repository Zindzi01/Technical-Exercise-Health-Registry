# Technical Exercise – Health Registry  
**National Health Facility Registry: Data Cleaning & Profiling**

---

## Project Overview

This repository contains a fully reproducible data profiling and cleaning pipeline for a **synthetic National Health Facility Registry**.  
The dataset consolidates health facility records from multiple administrative sources and has been prepared for downstream analytics, **knowledge graph construction**, and **Retrieval-Augmented Generation (RAG)** applications.

---
## Repository Structure

.

├── notebooks/

│           └── health_registry_eda_clean.ipynb

├── data/

│            ├── raw/

│            │     └── health_registry.csv

│            └── processed/

│                 └── cleaned_health_registry.csv

├── README.md

└── Documentation.txt


---

## How to Run the Notebook

1. Ensure **Python 3.x** is installed.

2. Install the required dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn missingno
   
Open the notebook in VS Code or Jupyter Notebook:


1. Copy code
notebooks/health_registry_eda_clean.ipynb

2. Update the file path in the notebook if necessary to point to the raw CSV file.

3. Run all cells sequentially to reproduce the exploratory analysis and generate the cleaned dataset.

## Key Assumptions & Decisions
1. The dataset is synthetic and contains no real patient or facility data.

2. A facility is uniquely identified using a composite key of facility_name and region, due to incomplete coverage of facility_id.

3. Exact duplicate records were removed entirely.

4. Logical duplicates were resolved by retaining the most recent record.

5. Missing categorical values were filled with "Unknown" where appropriate.

6. Capacity values were converted to numeric where possible; non-numeric values were retained as missing rather than defaulted to zero.

## Outputs
health_registry_eda_clean.ipynb
Fully reproducible exploratory data analysis and cleaning notebook.

## Loom Video Explanation

cleaned_health_registry.csv
Analytics-ready, deduplicated dataset suitable for downstream use.
