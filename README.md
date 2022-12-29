# Fintech_Module5
---

![Financial_Analysis.png](https://github.com/nielsdehaan1977/Fintech_Module4/blob/main/Images/Financial_Analysis.PNG)

## Risk Return Analysis.ipynb

### This Jupyter notebook is a template on how to prepare market data, what metrics can be used to analyse, and how to visualize key risk and return metrics for a solid Risk Return Analysis. 

---
## Table of Content

- [Tech](#technologies)
- [Installation Guide](#installation-guide)
- [Usage](#usage)
- [Contributor(s)](#contributor(s))
- [License(s)](#license(s))

---
## Tech

This project leverages python 3.9 and Jupyter Lab with the following packages:

* `Python 3.9`
* `Jupyter lab`

* [JupyterLab](https://jupyter.org/) - Jupyter Lab is the latest web-based interactive development environment for notebooks, code, and data.

* [pandas](https://pandas.pydata.org/pandas-docs/stable/index.html) - Pandas is an open source, BSD-licensed library providing high-performance, easy-to-use data structures and data analysis tools for the Python programming language.

* [os](https://docs.python.org/3/library/os.html) - module provides a portable way of using operating system dependent functionality.

* [requests](https://requests.readthedocs.io/en/latest/) - Requests is an elegant and simple HTTP library for Python, built for human beings.

* [json](https://docs.python.org/3/library/json.html) -  JSON is a lightweight data interchange format inspired by JavaScript object literal syntax.

* [dotenv](https://pypi.org/project/python-dotenv/) - Python-dotenv reads key-value pairs from a .env file and can set them as environment variables.

* [alpaca_trade_api](https://pypi.org/project/alpaca-trade-api/) - alpaca-trade-api-python is a python library for the Alpaca Commission Free Trading API. 

* [MCForecastTools](https://cdn.inst-fs-pdx-prod.inscloudgate.net/e0e08ad7-c5b3-43c1-8e7c-e7efc5f1f39c/MCForecastTools.py?token=eyJhbGciOiJIUzUxMiIsInR5cCI6IkpXVCIsImtpZCI6ImNkbiJ9.eyJyZXNvdXJjZSI6Ii9lMGUwOGFkNy1jNWIzLTQzYzEtOGU3Yy1lN2VmYzVmMWYzOWMvTUNGb3JlY2FzdFRvb2xzLnB5IiwidGVuYW50IjoiY2FudmFzIiwidXNlcl9pZCI6IjE1MDQyMDAwMDAwMDA0MTkyOCIsImlhdCI6MTY3MjMwNDM5NywiZXhwIjoxNjcyMzkwNzk3fQ.WGJMX_rASeilWSbulLAihV6NgGxdQXfVJnemxa9Pdyydjy0LvqbqBUcMU_ORuels5eLcI8CUQ7bzjZMIcmOi3A&content_type=text%2Fx-python) -  A Python class for runnning Monte Carlo simulation on portfolio price data.

* [matplotlib](https://matplotlib.org/) - Matplotlib is a comprehensive library for creating static, animated, and interactive visualizations in Python

---

## Installation Guide

### Before running the application first install the following dependencies in either Gitbash or Terminal. (If not already installed)

#### Step1:    conda activate dev

#### Step2: install the following libraries by typing:
```python
    pip install pandas
    pip install python-dotenv
    pip install alpaca-trade-api
    conda install -c anaconda requests
    conda install -c jmcmurray json
```

#### Step3: Get the Alpaca API and Secret Keys

You need to generate your API credentials from the Alpaca API. To create an account, enter an email address, create a 12-character password, and then click “Sign up for free.” You’ll receive an email to verify the address before you can continue. Once you verify your email address, the "Welcome to Alpaca” page displays. Click the “Go to Paper Account” link. 
In the “Your API Keys” area, click the View button. Then click “Generate API Keys.” This generates two keys: the API Key ID and a secret key.
You can put both keys in the SAMPLE.env file in the repository and change the name to .env (remove "Sample" from file name). Please note that the .env file needs to be in the same folder as the jupyter notebook file to work properly. 

![Alpaca](https://github.com/nielsdehaan1977/Fintech_Module5/blob/main/Images/Alpaca.PNG)

#### Step4: MCForecastTools.py file


#### Step5: Start Jupyter Lab
Jupyter Lab can be started by:
1. Activate your developer environment in Terminal or Git Bash (already done in step 1)
2. Type "jupyter lab --ContentsManager.allow_hidden=True" press enter (This will open Jupyter Lab in a mode where you can also see hidden files)

![JupyterLab](https://github.com/nielsdehaan1977/Fintech_Module5/blob/main/Images/JupyterLab.PNG)


## Usage

To use the Risk Return Analysis jupyter lab notebook simply clone the full repository including resources folder and open the **risk_return_analysis.ipynb.ipynb** file in Jupyter Lab. 

Upon launching risk_return_analysis.ipynb notebook, you will go through all the steps to analyse:

1. Import Data - Import required data and import required libraries.
2. Analyze performance - Analyze the data to determine if any of the portfolios outperform the broader stock market.
3. Analyze volatility - Analyze the volatility of each portfolios/stock and of the bench mark index by using box plots.
4. Analyze risk - Evaluate the risk profile of each portfolio/stock by using the standard deviation and the beta.
5. Analyze risk return profile - Determine the overall risk return of an asset or portfolio by considering the Sharpe ratios for each portfolio/stock. 
6. Diversify portfolio - Evaluate how the portfolios/stocks react relative to the broader market and conclude which one(s) can be used to diversify existing portfolio.


## Contributor(s)

This project was created by Niels de Haan (nlsdhn@gmail.com)

---

## License(s)

MIT
