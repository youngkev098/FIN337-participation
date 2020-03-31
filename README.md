# Assignment 5 Scrapping Data  
### Kevin Williams 

The goal of this assignment is to answer the question "Are the investment choices (R&D and CAPX) a firm makes related to its technology and risks it faces?" 

To answer this question I:
* Take advantage of a provided data set
* Build a scrapper which gets a firm's 10-K filing from 2007
* Parse and search the 10-K filings for preselected risks
* Measure and store the risk measures 
* Create plots to visualize the relationship between investment (R&D and CAPX) and the risks a firm faces

The assignment instructions can be found [here](https://ledatascifi.github.io/assignments/asgn05.html).

## Summary Of The Analysis:
I found that ...

I saw that Outstanding OTC derivatives amounts were high.. 
![alt text](https://www.bis.org/statistics/otc_hy1905_graph1.jpg) 

* link to image site can be found [here](https://www.bis.org/publ/otc_hy1905.htm)

## About This Repository
My Assignment 5 Repo is organized as follows:

**Contents**:
* README.md = Current README file for repo.
* downloads_10Ks.ipynb = Downloads 2007_inv_and_tech.dta from GitHub and downlads 2007 form 10-K filings for companies in 2007_inv_and_tech.dta.
  * The link to 2007_inv_and_tech.dta variable desriptions can be found [here](https://github.com/LeDataSciFi/lectures-spr2020/tree/master/assignment_data#firms_2006_fullerdta).
  * \* Note that running this code will create subfolders with approx 250MB in size\* 
* edgar_filings = Is created from downloads_10Ks.ipynb and holds all company's form 10-K for 2007.
  * Proof of Downloaded 148 edgar filings: ![148_filings](https://user-images.githubusercontent.com/31543415/77296354-e3853c80-6cbd-11ea-848e-aad99bfea110.png)
* input = Is created from downloads_10Ks.ipynb and holds 2007_inv_and_tech.dta.
* output = Is created from measure_risk.ipynb and holds new df to answer research question.
* measure_risk.ipynb = Reads input and calculates determined risk measures. It uses NEAR_regex.py to calculate risk measures and outputs a new df with such risk calculations.
* analysis.ipynb = Visualizes df in output and answers research question.
* NEAR_regex.py = Is a function created by Professor Bowen to help calculate risks

Quick Tip: *Run downloads folder first, which creates input and edgar_filings folder. Then explore NEAR_regex.py and run measure_risks, which creates output folder. Lastly, run analysis folder.*

**Imports**:
- [X] `import pandas as pd`
- [X] `import pandas_datareader as pdr`
- [X] `import numpy as np`
- [X] `import matplotlib.pyplot as plt`
- [X] `import seaborn as sns`
- [X] `from requests_html import HTMLSession`
- [X] `import os`
- [X] `import re`
- [X] `from time import sleep`
- [X] `from tqdm.notebook import tqdm`
- [X] `from bs4 import BeautifulSoup`


