# Python-Pandas-Seaborn-Matplt

# India Industrial Development Analysis Project

An end-to-end data analytics and statistical exploratory profiling project leveraging Python to assess and optimize performance, employment footprint, investment distributions, and environmental impact across diverse industrial landscapes in India.

## 📌 Project Overview
This repository contains a comprehensive data analysis pipeline that transforms raw, unpolished industrial metadata into actionable statistical insights. The analytical workflow incorporates meticulous data cleansing, segment imputation, categorical typing corrections, and correlative behavior mapping.

## 📊 Dataset Profile & Features
The core dataset (`Industrial Development.csv`) contains **15,500 observation rows** tracking industrial performance with the following key attributes:

* **Categorical Context**: `State`, `Industry_Type`
* **Temporal Footprint**: `Year`
* **Operational Scale Metrics**: `Industrial_Output_Crore`, `Factories_Count`
* **Socio-Economic Indicators**: `Employment_Lakh`, `Investment_Crore`, `Export_Crore`
* **Resource & Environment Footprint**: `Electricity_Consumption_GWh`, `Pollution_Index`

## 🛠️ Tech Stack & Libraries
* **Python 3.x**
* **Pandas**: High-performance structured data operations and transformations.
* **NumPy**: Vectorized data arrays and statistical handling.
* **Matplotlib**: Low-level custom visualization layouts.
* **Seaborn**: High-level statistical visualization and feature correlation plotting.

## 📈 Data Pipeline Architecture & Implementation
The analysis executed within the Jupyter Notebook follows a structured engineering workflow:

1. **Exploratory Assessment**: Loading datasets, inspecting dimensional shape boundaries, and verifying feature data type mapping (`df.info()`).
2. **Missing Value Analysis**: Diagnosing systematic omissions across key operational pillars (averaging ~460 null items per field).
3. **Deduplication Engine**: Detecting and pruning redundant data records natively to secure unique rows.
4. **Data Type Correction**: Restructuring numerical and continuous values masquerading as object strings back into accessible numeric arrays.
5. **Statistical Imputation & Integrity**:
    * Imputing discrete temporal features (`Year`) and continuously skewed segments using mean/median bounds.
    * Converting temporal floats (`2024.0`) to canonical integer dates (`2024`).
    * Imputing missing categorical string labels (`Industry_Type`) safely under an `"Unknown"` classification banner to guarantee data preservation.
6. **Feature Interdependence Mapping**: Building a mathematical correlation matrix using `.corr(numeric_only=True)` to assess macro relationships between output scale, factory volumes, energy footprint, and emissions indexes.
7. **Pipeline Output**: Exporting a pristine, high-fidelity source data structure (`industrial_development_india_cleaned.csv`) for secondary BI dashboard ingestion.

## 🚀 How To Run The Project

### Prerequisites
