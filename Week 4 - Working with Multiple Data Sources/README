# Week 4: Working with Multiple Data Sources (Merging, Joining, and Combining DataFrames)

## Overview

Week 4 focused on one of the most important responsibilities of a Data Engineer: combining data from multiple sources into a single, meaningful dataset. Using Pandas, I learned how to merge related datasets, concatenate multiple DataFrames, perform data analysis, and generate reports from combined data.

This week emphasized concepts that directly relate to SQL JOIN operations while demonstrating how to perform the same tasks using Python and Pandas.

---

## Topics Covered

- Loading multiple CSV files into Pandas
- Merging DataFrames with `pd.merge()`
- Understanding join types:
  - Inner Join
  - Left Join
  - Right Join
  - Outer Join
- Concatenating DataFrames using `pd.concat()`
- Sorting data with `sort_values()`
- Filtering rows using conditional statements
- Grouping and aggregating data with `groupby()`
- Creating calculated columns
- Exporting processed data to CSV

---

## Key Skills Learned

### DataFrame Merging

Combined multiple datasets using a common key (`server_id`) to enrich server inventory data with monitoring metrics and ownership information.

Example:

```python
server_report = pd.merge(servers, metrics, on="server_id")
server_report = pd.merge(server_report, owners, on="server_id")
```

---

### Understanding Join Types

Learned the differences between:

- Inner Join
- Left Join
- Right Join
- Outer Join

and how these concepts directly translate from SQL into Pandas.

---

### Concatenating DataFrames

Combined datasets with identical structures into a single DataFrame using:

```python
pd.concat()
```

This is commonly used when combining daily, weekly, or monthly log files.

---

### Filtering and Sorting

Filtered data based on server status and CPU usage.

Examples:

- Down servers
- High CPU servers
- Sorting CPU usage from highest to lowest

---

### Data Aggregation

Calculated average CPU usage by environment using:

```python
groupby()
mean()
```

---

### Feature Engineering

Created a new column named `health` based on CPU usage thresholds.

| CPU Usage | Health Status |
|-----------|---------------|
| 90% or higher | Critical |
| 80–89% | Warning |
| Below 80% | Healthy |

---

### Exporting Reports

Saved the final processed DataFrame as a CSV report using:

```python
to_csv()
```

---

# Mini Project

## Project: Multi-Source Server Health Report

### Objective

Build a complete server health report by combining information from multiple CSV files.

### Data Sources

- `servers.csv`
- `metrics.csv`
- `owners.csv`

### Tasks Completed

- Loaded multiple CSV files
- Merged server inventory with performance metrics
- Merged ownership information
- Filtered servers that were down
- Identified high CPU utilization servers
- Sorted CPU usage
- Calculated average CPU usage by environment
- Created a server health classification column
- Exported the completed report to CSV

---

## Skills Demonstrated

- Pandas
- DataFrame Merging
- DataFrame Concatenation
- Data Cleaning
- Filtering
- Sorting
- Grouping
- Aggregation
- Feature Engineering
- CSV Export

---

## Files Included

- Week 4 Lesson Notebooks
- Week 4 Mini Project Notebook
- `servers.csv`
- `metrics.csv`
- `owners.csv`
- `server_health_report.csv`
- `README.md`

---

## What I Learned

This week helped me understand how data engineers combine multiple datasets into a single source of truth. I learned when to use `merge()` versus `concat()`, how different join types affect the resulting data, and how to transform and analyze combined datasets using Pandas.

I also strengthened my understanding of how SQL JOIN concepts translate directly into Python, making it easier to work with real-world ETL workflows.

---

## Technologies Used

- Python 3
- Pandas
- Jupyter Notebook
- CSV Files

---

## Next Steps

In Week 5, I will begin working with real-world messy datasets by learning how to:

- Handle missing values
- Remove duplicate records
- Standardize inconsistent data
- Parse and convert dates
- Prepare raw datasets for analysis and ETL pipelines

These skills will further develop my ability to build production-ready data engineering workflows.
