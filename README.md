# Datasets

This repository contains experimental datasets. You can access a dataset from a Google Colab Python notebook in two different ways.


### Option 1
In the Google Colab notebook, use the following code to clone this github repository, view the files in it, and open one of the files using Pandas.
```
# enter the folder you want to clone the respositry into
%cd /content/
# remove the cloned folder if it exists already
!rm -rf cloned-data
# clone the Github repo
!git clone -l -s git://github.com/ericmuckley/datasets.git cloned-data
# navigate to the cloned repo
%cd cloned-data
# print the list of files inside the cloned repo
print('-------------------------- Files in repo: --------------------------')
!ls

# for a csv or Excel file, open using Pandas
import pandas as pd
data = read_csv('filename.csv')

# for a serialized Python pickle file, open using pickle
import pickle

def open_pickle(filename):
    '''
    Opens serialized Python pickle file as a dictionary.
    Filename should be something like 'saved_data.pkl'.
    '''
    with open(filename, 'rb') as handle:
        dic = pickle.load(handle)
    return dic

# open the file we want
dic = open_pickle('pp_multimode.pkl')


# get out of the repo folder and back to the main content folder
%cd /content/
```




### Option 2
Open the dataset. Near the data headers, click the **Raw** button. Once you are viewing the data in raw form, copy the URL.

In a Google Colab notebook, paste the URL as the *url* variable inside quotes to designate that its a string. Use the Python library Pandas to import the dataset. In this case it is a csv file:

```
import pandas as pd

# set the URL
url = 'https://raw.githubusercontent.com/ericmuckley/datasets/master/hops_enose_response.csv'

# read the dataset from the URL
df1 = pd.read_csv(url)

# show the first few rows of the dataset
print(df1.head())

```
