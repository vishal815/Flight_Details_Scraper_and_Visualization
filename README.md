# Flight Data Scraper and Visualization

## Overview
This project focuses on scraping flight details from [Google Flights](https://www.google.com/travel/flights?gl=IN&hl=en), processing the data, and performing cleaning and visualization for future use in analytics or predictive modeling.

## Workflow step-by-step
![web_scraping_workflow](https://github.com/user-attachments/assets/23379c68-2f55-4110-b40a-89cd9fd4c002)

## Features
- **Web Scraping**: Extracts detailed flight information, including:
  - Airline names
  - Flight duration
  - Price
  - Departure and arrival times
  - Departure and arrival dates
  - Airports
  - Stops
  - CO2 emissions
- **Data Cleaning**: Processes and filters scraped data to handle missing or unavailable values.
- **CSV Outputs**: Saves data in various stages for easy access and further use.

)
## Website
Data is scraped from [Google Flights](https://www.google.com/travel/flights?gl=IN&hl=en).

![Detailed flight information which I am going to Scrap](![Screenshot 2025-01-15 084745](https://github.com/user-attachments/assets/1d87c857-eba2-4f17-b0d4-65c3dee70983)

## Generated Files
1. `google_flights_data.csv`: Raw flight data scraped from the website.
2. `price_unavailable_data.csv`: Records where price information is unavailable.
3. `cleaned_google_flights_data.csv`: Cleaned and processed dataset ready for analysis.

## Technologies Used
- **Python**
- **Selenium**: For browser automation and interaction.
- **BeautifulSoup**: For parsing HTML and extracting data.
- **Pandas**: For data manipulation and cleaning.

## Steps to Run
1. **Install Dependencies**:
   ```bash
   pip install selenium beautifulsoup4 pandas
   ```
2. **Set Up ChromeDriver**:
   - Download the appropriate version of ChromeDriver from [here](https://chromedriver.chromium.org/downloads).
   - Update the path to the driver in the script.
3. **Run the Script**:
   ```bash
   python scrape_flight_details_and_visualization.ipynb
   ```
4. **Check Outputs**:
   - The scraped data will be saved as CSV files in the working directory.

## Data Flow
1. **Scraping**:
   - Selenium navigates to the specified Google Flights URL.
   - BeautifulSoup parses the HTML to extract flight details.
2. **Data Cleaning**:
   - Processes columns like "Price" and "Arrival Time."
   - Saves filtered data to `cleaned_google_flights_data.csv`.

## Example Output
| Airline | Flight Duration | Price    | Departure Time | Departure Date | Departure Airport                              | Arrival Time | Arrival Date | Arrival Airport           | Stops  | CO2 Emissions | Next Day Dispatcher |
|---------|-----------------|----------|----------------|----------------|-----------------------------------------------|--------------|--------------|---------------------------|--------|---------------|---------------------|
| IndiGo  | 11 hr 30 min    | ₹27,515  | 8:45 AM        | Sun, Feb 2     | Jayprakash Narayan International Airport, Patna | 6:45 PM      | Sun, Feb 2   | Zayed International Airport | 1 stop | 266 kg CO2e   | 0                   |
| IndiGo  | 11 hr 15 min    | ₹28,349  | 12:40 PM       | Sun, Feb 2     | Jayprakash Narayan International Airport, Patna | 10:25 PM     | Sun, Feb 2   | Zayed International Airport | 1 stop | 257 kg CO2e   | 0                   |


## some output of visualization
![image](https://github.com/user-attachments/assets/9c5eb579-aa6c-40da-b43c-6b845f87bc3f)

![image](https://github.com/user-attachments/assets/97e9a9d2-f4ba-4905-9f1c-88f7de3ec21f)


## Future Work
- Autometion using crontab linux.
- Collect more data for extended analysis.
- Implement advanced visualization techniques.
- Apply ML/DL models for predictive analytics, such as estimating missing flight prices.

## License
This project is licensed under the MIT License. See the LICENSE file for more details.

---

*For questions or contributions, feel free to open an issue or submit a pull request.*
## Vishal Lazrus

