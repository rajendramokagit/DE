# DE

## Data Cleaning

The `datacleaning` script performs data cleaning on an employee dataset (`Employee_Table.csv`) using PySpark:

1. **Load data**: Creates a Spark session and reads `Employee_Table.csv` with header and inferred schema, then prints the schema and the DataFrame before cleaning.
2. **Handle nulls**: Fills missing values in the `Department` column with `'Generalist'`, and fills missing `Joining Year` values with `2010` (assumed to mean the employee joined during company founding).
3. **Standardize values**: Replaces `'Information Tech'` with `'IT'` in the `Department` column.
4. **Remove outliers**: Filters out employees with `Age >= 60` or `Age <= 18` (max working age assumed to be 59, minimum 19).
5. **Remove incomplete rows**: Drops rows missing both `First Name` and `Last Name`.

Finally, it prints the cleaned DataFrame.

