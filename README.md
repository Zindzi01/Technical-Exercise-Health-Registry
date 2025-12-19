# Technical-Exercise-Health-Registry
National Health Facility Registry – Data Cleaning & Profiling
Project Overview
This repository contains a reproducible data profiling and cleaning pipeline for a synthetic National Health Facility Registry. The dataset consolidates health facility records from multiple administrative sources and is prepared for analytics, knowledge graph construction, and Retrieval-Augmented Generation (RAG) applications.

Repository Structure
.
├── notebooks/
│   └── health_registry_eda_clean.ipynb
├── data/
│   ├── raw/
│   │   └── health_registry.csv
│   └── processed/
│       └── cleaned_health_registry.csv
├── README.md
└── Documentation.txt


How to Run the Notebook
Ensure Python 3.x is installed.


Install required dependencies:

 pip install pandas numpy matplotlib seaborn missingno


Open the notebook in VS Code or Jupyter:

 notebooks/health_registry_eda_clean.ipynb


Update the file path in the notebook to point to the raw CSV if necessary.


Run all cells sequentially to reproduce the analysis and generate the cleaned dataset.



Key Assumptions & Decisions
The dataset is synthetic and contains no real patient or facility data.


A facility is uniquely identified by the combination of facility_name and region due to incomplete facility_id coverage.


Exact duplicates were removed entirely.


Logical duplicates were resolved by retaining the most recent record.


Missing categorical values were filled with "Unknown" where appropriate.


Capacity values were converted to numeric where possible; non-numeric values were retained as missing rather than defaulted to zero.



Outputs
health_registry_eda_clean.ipynb – Fully reproducible profiling and cleaning notebook


cleaned_health_registry.csv – Analytics-ready, deduplicated dataset



