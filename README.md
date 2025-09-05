# Lake Level Data Scraper

This repository contains a Python script to scrape lake storage and level data from the Chennai Metropolitan Water Supply and Sewerage Board (CMWSSB) website for specified dates listed in an Excel file.

## Overview

The script utilizes Selenium WebDriver to automate the extraction of lake level data, including reservoir details such as full tank level, storage capacity, current level, inflow, outflow, rainfall, and storage comparison with the previous year. The extracted data is saved into an Excel file for further analysis.

## Prerequisites

- **Python 3.x**
- Required Python libraries:
  - `pandas`
  - `selenium`
  - `webdriver-manager`
- **Chrome WebDriver** (automatically managed by `webdriver-manager`)
- An Excel file containing dates in the format `DD-MM-YYYY` (e.g., `datesn.xlsx`)

### Installation

1. Clone the repository:
   ```
   git clone github.com/Rupesh4604/Lake-Level-Data-Scraper.git
   cd Lake-Level-Data-Scraper
   ```

2. Install the required Python packages:
   ```
   pip install pandas selenium webdriver-manager
   ```

3. Ensure an Excel file named `datesn.xlsx` with a column of dates is available in the project directory. Update the `excel_file_path` variable in the script if the file name or path differs.

## Usage

1. Prepare an Excel file (e.g., `datesn.xlsx`) with a column of dates in `DD-MM-YYYY` format.
2. Run the script:
   ```
   python dataScrapper.py
   ```

3. The script will:
   - Test the scraper with a single date (`04-08-2023` by default).
   - Prompt for confirmation to proceed with scraping all dates from the Excel file.
   - Save the extracted data to `lake_level_extract.xlsx`.

4. Review the output file and console logs for the scraped data and any errors.

## Configuration

- Modify `excel_file_path` in the `main()` function to point to your Excel file.
- Adjust `output_file_path` if a different output file name is preferred.
- Customize `desired_headers` in the `LakeLevelScraper` class to match the table columns if the website structure changes.

## Notes

- The script includes a delay between requests to respect the website's server load.
- Run in a non-headless mode initially to verify the scraping process; enable headless mode by uncommenting the relevant line in `setup_driver()`.
- Ensure the CMWSSB website structure remains consistent, as changes may require script updates.


## Contributing

Contributions are welcome. Please fork the repository and submit pull requests for any improvements or bug fixes.

## Contact

For questions or support, please open an issue in the repository.
