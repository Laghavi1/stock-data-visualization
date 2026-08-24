# stock-data-visualization
 Learning project, extracting financial data of Tesla, Amazon, AMD and GameStop such as historical stock prices and quarterly revenue from multiple sources using Python libraries and web scraping techniques.
# Extracting and Visualizing Stock Data

## Description
Extracting essential data from a dataset and displaying it is a necessary part of data science, enabling individuals to make informed decisions based on historical trends. This project focuses on extracting stock performance and revenue data for **Tesla (TSLA)** and **GameStop (GME)**, cleaning the data, and building a visualization dashboard to compare historical share prices against quarterly revenue.

## Table of Contents
* [Technologies Used](#technologies-used)
* [Project Workflow](#project-workflow)
* [Installation and Setup](#installation-and-setup)
* [Usage](#usage)
* [Author](#author)

## Technologies Used
This project relies on the following Python libraries:
* **`yfinance`**: For extracting historical stock price data via the Yahoo Finance API.
* **`requests`**: For downloading HTML data from web pages.
* **`BeautifulSoup` (`bs4`)**: For web scraping and parsing HTML to locate revenue tables.
* **`pandas`**: For data manipulation, cleaning, and storing data in DataFrames.
* **`matplotlib`**: For rendering static subplot visualizations (dashboards) of the extracted data.

## Project Workflow
The Jupyter Notebook (`Revenue Data and Building a Dashboard.ipynb`) is structured to execute the following tasks:
1. **Define a Graphing Function:** Establish a reusable `make_graph` function using `matplotlib` to plot share price and revenue on stacked subplots.
2. **Extract Tesla Stock Data:** Utilize `yfinance` to pull the maximum historical stock data for TSLA.
3. **Scrape Tesla Revenue Data:** Use `requests` and `BeautifulSoup` to extract quarterly revenue data from a web source, followed by data cleaning (removing dollar signs, commas, and null values) using `pandas`.
4. **Extract GameStop Stock Data:** Utilize `yfinance` to pull the maximum historical stock data for GME.
5. **Scrape GameStop Revenue Data:** Scrape and clean GME quarterly revenue data using the same web scraping methodologies.
6. **Data Visualization:** Plot the historical share prices and revenues for both Tesla and GameStop to create a clear, visual dashboard.

## Installation and Setup
To run this notebook locally, ensure you have Python installed, and then install the required dependencies. You can do this by running the following commands in your terminal or command prompt:

```bash
pip install yfinance
pip install bs4
pip install nbformat
pip install matplotlib
pip install pandas
pip install lxml
```
Note: The lxml parser and io.StringIO module are utilized to ensure pandas.read_html functions correctly without raising FileNotFoundError exceptions in newer versions of Pandas.

Author
Laghavi Mukkirla

Project completed as part of an IBM Data Science skills network curriculum.
