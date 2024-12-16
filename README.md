# mars_website_data_scraping

This repository contains code for scraping and analyzing data from a Mars-related website, specifically focusing on news articles and weather data. The project is divided into two parts:

## Part 1: Scrape Titles and Preview Text from Mars News

This part focuses on scraping titles and preview text from Mars news articles.

### Files

-   **part_1_mars_news.ipynb**: Jupyter Notebook containing the code for scraping Mars news titles and preview text using Splinter and Beautiful Soup.
-   **part_1_mars_news.pdf**: PDF file explaining the code in `part_1_mars_news.ipynb` step-by-step.

### Description

The Jupyter Notebook `part_1_mars_news.ipynb` automates the process of visiting the [Mars News website](https://static.bc-edx.com/data/web/mars_news/index.html) using Splinter, extracting the HTML content, and then parsing it with Beautiful Soup to scrape titles and preview text of news articles. The scraped data is stored in a list of dictionaries, where each dictionary represents a news article and contains the keys "title" and "preview". The code then prints the list of dictionaries and optionally exports it to a JSON file.

**Key Steps in the Notebook:**

1. **Import Libraries:** Imports necessary libraries (Splinter, BeautifulSoup, json).
2. **Setup Splinter:** Initializes the Chrome browser.
3. **Visit Website:** Navigates to the Mars News website.
4. **Parse HTML:** Extracts and parses the HTML content using BeautifulSoup.
5. **Create Empty List:** Initializes a list to store the scraped data.
6. **Find All News Articles:** Locates all div elements containing news article information.
7. **Loop Through Each Article:** Iterates through each article element.
8. **Extract Title and Preview:** Extracts the title and preview text from each article.
9. **Create Dictionary:** Stores the title and preview in a dictionary.
10. **Add Dictionary to List:** Appends the dictionary to the list.
11. **Print and Export List:** Prints the list and optionally exports it to a JSON file.
12. **Quit Browser:** Closes the browser instance.

## Part 2: Scrape and Analyze Mars Weather Data

This part focuses on scraping and analyzing Mars weather data, which is presented in a table format on the website.

### Files

-   **part_2_mars_weather.ipynb**: Jupyter Notebook containing the code for scraping and analyzing Mars weather data using Splinter, Beautiful Soup, Pandas, and Matplotlib.
-   **part_2_mars_weather.pdf**: PDF file explaining the code in `part_2_mars_weather.ipynb` step-by-step.

### Description

The Jupyter Notebook `part_2_mars_weather.ipynb` automates the process of visiting the [Mars Temperature Data website](https://static.bc-edx.com/data/web/mars_facts/temperature.html) using Splinter, extracting the HTML content, and then parsing the table data with Beautiful Soup. The scraped data is then loaded into a Pandas DataFrame, where data types are adjusted, and various analyses are performed. Finally, the results are visualized using Matplotlib, and the DataFrame is exported to a CSV file.

**Key Steps in the Notebook:**

1. **Import Libraries:** Imports necessary libraries (Splinter, BeautifulSoup, Pandas, Matplotlib).
2. **Setup Splinter:** Initializes the Chrome browser.
3. **Visit Website:** Navigates to the Mars Temperature Data website.
4. **Parse HTML:** Extracts and parses the HTML content using BeautifulSoup.
5. **Find Table:** Locates the HTML table element.
6. **Extract Data Rows:** Extracts all data rows from the table.
7. **Create Empty List:** Initializes a list to store the extracted data.
8. **Loop Through Rows:** Iterates through each row in the table.
9. **Extract Data from Each Row:** Extracts data from each cell in the row.
10. **Create Dictionary:** Stores the extracted data in a dictionary.
11. **Add Dictionary to List:** Appends the dictionary to the list.
12. **Create DataFrame:** Creates a Pandas DataFrame from the list of dictionaries.
13. **Examine Data Types:** Prints the data types of each column.
14. **Convert Data Types:** Converts columns to appropriate data types (datetime, int, float).
15. **Data Analysis:** Performs calculations like:
    -   Number of unique months.
    -   Number of unique Martian days.
    -   Average minimum temperature by month.
    -   Coldest and warmest months.
    -   Average pressure by month.
    -   Lowest and highest pressure months.
    -   Estimate the length of a Martian year in Earth days.
16. **Data Visualization:** Creates visualizations using Matplotlib:
    -   Bar chart of average minimum temperature by month.
    -   Bar chart of average pressure by month.
    -   Line plot of daily minimum temperature to estimate Martian year length.
17. **Export DataFrame:** Exports the DataFrame to a CSV file.
18. **Quit Browser:** Closes the browser instance.

## Summary of Results from Part 2

-   Mars experiences significant temperature variations throughout its year, with a difference of about 15°C between the coldest and warmest months, on average.
-   Atmospheric pressure on Mars also changes throughout the year, and there appears to be an inverse relationship between temperature and pressure.
-   A Martian year is estimated to be approximately 675 Earth days long, based on the analysis of temperature cycles.

## Getting Started

To run the code in this repository, you will need to have the following libraries installed:

-   splinter
-   beautifulsoup4
-   pandas
-   matplotlib

You can install these libraries using pip:

```bash
pip install splinter beautifulsoup4 pandas matplotlib
```

You will also need to have a compatible WebDriver installed for Splinter. The code uses the Chrome WebDriver, which you can download from the [official website](https://chromedriver.chromium.org/).

## Usage

1. Clone the repository to your local machine:

    ```bash
    git clone https://github.com/your_username/mars_website_data_scraping.git
    ```

    Replace `your_username` with your actual GitHub username.
2. Navigate to the repository directory:

    ```bash
    cd mars_website_data_scraping
    ```

3. Open and run the Jupyter Notebooks (`part_1_mars_news.ipynb` and `part_2_mars_weather.ipynb`) using Jupyter Notebook or Jupyter Lab.

4. Make sure to update the path to your WebDriver in the notebooks if it's not in the default location.

## Contributing

Contributions to this project are welcome. Please feel free to fork the repository, make changes, and submit a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details. (Note: You should add a LICENSE file to your repository).
