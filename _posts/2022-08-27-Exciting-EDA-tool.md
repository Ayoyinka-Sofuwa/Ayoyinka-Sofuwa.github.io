---
layout: post
title: Found an exciting all-in-one EDA tool.
---

It is popularly said that 80% of a data scientist's time is spent on EDA, looking for a simple way to do your basic EDA in one or two lines of code?


[Pandas-profiling](https://pypi.org/project/pandas-profiling/) is a tool for creating profile reports from a pandas dataframe. It's really useful for some quick data analysis. 

Here's what I did with it. I worked on this dataset from [JovianML](https://twitter.com/jovianml) and we're tasked with creating an automated system to estimate the annual medical expenditure for new customers, using information such as their age, sex, BMI, children, smoking habits and region of residence. Basically, we want to determine what features influence the medical charges for different patients and how we can predict medical bills for new users using their different demographics.

Now let's have a quick EDA that gives us more information about our data in a single line of code.

The data used for this analysis can be found [here](https://raw.githubusercontent.com/JovianML/opendatasets/master/data/medical-charges.csv):
  > First install pandas-profiling package and others we might need.
  `pip install pandas-profiling`

  `pip install pandas`

  > Next import dependencies

  `from pandas-profiling import ProfileReport`

  `import pandas as pd`

  > Now let's retrieve the csv file from the url and view what it looks like:

  We can do it in two ways:
  `data = pd.read_csv(url)`

  `data.head()`
  or 
  `from urllib.request import urlretrieve`

  `urlretrieve(url, "medical-charges.csv")`

  `data = pd.read_csv(medical-charges.csv)`

  `data.head()`

I'm not really sure which method I prefer but let's move on:
  > Running the analysis with pandas-profiling package
  `profile = pdp.ProfileReport(data, title="Pandas Profiling Report")`
  
  `profile`
 
 It shows us the descriptive statistics (include snippets of data output)
