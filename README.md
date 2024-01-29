# ETL Project: Country-GDP Data

## Introduction

This project is about creating an automated script that can extract the list of all countries in order of their GDPs in billion USDs (rounded to 2 decimal places), as logged by the International Monetary Fund (IMF). The data is extracted from the following URL:

'https://web.archive.org/web/20230902185326/https://en.wikipedia.org/wiki/List_of_countries_by_GDP_%28nominal%29'

The data is then transformed by converting the GDP information from currency format to float value, and from USD (millions) to USD (billions). The data is then loaded to a CSV file `Countries_by_GDP.csv` and a database file `World_Economies.db` with a table `Countries_by_GDP` with attributes `Country` and `GDP_USD_billion`.

The script also runs a query on the database table to display only the entries with more than a 100 billion USD economy. The entire process of execution is logged in a file `etl_project_log.txt`.

## Requirements

To run this project, you need to have the following:

- Python 3 installed on your system
- The following Python libraries installed using `pip` or `conda`:
  - `bs4` for web scraping
  - `requests` for sending HTTP requests
  - `pandas` for data manipulation and analysis
  - `numpy` for numerical computation
  - `sqlite3` for database connection and manipulation
  - `datetime` for logging timestamps
- An internet connection to access the URL

## Usage

To execute the script, you can run the following command in your terminal:

`python etl_project_gdp.py`

The script will create the CSV file, the database file, and the log file in the same directory as the script. You can open them using any suitable application. The script will also print the query output on the terminal.

## Code Structure

The script is named `etl_project_gdp.py` and consists of two parts:

- The first part defines the functions for each stage of the ETL process, as well as the logging and query functions.
- The second part defines the required entities and calls the relevant functions in the correct order to complete the project.

The script is commented and documented for better readability and understanding. You can refer to the comments and the docstrings for more details about the functions and the variables.


## Modularity and Reusability

The script is modular and reusable. You can change the URL, the table attributes, the file names, or the query statement as per your requirements. You can also modify the functions or add new ones as per your needs.
