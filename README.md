Technical Exercise – Health Registry

National Health Facility Registry: Data Cleaning & Profiling

Project Overview

This repository contains a fully reproducible data profiling and cleaning pipeline for a synthetic National Health Facility Registry.
The dataset consolidates health facility records from multiple administrative sources and has been prepared for downstream analytics, knowledge graph construction, and Retrieval-Augmented Generation (RAG) applications.

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
└── Documentation.pdf

How to Run the Notebook

Ensure Python 3.x is installed.

Install the required dependencies:

pip install pandas numpy matplotlib seaborn missingno


Open the notebook in VS Code or Jupyter Notebook:

notebooks/health_registry_eda_clean.ipynb


Update the file path in the notebook if necessary to point to the raw CSV file.

Run all cells sequentially to reproduce the exploratory analysis and generate the cleaned dataset.

Key Assumptions & Decisions

The dataset is synthetic and contains no real patient or facility data.

A facility is uniquely identified using a composite key of facility_name and region, due to incomplete coverage of facility_id.

Exact duplicate records were removed entirely.

Logical duplicates were resolved by retaining the most recent record.

Missing categorical values were filled with "Unknown" where appropriate.

Capacity values were converted to numeric where possible; non-numeric values were retained as missing rather than defaulted to zero.

Outputs

health_registry_eda_clean.ipynb
Fully reproducible exploratory data analysis and cleaning notebook.

cleaned_health_registry.csv
Analytics-ready, deduplicated dataset suitable for downstream use.
