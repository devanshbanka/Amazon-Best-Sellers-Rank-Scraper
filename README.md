# Amazon-Best-Sellers-Rank-Scraper

This repository contains a Python script that scrapes the Best Sellers Rank of products on Amazon and stores the data in Google Sheets. The script can be scheduled to run every hour to keep track of the rank changes, which can be used to build models to estimate sales and market share.

## Features

- **Google Sheets Integration**: Creates new worksheets for each product based on the SKU and stores the rank data.
- **Web Scraping**: Scrapes the Best Sellers Rank from Amazon product pages.
- **Data Logging**: Appends the rank data to the corresponding worksheet in Google Sheets.
- **Historical Data Collection**: Collects data over time to build models for sales and market share estimation.

## Setup

### Google Cloud Setup
- Create a project in the Google Cloud Console.
- Enable the Google Sheets API and Google Drive API.
- Create a service account and download the JSON key file.
- Share your Google Sheet with the service account email.

### Configuration
- Place the service account JSON key file in your project directory.
- Replace 'path/to/credentials.json' with the path to your JSON key file in the script.

### Google Sheet Setup
- Create a Google Sheet named Amazon Data Analytics (or any name you prefer).
- Add a worksheet with product SKUs and URLs.
    * Column A: SKU
    * Column B: URL

### Libraries

Install the required libraries using pip:

```bash
pip install gspread oauth2client beautifulsoup4 requests
