# Data Wrangling & Analysis: Hospital Records 

##  Overview
This repository contains a Jupyter Notebook (`Assignment(4).ipynb`) that tackles a comprehensive data preprocessing pipeline for a hospital. Working with multiple datasets (patient info and billing details), this project resolves common real-world data issues such as missing values, duplicate entries from patient follow-ups, and fragmented data sources. 

The ultimate goal is to produce a clean, unified dataset ready for advanced analytics on department-wise revenue and doctor performance.

##  Key Skills & Operations Demonstrated

The notebook executes the following data wrangling tasks using `pandas`:

### 1. Data Cleaning & Subsetting
* **Initial Inspection:** Using `.info()` to generate high-level dataset summaries.
* **Feature Selection:** Subsetting the DataFrame to isolate relevant billing columns (`PatientID`, `Department`, `Doctor`, `BillAmount`).
* **Dimensionality Reduction:** Dropping irrelevant administrative columns (e.g., `ReceptionistID`, `CheckInTime`) to streamline the dataset.
* **Deduplication:** Removing duplicate patient rows based on `PatientID` to account for follow-up visits.
* **Data Imputation:** Handling missing `BillAmount` values by filling them with the statistical mean.

### 2. Data Aggregation
* **Grouping Data:** Utilizing `.groupby()` to calculate the total bill amount per department, providing a foundational metric for revenue tracking.

### 3. Data Integration (Merging & Concatenating)
* **Merging:** Joining the separate billing dataset with the main patient dataset using a common key (`PatientID`).
* **Row-wise Concatenation:** Appending a new DataFrame containing weekly new patient records to the bottom of the main dataset.
* **Column-wise Concatenation:** Adding new calculated/categorical billing columns (`InsuranceCovered`, `FinalAmount`) horizontally alongside the existing data.

## 🛠️ Technologies Used
* **Python 3**
* **Jupyter Notebook**
* **Libraries:** `pandas`
