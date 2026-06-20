# Week 2 - Pandas for Data Engineering

## Objective
Learn how to use Pandas to read, analyze, clean, and summarize tabular data.

## Skills Demonstrated
- Reading CSV files with Pandas
- Creating DataFrames
- Filtering rows
- Sorting data
- Creating new columns
- GroupBy aggregations
- Value counts
- Missing value detection
- Removing duplicates

## Files
- server_health_analysis.ipynb
- server_health.csv

## Key Concepts Learned

### Reading Data
```python
pd.read_csv()
```

### Filtering Data
```python
df[df["status"] == "Down"]
```

### Grouping Data
```python
df.groupby("team")["cpu"].sum()
```

### Data Cleaning
```python
df.drop_duplicates()
df.isnull().sum()
```

## Project Summary
Created a server health analysis project that:
- Identified down servers
- Flagged high CPU utilization
- Calculated team-level CPU statistics
- Generated summary reports using Pandas

## Technologies Used
- Python
- Pandas
- Jupyter Notebook
