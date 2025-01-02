# ELT- GDP Web Scraper

## create an automated script that will extract, transform, and load (ETL) the GDP data of countries, as published by the International Monetary Fund (IMF).

### Project Objective:
The goal of this project is to develop a Python script (`etl_project_gdp.py`) that performs the following tasks:

1. **Data Extraction**:
   - Retrieve the list of countries and their GDP in nominal terms (in Million USD) from a provided URL:
     - [List of countries by GDP (Nominal) on Wikipedia](https://web.archive.org/web/20230902185326/https://en.wikipedia.org/wiki/List_of_countries_by_GDP_%28nominal%29)

2. **Data Transformation**:
   - Convert the GDP values from "Million USD" to "Billion USD", rounding them to two decimal places.

3. **Data Loading**:
   - Save the transformed data in two formats:
     - A **CSV file**: `Countries_by_GDP.csv`
     - An **SQLite database**: `World_Economies.db`, with a table `Countries_by_GDP` containing the columns `Country` and `GDP_USD_billion`.

4. **Database Query**:
   - Run a query on the SQLite database to retrieve and display countries with a GDP greater than 100 billion USD.

5. **Logging**:
   - Log the entire process of the extraction, transformation, and loading steps in a log file: `etl_project_log.txt`, capturing key milestones and execution details with timestamps.

### Project Requirements:

- **Automation**: The script must be capable of running automatically to extract and update the GDP data whenever the IMF releases a new report (twice a year).
- **Data Storage**: Store the processed GDP data in both a CSV file and a relational database (SQLite).
- **Data Query**: Retrieve relevant data by running a query to display countries with GDPs exceeding 100 billion USD.
- **Logging**: Ensure the execution process is logged, including timestamps to track the progress of the ETL pipeline.

### Tools and Technologies:

- **Python** for scripting the ETL process.
- **Libraries**:
  - `requests` and `BeautifulSoup` for web scraping.
  - `pandas` for handling data and saving it to CSV.
  - `sqlite3` for interacting with the SQLite database.
  - `logging` for process logging with timestamps.
  
### Expected Outcomes:

1. **CSV File**: `Countries_by_GDP.csv` containing country names and GDP in billion USD.
2. **Database**: `World_Economies.db` with a table `Countries_by_GDP` storing the same data in a relational database format.
3. **Database Query**: A result set showing countries with GDP greater than 100 billion USD.
4. **Log File**: `etl_project_log.txt` capturing the full ETL process with detailed logs.

### Business Impact:
This automated process will help the firm to stay updated with the latest global economic rankings and support its decision-making when considering expansion opportunities in different countries. By automating the extraction and processing of the GDP data, the firm will save time and ensure accuracy as the IMF updates the data bi-annually.
