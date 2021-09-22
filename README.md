# Data Analytics 
# Read and write from SQL by using Panadas

you can download PostgreSQL by https://www.postgresql.org/download/

```python
import psycopg2
import pandas as pd
from sqlalchemy import create_engine

```
# Read from th datasets contains information about rental appartments in Berlin.
```python
Data = pd.read_csv("https://raw.githubusercontent.com/juliandnl/redi_ss20/master/berlin_rental.csv")
```


# connection to Database

Username: postgres,
Password: postgres,
host: localhost,
Port: 5432,
Database: Sample
```python
engine = create_engine('postgresql+psycopg2://postgres:postgres@localhost:5432/Sample')

```
# write to SQL by using Pandas
```python
Data.to_sql('Sample_table_4',engine)

```

# Read to SQL by using Pandas
```python
dfd=pd.read_sql('Sample_table',engine)

```
