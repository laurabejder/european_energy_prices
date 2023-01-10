# European energy prices

This repository contains the code to an automated daily scraper of the energy prices in most European countries, and data on the hourly energy prices and daily average prices since December 1st, 2022. 

### Notebooks
- `1_energy_prices_scrape.ipynb`: This notebook scrapes the day-ahead energy prices from the European Network of Transmission System Operators for Electricity's (ENTSO-E) [website](https://transparency.entsoe.eu/transmission-domain/r2/dayAheadPrices/show?name=&defaultValue=false&viewType=GRAPH&areaType=BZN&atch=false&dateTime.dateTime=06.01.2023+00:00|CET|DAY&biddingZone.values=CTY|10YSE-1--------K!BZN|10Y1001A1001A47J&resolution.values=PT15M&resolution.values=PT30M&resolution.values=PT60M&dateTime.timezone=CET_CEST&dateTime.timezone_input=CET+(UTC+1)+/+CEST+(UTC+2)). ENTSO-E is the association for the cooperation of the European transmission system operators (TSOs), and thus has data on most European countries. 

###Inside the `data` directory:
Scrapers written using Playwright (mostly) for pending murder cases from courts of five different districts in Maharashtra state of India.
The data on the website gets updated every single day.
The data was scraped within a span of three days in the first week of December 2022.
Inside original scrapes folder:
A folder named after each district.
Some districts have multiple district-level courts operating inside its limit.
Therefore, each folder contains files of every district-level court in the district that folder is named after.
The subfolder named JOINED_FILES contains consolidated data of all disitrict-level courts in that district.
You are free to either used the original files or use the consolidated files.
Inside Cleaning and analysis folder:
Jupyter notebook containing data cleaning and analysis for class project.
Inside map_stuff zip file:
This contains a javascript file that is home to mapping coordinates (in form of geojson), formatting, and corresponding data for five selected districts.
It also has a html page that shows the mapped version of the data.
