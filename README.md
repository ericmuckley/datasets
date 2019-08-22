# Datasets

This repository contains experimental datasets. To access a dataset from a Google Colab Python notebook, open the dataset. Near the data heders, click the **_Raw_** button. Once you are viewing the data in raw form, copy the URL.

In a Google Colab notebook, paste the URL as the *url* variable inside quotes to designate that its a string. Use the Python library Pandas to import the dataset. In this case it is a csv file:

```
import pandas as pd

# set the URL
url = 'https://github.com/ericmuckley/datasets/blob/master/hops_enose_response.csv'

# read the dataset from the URL
df1 = pd.read_csv(url)

# show the first few rows of the dataset
print(df1.head())

```
