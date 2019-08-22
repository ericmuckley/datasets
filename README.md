# Datasets

This repository contains experimental datasets. To access a dataset from a Google Colab Python notebook, open the dataset and click on *View Raw*. Copy the URL to the raw dataset.

Then in a Google Colab notebook, paste the URL as the *url* variable. Use the Python library Pandas to import the dataset. In this case it is a csv file:

```
import pandas as pd

# set the URL
url = 'copied_raw_URL_link'

# read the dataset from the URL
df1 = pd.read_csv(str(url))

# show the first few rows of the dataset
print(df1.head())

```
