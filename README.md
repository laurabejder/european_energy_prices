# European energy prices

This repository contains the code to an automated daily scraper of the energy prices in most European countries, and data on the hourly energy prices and daily average prices since December 1st, 2022. 

The file `index.html` contains the code for the website https://laurabejder.github.io/european_energy_prices/ which displays autoupdating charts of the daily and hourly energy prices of tomorrow. 

### Notebooks
- `1_energy_prices_scrape.ipynb`: Using (mostly) playwright, this notebook scrapes the day-ahead energy prices from the European Network of Transmission System Operators for Electricity's (ENTSO-E) [website](https://transparency.entsoe.eu/transmission-domain/r2/dayAheadPrices/show?name=&defaultValue=false&viewType=GRAPH&areaType=BZN&atch=false&dateTime.dateTime=06.01.2023+00:00|CET|DAY&biddingZone.values=CTY|10YSE-1--------K!BZN|10Y1001A1001A47J&resolution.values=PT15M&resolution.values=PT30M&resolution.values=PT60M&dateTime.timezone=CET_CEST&dateTime.timezone_input=CET+(UTC+1)+/+CEST+(UTC+2)). ENTSO-E is the association for the cooperation of the European transmission system operators (TSOs), and thus has data on most European countries. 
- `2_several_days.ipynb`: This notebook cleans up today's data scrape and appends it to `europaenergy.csv` – a csv containing the hourly prices for all countries since January 5th, 2023.
- `3_reformatting_data.ipynb`: This notebook reformats today's hourly energy prices into a daily average and appends the data to the files used for visualization. 
- `4_earlier_data.ipynb`: This notebook does not run daily but contains the code for a scrape of the energy prices from December 1st, 2022 to January 4th, 2023. By changing the dates, the notebook can easily be expanded to include more past days or focus on a particular timeframe. (e.g., February 2022 if one wants to examine the effect of the Russian invasion of Ukraine).

### Inside the `data` directory:
- `europaenergy_today.csv`: Today's scrape of prices broken down to the hour. Includes the countries in ENTSO-E's system where the prices are missing. 
- `europaenergy.csv`: The hourly prices for all countries since January 5th, 2023
- `links.csv`: File containing all the links for the scrape. One link per country. If several transmission system operators cover the same country, then the csv include a link for each TSO. Some of the links will provide missing values since the prices aren't published, but they are included in the case the prices become available later on. 
- `price_wide.csv`: Longitudinal data of the average daily prices for each country. Wide version that is used for visualization. 
- `prices_long.csv`: Longitudinal data of the average daily prices for each country. Long version.
- `prices_today_hourly`:
- `today_price_long.csv`:
