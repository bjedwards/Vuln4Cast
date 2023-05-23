# Vuln4Cast

## What is this repository all about?
This repository holds the code that uses NVD data to demonstrate that it is possible to forecast vulnerabilities with reasonable accuracy both quarterly and yearly. We believe this is foundational rather than an end result. In other words, this forecasting will enable other research to be performed that might not have existed before. We encourage you to make more accurate forecasts, or extend the lookahead window, or make sub-forecasts for specific vendors.

## Quickstart

Clone this repository, configure a suitable Python 3 and Jupyter Notebook environment.

```
git clone https://github.com/FIRSTdotorg/Vuln4Cast.git
cd Vuln4Cast
pip install -r requirements.txt
```

Before running the analysis, you will need to run the code to fetch NVD data, see `NVDDataFetch-V1.ipynb`. This builds directory structures, fetches data from NVD (and CVE), and unpacks that data into formats that are easier to work with. This will take a few minutes depending on your network.

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/FIRSTdotorg/Vuln4Cast/HEAD)
<a target="_blank" href="https://colab.research.google.com/github/FIRSTdotorg/Vuln4Cast">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>

## Analysis

Once the data has been fetched, you can run either the quarterly or yearly forecasts. They each use a Sarimax model that gives good results, and we consider as a benchmark for your own research to beat. They also contain a hurst exponent analysis that should demonstrate that it is both possible to forecast, and there is long term trending in the data. Other graphs help demonstrate features useful to forecasters who will wish to extend or improve the work.

If all of this interests you, we encourage you to get in touch, and help us build a community dedicated to prediction and forecasting of vulnerabilities. We believe we are part of a wider movement of cyber risk quantification that includes our allies like [EPSS](https://github.com/FIRSTdotorg/epss). They predict exploitation of CVEs rather than CVE volumes. We honestly foresee a world in which these techniques become combined and and even perhaps the economic damage of explotation can be predicted as well.

## To cite the original paper

Éireann Leverett, Matilda Rhode, and Adam Wedgbury. 2022. Vulnerability Forecasting: Theory and Practice. Digital Threats 3, 4, Article 42 (mar2022), 27 pages. https://doi.org/10.1145/3492328

@article{10.1145/3492328,
author = {Leverett, \'{E}ireann and Rhode, Matilda and Wedgbury, Adam},
title = {Vulnerability Forecasting: Theory and Practice},
year = {2022},
issue_date = {December 2022},
publisher = {Association for Computing Machinery},
address = {New York, NY, USA},
volume = {3},
number = {4},
issn = {2692-1626},
url = {https://doi.org/10.1145/3492328},
doi = {10.1145/3492328},
abstract = {It is possible to forecast the volume of CVEs released within a time frame with a given prediction interval. For example, the number of CVEs published between now and a year from now can be forecast within 8% of the actual value. Different predictive algorithms perform well at different lookahead values other than 365 days, such as monthly, quarterly, and half year. It is also possible to estimate the proportions of that total volume belonging to specific vendors, software, CVSS scores, or vulnerability types. Some vendors and products can be predicted with accuracy, others with too much uncertainty to be practically useful. This article documents which vendors are amenable to being forecasted. Strategic patch management should become much easier with these tools, and further uncertainty reductions can be built from the methodologies in this article.},
journal = {Digital Threats},
month = {mar},
articleno = {42},
numpages = {27},
keywords = {Cyberrisk, forecasting, prediction, CVE, vulnerabilities, vulnerability management}
}

## To cite this codebase if you use it for your own paper

Leverett, É; Rhode, M; Burns, E; Manion, A (2023) Vuln4Cast source code (Version 1.0.0) [Source code]. https://github.com/FIRSTdotorg/Vuln4Cast/
