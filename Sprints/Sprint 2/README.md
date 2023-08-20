Evan Spiller's Capstone
=========================

### Project Overview  
I'm currently exploring a dataset of NYC taxi and rideshare rides that exists from 2009-2023. [Here](https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page) is the data. Since each month of uber and lyft rides has as many as 90M rows, I aggregated the the data by hour and grouped the data into 3 sets of years (2019-2020, 2021, and 2022-3). With those groupings, I was first able to look at key questions about life and transportation in New York City, including effects of the pandemic on work and nightlife commutership, rides after games at Yankee stadium, and the decline and recovery of general and airport commutership from 2019-2023. 

Then, I built a model to find the shortest route, weighted by traffic from adjacent district to adjacent district, from any district to any district. This is built as code in Shortest_Path_Including_Including_Adjacency_Code.ipynb and visualized as an application in SpillerMaps.twb. 

Finally, I built a model to give the route from location A to location B, given x number of taxi zones passed through, weighted by traffic, which would potentialy serve as a bus route that made redundant the largest number of Uber/Lyft rides -- a way to poentially plan bus routes to eliminate maximum traffic from rideshares. Code for this is here: Longest_Path_With_Adjacency.ipynb. I am working on the visualization, data collection and presentation now.

### Problem and  opportunity

Context: A huge amount of for-pay rides are < 2 miles. Just in January: New Yorkers spent $54M on rides < 2 miles. This represents a failure of public transit to serve New Yorker’s basic transit needs, increasing traffic and costing New Yorkers money and experiences. 

Problem: Increase bus ridership by designing routes with high demand. Furthermore, study the speed by which these patterns change in order to understand the utility of MTA’s multi-year planning process.

Opportunity: create an application that finds the a potential bus route from one location to another that would make the most number of for-pay rides unnecessary. Furthermore, predict how these routes will change over time.


### Walkthrough Demo

Begin by opening and running File_compressor_NYCTaxisAndRideshares -- this will aggregate the public data into managable files. So far, I've run it for rideshares from 2019-2023, but will include older rideshare and taxi data as well in the future.

Then, view the file NYC_TaxiRideshare_EDA. This is a file that contains several exploratory visualizations and experiments that tell you key facts about what you should expect to see inside the data.

Next, view the code in in Shortest_Path_Including_Including_Adjacency_Code.ipynb and the visualization in SpillerMaps.twb to see a rudimentary tool for drivers to view the best path from place to place for NYC.

Next, view Longest_Path_With_Adjacency.ipynb to see the modeling for potential bus routes.  

### Project Organization

* `data` 
    - contains 'compressed' aggregated data files that I work with in the majority of this project
    - also contains various inputs and outputs for EDA

* `notebooks`
    - contains all notebooks, including NYC_TaxiRideshare_EDA, Shortest_Path_Including_Including_Adjacency_Code.ipynb, Longest_Path_With_Adjacency.ipynb. Once the project is finalized I will put the key notebooks in a special and the ones that involved more exploratory work in another notebook.

* `tableau`
    - contains visualizations of pathing and mapping used in this project.

* `reports`
    - Will contain final reports

* `.gitignore`
    - Used to prevent .parquet files from being uploaded to GitHub as they are too large

* `README.md`
    - Project landing page (this page)

