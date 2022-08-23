# Data Import Setup

## SQL via duckdb

duckdb is a zero-dependency in-memory SQL database.

It can read CSV files automatically into memory, and can do in-memory processing of the files. It would simplify the installation instructions greatly (no need to set up a postgres database.

It is instantly usable via [dbeaver](https://dbeaver.io/download/), an open source SQL client (specify :memory: for the filepath and install the jdbc drivers), or you can install the ODBC driver or use the CLI.

To use, do the following:

`git clone https://github.com/chop-analytics/analyst-take-home-task`

Open duckdb sql client, example read:

```sql
select *
    from read_csv_auto('~/analyst-take-home-task/datasets/encounters.csv', SAMPLE_SIZE = -1)
```

For more detailed instructions on setting up duckdb with dbeaver, click [here](duckdb_setup.md)

## Python

```python
import pandas as pd

pd.read_csv('https://raw.githubusercontent.com/chop-analytics/analyst-take-home-task/master/datasets/allergies.csv')
```

## R

```r
readr::read_csv('https://raw.githubusercontent.com/chop-analytics/analyst-take-home-task/master/datasets/allergies.csv')
```
