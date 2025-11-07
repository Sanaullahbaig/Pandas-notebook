# Pandas Notebook README

This notebook provides an introduction to the pandas library in Python, covering fundamental data structures, data manipulation techniques, and handling missing data.

## Data Structures

- **Series:** One-dimensional labeled arrays capable of holding various data types.
- **DataFrame:** Two-dimensional labeled data structures with columns of potentially different types.

The notebook demonstrates creating Series and DataFrames from lists and dictionaries.

## CSV File Handling

- **Writing to CSV:** The notebook shows how to save a DataFrame to a CSV file using `to_csv()`.
- **Reading from CSV:** It illustrates reading data from a CSV file using `read_csv()`, including options for specifying the number of rows, selecting specific columns, skipping rows, changing the index column, setting headers, renaming columns, and changing data types during import.

## Handling Missing Data

- **`dropna()`:** Used to remove rows or columns containing missing values (NaN). Examples show dropping rows/columns with any or all NaN values, or based on a subset of columns or a threshold of non-NaN values.
- **`fillna()`:** Used to replace missing values with specified values. Examples include filling with a single value, a dictionary of values for specific columns, or using forward fill (`ffill`) or backward fill (`bfill`) methods with optional limits.
- **`replace()`:** Used to replace specific values with other values. Examples demonstrate replacing single values, lists of values, or using regular expressions for replacement. It also shows using `ffill` and `bfill` methods with `replace`.
- **`interpolate()`:** Used to estimate missing values based on existing data, primarily for numerical data. Examples show default linear interpolation, interpolation along different axes, and setting limits on the number of consecutive missing values to fill.

## Merging and Concatenating

- **`merge()`:** Combines DataFrames based on matching values in common columns, similar to SQL joins. Examples show inner, left, right, and outer merges, and how to handle columns with the same name using suffixes.
- **`concat()`:** Stacks DataFrames or Series along an axis. Examples show concatenating Series and DataFrames along rows (axis=0) and columns (axis=1), handling different column names, and using `join` to control how the concatenation handles missing values. It also shows how to add keys to the concatenated data.

## Group By

- **`groupby()`:** Groups DataFrame rows based on unique values in a specified column. The notebook demonstrates iterating through groups, getting a specific group, and applying aggregation functions like `min()`, `max()`, and `mean()` to the grouped data.

## Changing The Shape Of DataFrame

- **`melt()`:** Unpivots a DataFrame from a wide to a long format, making column headers into row values. Examples show basic melting, specifying ID variables, and renaming the resulting variable and value columns.
- **`pivot()`:** Reshapes a DataFrame based on column values. Examples show pivoting with an index and columns, and specifying values to include in the pivoted table.
- **`pivot_table()`:** A more flexible version of `pivot` that can handle duplicate entries for a given index/column combination by aggregating values using a specified function (`aggfunc`). It also shows how to include margins for summary statistics.

This notebook provides a practical overview of these essential Pandas functions for data manipulation and analysis.
