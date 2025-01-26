
# Data-Analysis-with-DBMS-and-SQLAlchemy

This project demonstrates how to connect Python with MySQL, perform database operations, and visualize data using Python libraries such as Pandas, Matplotlib, and Seaborn. It is designed to help you manage and analyze data stored in a MySQL database. In this project **SQLAlchemy** is also used for a more flexible and powerful library for managing database connections and running SQL queries in a more abstracted manner.


## Example Code

### Establishing the Database Connection (Using SQLAlchemy):

```python
from sqlalchemy import create_engine

# Replace with your own credentials
engine = create_engine('mysql+mysqlconnector://root:password@localhost:3306/database_name')

# Connect to the database
connection = engine.connect()
print(connection)
```

### Executing SQL Queries:

```python
# Using the SQLAlchemy engine to execute a query
result = connection.execute("SELECT * FROM your_table")
for row in result:
    print(row)
```

### Data Visualization Example:

```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Example DataFrame creation from SQL query
df = pd.read_sql("SELECT * FROM your_table", connection)

# Visualization
plt.figure(figsize=(10,6))
sns.histplot(df['column_name'])
plt.show()
```



