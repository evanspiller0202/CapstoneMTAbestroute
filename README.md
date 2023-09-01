Evan Spiller's Capstone Project: Lessons for the MTA on bus route planning
=========================

![best_route_gif]("https://github.com/evanspiller0202/CapstoneMTAbestroute/blob/main/reports/Gif_images_bed_to_sh/best_route_gif.gif")

### Project Overview  
This project builds an algorithm to draw the 'best bus routes' in NYC based on data on rideshare usage, which I used to guage demand from one location to another. A detailed explanation of the project's inspiration, logic, methodology and results is provided in FinalPresentation_ Lessons for the MTA_FULL.pptx.

 [Here](https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page) is the data. Since each month of uber and lyft rides has as many as 90M rows, I aggregated the the data by hour and grouped the data into 3 sets of years (2019-2020, 2021, and 2022-3). With those groupings, I was first able to look at key questions about life and transportation in New York City, including effects of the pandemic on work and nightlife commutership, rides after games at Yankee stadium, and the decline and recovery of general and airport commutership from 2019-2023. 

Then, I built a model to find the shortest route, weighted by traffic from adjacent district to adjacent district, from any district to any district. This is built as code in Shortest_Path_Including_Including_Adjacency_Code.ipynb and visualized as an application in SpillerMaps_shortest_path_application.twb. 

Third, I built a model to give the route from location A to location B, given x number of taxi zones passed through, weighted by traffic or amount of fare. The goal is to find a route that potentially would either: a. replace the maximum number of rideshare rides or b. replace the maximum amount spent on rideshares in a certain time period. Code for this is here: Longest_Path_With_Adjacency.ipynb. 

I visualized this in Best_bus_route_FINAL.twb and analyzed the results quantitatively in Analysis_of_results.ipynb.

### Problem and  opportunity

Context: The MTA has a long planning and implementation process, often delayed by politics and an intense process. It's not clear if this is a good way to plan bus routes as traffic patterns may be shifting faster than the MTA is currently planning and implementing routes.

Problem: Design an algorithm to plan routes that optimize for demand. Then, study the speed by which these patterns change in order to evaluate what a sensible timeline for planning new routes would look like.

Opportunity: create an application that finds the a potential bus route from one location to another that would make the most number of for-pay rides unnecessary. Evaluate quantitatively how these routes change over time.


### Glossary of key notebooks

Analysis_of_results.ipynb -- final analysis of results
EDA_Final.ipynb -- EDA on rideshare data with key insights on how this data behaves
File_compressor_NYCTaxisAndRideshares.ipynb -- compresses files on rideshares with designation HFFHV into summary files
File_compressor_NYCTaxisAndRideshares_FHV.ipynb -- compresses files on rideshares with designation FHV into summary files
Longest_Path_Comparison_By_Quarter.ipynb -- this file runs the best bus route algorithm for 15 bus routes
Shortest_Path_Including_Including_Adjacency_Code.ipynb -- this file creates a network for taxi zones in NYC and runs the shortest path algorithm, weighted by total number of trips in 2022

 ### Glossary of key tableau visualizations

Adjacency_spotcheck.twb -- spotchecks my adjacency code used in Shortest_Path_Including_Including_Adjacency_Code.ipynb
Best_bus_route_FINAL.twb -- visualizes best bus routes from Longest_Path_Comparison_By_Quarter.ipynb, showing how routes change over time for 15 proposed bus routes
Main_Pickup_zones_per_dropoff_2022.twb -- visualizes the major pickup zones for each dropoff zone
SpillerMaps_shortest_path_application.twb -- visualizes the shortest paths created in Shortest_Path_Including_Including_Adjacency_Code.ipynb i.e., a highly simplified version of Google Maps for NYC

 ### Glossary of key presentations
 FinalPresentation_ Lessons for the MTA_FULL.pptx -- full final explanation of project and findings

### Project Organization

* `data` 
    - contains 'compressed' aggregated data files that I work with in the majority of this project
    - also contains various inputs and outputs for EDA 
    -- contains midway steps that I input into notebooks and final results which I visualized in tableau

* `notebooks`
    - contains all Jupyter notebooks -- important ones are outlined above

* `tableau`
    - contains visualizations of pathing and mapping used in this project.

* `Reports`
    - contains visuals created throughout the project -- sort of a misnomer but it's referenced in a bunch of notebooks

* `.gitignore`
    - Used to prevent .parquet files from being uploaded to GitHub as they are too large

* `README.md`
    - Project landing page (this page)

