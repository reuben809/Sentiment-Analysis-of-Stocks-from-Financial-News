# Sentiment Analysis of Stocks from Financial News

## Overview

This project extracts stock sentiments from financial news headlines, visualizes hourly and daily sentiments in a Flask web application, and deploys the app online. The application provides insightful visualizations to help users understand sentiment trends of their chosen stocks.

## Project Directory Structure

```
stock_sentiment_webapp/
│
├── app/
│   ├── __init__.py
│   ├── routes.py
│   ├── templates/
│   │   ├── index.html
│   │   └── sentiment.html
│   └── static/
│       └── style.css
│
├── data/
│   ├── apple-computers.txt
│   └── apple-fruit.txt
│
├── requirements.txt
└── run.py
```



### Explanation of Structure

- **app/**: Contains the Flask application files.
  - **\_\_init\_\_.py**: Initializes the Flask application.
  - **routes.py**: Defines the routes and views for the application.
  - **templates/**: Contains HTML templates for rendering pages.
    - **index.html**: Main page for user input.
    - **sentiment.html**: Page displaying sentiment analysis results.
  - **static/**: Contains static files such as CSS stylesheets.
    - **style.css**: Styles for the web pages.

- **data/**: Contains text files with data related to Apple Inc. and apple fruit.
  - **apple-computers.txt**: Information about Apple Inc.
  - **apple-fruit.txt**: Information about the apple fruit.

- **requirements.txt**: Lists the required Python packages for the project.

- **run.py**: Script to run the Flask application.

## Features

- **Sentiment Analysis**: Extracts and scores news headlines for given stock tickers using VADER sentiment analyzer.
- **Hourly and Daily Sentiment Visualization**: Plots the hourly and daily sentiment scores using Plotly.
- **User Interaction**: Users can input a stock ticker to view sentiment analysis results in graphical and tabular formats.

## Installation

To install and run the application locally, follow these steps:

1. **Clone the repository to your local machine**:
    ```bash
    git clone https://github.com/YourUsername/stock_sentiment_webapp.git
    ```

2. **Install the required dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

3. **Run the Flask application**:
    ```bash
    python run.py
    ```

## Usage

1. **Navigate to the web application URL in your web browser**.
2. **Input a stock ticker in the form on the index page**.
3. **Submit the form to view sentiment analysis results, including charts and news headlines**.

## Detailed Workflow

### Import Necessary Libraries

Import required libraries such as Flask, BeautifulSoup, pandas, plotly, nltk, etc.

### Configure SSL and Download NLTK Data

Configure SSL to handle secure connections and download NLTK data required for sentiment analysis.

### Define Functions

- `get_news(ticker)`: Fetches news headlines for a given stock ticker from the FinViz website.
- `parse_news(news_table)`: Parses the raw HTML news table into a pandas DataFrame.
- `score_news(parsed_news_df)`: Scores each headline in the DataFrame using the VADER sentiment analyzer.
- `plot_hourly_sentiment(parsed_and_scored_news, ticker)`: Plots the hourly sentiment scores of the stock.
- `plot_daily_sentiment(parsed_and_scored_news, ticker)`: Plots the daily sentiment scores of the stock.

### Create Flask Application

Initialize the Flask application.

### Define Routes

Define routes and views for the application:
- `/`: Renders the index page.
- `/sentiment`: Handles the sentiment analysis request and renders the sentiment page.

### Define Route Functions

- `index()`: Renders the index page containing the form to input the stock ticker.
- `sentiment()`: Handles the sentiment analysis request, fetches news data, performs sentiment analysis, and renders the sentiment page with charts and news headlines.

### Run the Application

Start the Flask application if the script is executed directly.

### HTML Templates and Static Files

- **Templates Directory**: Contains HTML templates for rendering web pages.
  - `index.html`: Provides a form to input the stock ticker.
  - `sentiment.html`: Displays sentiment analysis results with charts and news headlines.

- **Static Directory**: Contains static files such as CSS stylesheets.
  - `style.css`: Defines styles for the web pages.

### Data Directory

Contains text files with information about Apple Inc. and the fruit.

### Requirements File

`requirements.txt` lists all the Python packages required by the application.

### Run Script

`run.py` is the script to run the Flask application.

## Execution

When the script is executed, it starts the Flask application. Users can access the application through a web browser, input a stock ticker to view sentiment analysis results, and interact with graphical and tabular data formats.

## Deployment

The Flask application can be deployed locally for testing and development purposes and can also be deployed to a web server to make it accessible over the internet.

## Dependencies

The application requires various Python packages, including Flask, BeautifulSoup, pandas, Plotly, and NLTK. These dependencies are listed in the `requirements.txt` file for easy installation.

---

**Note:** Ensure you replace placeholders like `YourUsername` with actual values as needed in your project setup and deployment.
