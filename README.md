# EDA-Project
NYC 311 Service Requests from NYC Open Data website

## Project Overview
This project loads and processes all NYC 311 service request records from 1/1/2010 - 7/18/2025 using the NYC OpenData API (found [here)](https://data.cityofnewyork.us/Social-Services/311-Service-Requests-from-2010-to-Present/erm2-nwe9/about_data), and aims to analyze / identify key trends of the dataset. 

## Data Methodology: 

* Data Description: This dataset represents all NYC 311 Service Request from 1/1/2010 onwards, provided by NYC 311. Only service requests that can be directed to specific agencies are included.
  
* Publishing Frequency: The dataset is refreshed and updated daily. Note that values for many fields may change over time. 
  
* Unique Limitations / Risks: This dataset does not include inquiries, some of which appear in the 311 Call Center Inquiry dataset or requests to agencies which have their own customer service response systems, like the New York City Housing Authority (NYCHA) or New York City Department of Corrections (DOC). This data has been geocoded before being published to NYC Open Data. Certain fields have been added to provide additional geospatial references, using GeoSupport and the street address provided in the original service request.  The complete list of geocoded fields in this dataset could not be verified. Additionally, keep in mind, this data represents complaints about the city, as opposed to objective snapshots of city services. For example, if a significant number of noise complaints come from one neighborhood, it doesn’t mean it’s the noisiest neighborhood in the city -- rather, that more people are complaining about noise there.

## Key Takeaways 
1. How have NYC 311 service requests grown over time?
2. Which month typically has the most 311 service requests?
3. Which borough has historically had the most 311 service requests? Which ZIP Code?
4. What is the most common 311 service complaint type?

## Other Questions This Data Could Answer: 
1. What is the average time it takes to complete a 311 service request?
2. What percentage of 311 service requests are never resolved / closed?
3. What percentage of 311 service requests are overlapping (i.e. same request made on multiple occasions)? (This is possible to approximate by filtering for similar complaint_types / descriptors in a similar location and timeframe, and by seeing when the request is resolved / closed)


## Sources
Given my limited Python experience, I relied heavily on the guides below (amongst other sources) to learn how to ingest, clean and wrangle the data:
* Rob Mulla - [Exploratory Data Analysis with Pandas Python](https://www.youtube.com/watch?v=xi0vhXFPegw&t=1279s)
* Keith Galli - [How to work with big data files (5gb+) in Python Pandas!](https://www.youtube.com/watch?v=l34l-90UF7U&t=136s)
* Misra Turp - [How to Do Data Cleaning (step-by-step tutorial on real-life dataset)](https://www.youtube.com/watch?v=qxpKCBV60U4&t=532s)
* Corey Schafer - [Python Pandas Tutorial (Part 2): DataFrame and Series Basics - Selecting Rows and Columns](https://www.youtube.com/watch?v=zmdjNSmRXF4&t=799s)
* Python Simplified - [Read Giant Datasets Fast - 3 Tips For Better Data Science Skills](https://www.youtube.com/watch?v=x2DxiL8WOmc&t=640s)






