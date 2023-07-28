Evan Spiller's Capstone
=========================

### Project Overview  
I'm currently exploring a dataset of NYC taxi and rideshare rides that exists from 2009-2023. [Here](https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page) is the data. Since each month of uber and lyft rides has as many as 90M rows, I aggregated the the data by hour and grouped the data into 3 sets of years (2019-2020, 2021, and 2022-3). With those groupings, I was able to look at key questions about life and transportation in New York City, including effects of the pandemic on work and nightlife commutership, rides after games at Yankee stadium, and the decline and recovery of general and airport commutership from 2019-2023. I'd like to go further and compare traffic patterns to current plans to remake Brooklyn's bus system and to create optimal bus routes that maximize ridership and evaluate whether patterns are shifting too quickly for the multi-year process to ensure maximum ridership.

### Problem and  opportunity

Context: A huge amount of for-pay rides are < 2 miles. Just in January: New Yorkers spent $54M on rides < 2 miles. This represents a failure of public transit to serve New Yorker’s basic transit needs, increasing traffic and costing New Yorkers money and experiences. 

Problem: Increase bus ridership by designing routes with high demand. Furthermore, study the speed by which these patterns change in order to understand the utility of MTA’s multi-year planning process.

Opportunity: create an application that finds the a potential bus route from one location to another that would make the most number of for-pay rides unnecessary. Furthermore, predict how these routes will change over time.


### Walkthrough Demo

Begin by opening and running File_compressor_NYCTaxisAndRideshares -- this will aggregate the public data into managable files. So far, I've run it for rideshares from 2019-2023, but will include older rideshare and taxi data as well in the future.

Next, view the file NYC_TaxiRideshare_EDA. This is a file that contains several exploratory visualizations and experiments that tell you key facts about what you should expect to see inside the data.

### Project Organization

* `data` 
    - contains 'compressed' aggregated data files that I work with in the majority of this project
    - also contains various inputs and outputs for EDA

* `notebooks`
    - contains all notebooks, including some rough work that ultimately ended up in NYC_TaxiRideshare_EDA, involved in the project. Once the project is finalized I will clean some of these up -- but most contain code and formulas that I've been copying for other work.

* `reports`
    - Will contain final reports

* `.gitignore`
    - Used to prevent .parquet files from being uploaded to GitHub as they are too large

* `README.md`
    - Project landing page (this page)

