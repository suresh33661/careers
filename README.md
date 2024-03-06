# Automated website url open with Python

## This Python script automate the process of opening website using various libraries such as pandas, requests, BeautifulSoup, Webbrowser, and time.


# Installation

## Ensure you have Python installed on your system. You can download it from the official [Python website.](https:/python.org)

## Install the required Python libraries using pip:

```bash
    pip install pandas numpy requests beautifulsoup4

```
# Usage
## Download the Data
```Python

import pandas as pd
import requests
from bs4 import BeautifulSoup
import webbrowser
import time
```
## Read the data using pandas 
```Python
df = pd.read_excel("downloaded path/file name.xlsx")
for index, row in df.iterrows():
    company = rows["company"] # Name of column given in data
    location = rows["Location"] # location name given in data 
    url = rows["Website"] # website url given in data

    response = request.get(url)
    soup = BeautifulSoup(response.content, 'html.parser')
    try:
        if soup.find('a' , text = "Careers") or soup.find('a', text = 'careers'): # we can use it or not, it is only to find whether website has careers.
        webbrowser.open(url) # customize opening browser Eg: Edge or Chrome.
        time.sleep(60) # open new link in every 60 seconds customize it.

    except Exception as e:
        pass

```
## The theme of this project is using automated script to open website.
