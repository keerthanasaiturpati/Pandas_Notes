# Pandas Learning Notes & Practice

My pandas notes and practice — learning it for data analysis/manipulation as part of my ML/AI portfolio. Covers core concepts from scratch, applied on real datasets (Iris, Titanic, employee records, air quality data).

## Contents

| File | Description |
|---|---|
| `pandas_learn.ipynb` | Core concept-by-concept notes and practice — Series, DataFrames, indexing, filtering, cleaning, transforming, grouping, merging |
| `Pandas_Practice.ipynb` | Applied practice exercises on the Iris and Titanic datasets |
| `IRIS.csv` | Iris flower dataset |
| `Titanic-Dataset.csv` | Titanic passenger dataset |
| `employee_data.csv` / `employee_data.json` | Small employee records dataset (same data, two formats) |
| `raw_data.csv` | Sample dataset with missing values, used for data-cleaning practice |
| `globalAirQuality.csv` | Air quality dataset used for filtering, querying, and datetime practice |

## Topics Covered

### Data Structures
- Series (1D labeled array) vs DataFrame (2D labeled array)
- Creating Series/DataFrames from dicts, lists, and NumPy arrays
- Reading data from CSV and JSON (`read_csv`, `read_json`)

### Exploration
- `head()`, `tail()`, `sample()`, `info()`, `shape`, `describe()`, `columns`, `nunique()`

### Selecting & Indexing
- Column selection (`df["col"]` vs `df[["col1", "col2"]]`)
- Row/cell access with `loc`, `iloc`, `at`, `iat`
- Difference between label-based (`loc`) and position-based (`iloc`) indexing

### Filtering
- Boolean masking (`df[df["col"] > x]`)
- `query()` — string-expression filtering, `@` for referencing Python variables, chaining conditions

### Data Cleaning
- Missing values: `isnull()`, `isna()`, `dropna()`, `fillna()`, `ffill()`, `bfill()`
- Duplicates: `duplicated()`, `drop_duplicates()`
- Data types: `dtypes`, `astype()`, `to_datetime()`
- String methods: `.str.lower()`, `.str.upper()`, `.str.capitalize()`, `.str.strip()`, `.str.split()`, `.str.contains()`

### Transforming Data (Feature Engineering)
- `apply()`, `map()`, `assign()`, `replace()`, `rename()`
- Creating new/derived columns
- Sorting: `sort_values()`, `sort_index()`
- Ranking: `rank()` (with tie-breaking methods — dense, min, max)
- Reordering and resetting index (`reset_index()`)
- Writing data back out with `to_csv()`

### Grouping & Aggregation
- `groupby()` + built-in aggregations (`mean`, `sum`, `min`, `max`, `count`)
- `agg()` with lists, dicts, and named aggregations
- Multi-column grouping and multi-stat aggregation

### Reshaping
- `melt()` — wide to long format
- `pivot()` — long to wide format

### Merging & Combining
- `pd.merge()` — inner, left, right, and outer joins
- `pd.concat()` — row-wise and column-wise concatenation

### Basic Visualization
- `.hist()`, `.plot(kind="scatter")`

## Setup

```bash
pip install pandas numpy
jupyter notebook
```

## Notes

This is a working log, not a polished project — comments are notes to myself on why something behaves the way it does. Expect rough edges as I keep adding to it.
