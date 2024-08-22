# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 22/08/2024

# AIM:
To Develop a python program to Plot a time series data for pH level for water quality

# ALGORITHM:

1. Import the required packages like pandas and matplot

2. Read the dataset using the pandas

3. Calculate the mean for the respective column.

4. Plot the data according to need and can be altered monthly, or yearly.

5. Display the graph.

# PROGRAM:

```py
import pandas as pd
import matplotlib.pyplot as plt
import numpy as np
```
```py
data = pd.read_csv('/content/prices.csv')
```
```py
data['Price Dates'] = pd.to_datetime(data['Price Dates'], format='%d-%m-%Y')
```

```py
X = np.array(data.index).reshape(-1, 1)
y = data['Methi']
```

```py
plt.figure(figsize=(12, 6))
plt.plot(data['Price Dates'], data['Methi'], label='Methi Price')
plt.xlabel('Date')
plt.ylabel('Price')
plt.title('Price of Methi Over Time')
plt.grid(True)
plt.show()
```

# OUTPUT:

![image](https://github.com/user-attachments/assets/2da3f636-fd28-4463-a39b-3d07c7ee0ec8)


# RESULT:
Thus we have created the python code for plotting the time series of given data.
