# Week 3: Data Transformation with Pandas

## Overview

This project demonstrates fundamental data transformation techniques using Python and Pandas. Data transformation is a critical part of the ETL (Extract, Transform, Load) process and is used to clean, standardize, and prepare data for analysis, reporting, and storage.

During this week of my Python for Data Engineering Bootcamp, I practiced common data engineering tasks including data cleaning, handling missing values, data type conversions, conditional transformations, sorting, and aggregation.

---

## Learning Objectives

By completing this project, I learned how to:

- Rename columns for consistency and readability
- Create new columns from existing data
- Apply conditional logic using `.loc`
- Clean and standardize text data
- Identify and handle missing values
- Convert data types using `.astype()`
- Sort datasets using `sort_values()`
- Aggregate and summarize data using `groupby()`

---

## Technologies Used

- Python 3
- Pandas
- Jupyter Notebook

---

## Key Concepts Practiced

### Column Renaming

Used `rename()` to standardize column names and improve readability.

```python
df.rename(columns={"Server Name": "server"})
```

### Creating New Columns

Generated new fields based on existing data.

```python
df["cpu_remaining"] = 100 - df["cpu_usage"]
```

### Conditional Transformations

Applied business rules using `.loc`.

```python
df.loc[df["cpu_usage"] >= 90, "cpu_status"] = "Critical"
```

### Text Cleaning

Standardized server names by removing whitespace and converting text to uppercase.

```python
df["server"] = df["server"].str.strip().str.upper()
```

### Handling Missing Values

Identified missing values and replaced them with default values.

```python
df["cpu_usage"] = df["cpu_usage"].fillna(0)
```

### Data Type Conversion

Converted string-based numeric data into integers for calculations.

```python
df["cpu_usage"] = df["cpu_usage"].astype(int)
```

### Sorting Data

Sorted servers by resource utilization.

```python
df.sort_values("cpu_usage", ascending=False)
```

### Grouping and Aggregation

Calculated average CPU usage by server status.

```python
df.groupby("status")["cpu_usage"].mean()
```

---

## Mini Project: Server Monitoring Data Transformation

### Scenario

A server monitoring dataset contained:

- Inconsistent server naming conventions
- Missing CPU utilization values
- CPU usage stored as text instead of numeric values

### Transformations Performed

1. Cleaned server names using string methods
2. Replaced missing values with default values
3. Converted CPU usage from strings to integers
4. Created CPU health categories:
   - Critical (>= 90%)
   - Warning (>= 70%)
   - Normal (< 70%)
5. Sorted servers by CPU utilization
6. Calculated average CPU usage by server status

### Sample Results

| Server | Status | CPU Usage | CPU Status |
|----------|----------|----------|----------|
| WEB02 | Down | 92 | Critical |
| WEB03 | Down | 70 | Warning |
| WEB01 | Up | 55 | Normal |
| DB01 | Up | 0 | Normal |

### Average CPU Usage by Status

| Status | Average CPU Usage |
|----------|----------|
| Down | 81.0 |
| Up | 27.5 |

---

## Skills Demonstrated

- Data Cleaning
- Data Transformation
- Data Quality Management
- Pandas DataFrames
- ETL Preparation
- Conditional Logic
- Aggregation and Reporting
- Data Engineering Fundamentals

---

## Key Takeaways

This project strengthened my ability to clean, transform, and summarize data using Pandas. These skills are essential for preparing raw data for analytics, reporting, dashboards, and downstream ETL pipelines. Through hands-on exercises and a server monitoring mini project, I gained practical experience with common data engineering workflows used in real-world environments.

---

## Next Steps

Week 4 will focus on combining data from multiple sources using:

- Merging DataFrames
- Joining DataFrames
- Concatenating DataFrames
- Real-world ETL data integration techniques

---

## Author

**LaQuandra Missick**  
Master of Information Technology Graduate  
Aspiring Data Engineer
