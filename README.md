# Fintech_Module5
---

![Financial_Analysis.png](https://github.com/nielsdehaan1977/Fintech_Module4/blob/main/Images/Financial_Analysis.PNG)

## Financial Planning with APIs and Monte Carlo Simulations

## financial_planning_tools.ipynb
---

### This Jupyter notebook is a template for Financial Planning with APIs (Application Programming Interface) and uses Monte Carlo simulation to simulate the future performance of a portfolio and trying to analyze its most probable outcome. 
The tool contains two financial analysis tools in one single jupyter notebook:
1. A financial planner for emergencies. Members will be able to use this tool to visualize their current savingsand can then determine if they have enough reserves for an emergency fund.
2. A financial planner for retirement. This tool will forecast the performance of their retirement portfolio in 30 years. To do this, the tool will make an Alpaca API call via the Alpaca SDK to get historical price data to use in Monte Carlo simulations.

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

#### Step1: Activate dev environment in Gitbash or Terminal to do so type:
```python
    conda activate dev
```
#### Step2: install the following libraries by typing:
```python
    pip install pandas
    pip install python-dotenv
    pip install alpaca-trade-api
    conda install -c anaconda requests
    conda install -c jmcmurray json
```

#### Step3: Get the Alpaca API and Secret Keys

You need to generate API credentials from the Alpaca API. To create an account, enter an email address, create a 12-character password, and then click “Sign up for free.” You’ll receive an email to verify the address before you can continue. Once you verify your email address, the "Welcome to Alpaca” page displays. Click the “Go to Paper Account” link. 
In the “Your API Keys” area, click the View button. Then click “Generate API Keys.” This generates two keys: the API Key ID and a secret key.
You can put both keys in the SAMPLE.env file in the repository and change the name to .env (remove "Sample" from file name). Please note that the .env file needs to be in the same folder as the jupyter notebook file to work properly. 

![Alpaca](https://github.com/nielsdehaan1977/Fintech_Module5/blob/main/Images/Alpaca.png)

#### Step4: MCForecastTools.py file

For the Monte Carlo simulation framework, please use the Python library named MCForecastTools. This library isn’t part of the Conda development environment, it exists as a Python file named MCForecastTools.py . This file contains all the logic, in the form of Python code, that you need to run the Monte Carlo simulation. Please note this file needs to be in the same folder as the Jupyter notebook that you’re working in. Then import MCForecastTools.py into the notebook to access it and therefore to run the simulations.

Please find the code for MCForecastTools in below link:

[MCForecastTools](https://cdn.inst-fs-pdx-prod.inscloudgate.net/e0e08ad7-c5b3-43c1-8e7c-e7efc5f1f39c/MCForecastTools.py?token=eyJhbGciOiJIUzUxMiIsInR5cCI6IkpXVCIsImtpZCI6ImNkbiJ9.eyJyZXNvdXJjZSI6Ii9lMGUwOGFkNy1jNWIzLTQzYzEtOGU3Yy1lN2VmYzVmMWYzOWMvTUNGb3JlY2FzdFRvb2xzLnB5IiwidGVuYW50IjoiY2FudmFzIiwidXNlcl9pZCI6IjE1MDQyMDAwMDAwMDA0MTkyOCIsImlhdCI6MTY3MjMwNDM5NywiZXhwIjoxNjcyMzkwNzk3fQ.WGJMX_rASeilWSbulLAihV6NgGxdQXfVJnemxa9Pdyydjy0LvqbqBUcMU_ORuels5eLcI8CUQ7bzjZMIcmOi3A&content_type=text%2Fx-python)

#### Step5: Start Jupyter Lab
Jupyter Lab can be started by:
1. Activate your developer environment in Terminal or Git Bash (already done in step 1)
2. Type "jupyter lab --ContentsManager.allow_hidden=True" press enter (This will open Jupyter Lab in a mode where you can also see hidden files)

![JupyterLab](https://github.com/nielsdehaan1977/Fintech_Module5/blob/main/Images/JupyterLab.PNG)


## Usage

To use the financial planning tools jupyter lab notebook, simply clone the full repository and open the **financial_planning_tools.ipynb** file in Jupyter Lab. 

**Upon running the tool please make sure MCForecastTools.py and the .env file with the Apalca API keys is in the same folder, otherwise the tool will not work properly.** 

The tool will go through all the steps of financial planning:

### Create a Financial Planner for Emergencies
1. Evaluate a cryptocurrency wallet by using the requests library
2. Evaluate a stock and bonds portfolio by using the Alpaca SDK
3. Evaluate the Emergency Fund

### Create a Financial Planner for Retirement
1. Create a Monte Carlo simulation
2. Analyze retirement portfolio forecasts
3. Forecast cumulative returns in 10 Years

## Contributor(s)

This project was created by Niels de Haan (nlsdhn@gmail.com)

---

## License(s)

MIT
