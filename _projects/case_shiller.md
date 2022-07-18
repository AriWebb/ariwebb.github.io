---
title: "Penguins Can Fly"
date: 2022-06-05
last_modified_at: 2022-07-17
header:
  teaser: /assets/images/case_shiller/country.png
sidebar:
  - title: "Role"
    image: /assets/images/case_shiller/country.png
    text: "Data Cleaning, VAR Model Builder"
  - title: "Languages"
    text: "Python, NumPy and Pandas"    
  - title: "Built For"
    text: "CS 229: ML Final Project"
  - text: "Time Spent: 4 weeks"
toc: true
---

I've worked in the real estate industry for most of my life. My work has been pragmatic though --construction, property management, labor. I only recently gained an interest in how the broader real estate market moves, and further how data can be leveraged to gain insights about the market.

# Project

As a final project for our course CS 229: Machine Learning, Matt Wolff, Laywood Fayne and I compiled economic data and used it to predict the Case Shiller housing index in 20 major US cities. Find the full source code for the project [here][repo].

# Method + Results

I implemented the Vector Autoregression algorithem on our data. VAR is a statistical model that captures the relationship between multiple variables, and uses these values to model future trends. More about the VAR model can be found in our [final write-up][write].

We ended with some nice graphs predicting future values of many features. See below for our predictions vs actual values in San Francisco:

<img src="{{ site.url }}{{ site.baseurl }}/assets/images/case_shiller/sf.png" alt="">


[repo]: https://github.com/AriWebb/case-shiller-prediction
[write]: https://github.com/AriWebb/case-shiller-prediction/blob/main/CS229__Project_Final_Report.pdf