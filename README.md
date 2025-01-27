# Olympic Medals Web Scraping Project

This project is a web scraping tool designed to collect and analyze data on the number of Olympic medals won by each country from Wikipedia. Using Python, the `requests` and `BeautifulSoup` (`bs4`) libraries scrape the data, and `pandas` is used to clean and analyze it.

## Project Overview

The goal of this project is to extract the data on Olympic medal counts by country, process it, and make it suitable for further analysis or visualization. This README file provides an overview of the project setup, tools used, and how to run the script.

## Table of Contents

- [Project Overview](#project-overview)
- [Project Structure](#project-structure)
- [Tools and Libraries Used](#tools-and-libraries-used)
- [Setup Instructions](#setup-instructions)
- [Usage](#usage)
- [Data Processing and Wrangling](#data-processing-and-wrangling)
- [Future Enhancements](#future-enhancements)

## Project Structure

```
├── olympic_medals_scraper.py    # Main script to scrape and process the data
├── README.md                     # Project documentation
├── requirements.txt              # List of dependencies
└── data
    └── olympic_medals.csv        # Cleaned data file (optional)
```

## Tools and Libraries Used

- **Python**: The core language used for this project.
- **Requests**: For making HTTP requests to Wikipedia to retrieve the HTML content of the page.
- **BeautifulSoup (bs4)**: For parsing and extracting the relevant data from the HTML.
- **Pandas**: For data cleaning, transformation, and exporting to a structured CSV format.

## Setup Instructions

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/olympic-medals-scraper.git
   cd olympic-medals-scraper
   ```

2. **Install Dependencies**:
   It’s recommended to set up a virtual environment before installing dependencies.

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
   ```

   Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

Run the `olympic_medals_scraper.py` script to scrape data and save it to a CSV file:

```bash
python olympic_medals_scraper.py
```

This script:
1. Sends a request to Wikipedia for the page listing Olympic medals by country.
2. Parses the HTML content to find and extract relevant data.
3. Cleans and structures the data using Pandas.
4. Exports the cleaned data to a CSV file in the `data` directory.

## Data Processing and Wrangling

The data collected from Wikipedia is initially unstructured. Using `pandas`, the script performs the following data wrangling steps:
- Removes any unnecessary columns or rows.
- Converts data types as needed for numerical analysis.
- Renames columns to be more readable and standardized.
- Fills in any missing values if necessary.

## Future Enhancements

In future versions, this project could be improved with the following features:
- **Automatic updates**: Schedule the script to re-run periodically to keep the data current.
- **Error handling and retries**: Add functionality to handle network errors or changes in the HTML structure of the Wikipedia page.
- **Visualization**: Add scripts or notebooks to visualize medal distribution by country using libraries like Matplotlib or Seaborn.
