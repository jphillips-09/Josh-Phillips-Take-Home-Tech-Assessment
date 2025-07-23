# Small Data Pipeline and EDA Project
NYC 311 Service Requests from NYC Open Data website

## Project Overview
This project loads and processes all NYC 311 service request records from 1/1/2010 - 7/18/2025 using the NYC OpenData API (found [here)](https://data.cityofnewyork.us/Social-Services/311-Service-Requests-from-2010-to-Present/erm2-nwe9/about_data), and aims to analyze / identify key trends of the dataset. 

* V1 of The Data QA / Ingestion Notebook can be found [here](01_data_ingestion.ipynb). This was my initial attempt to download all rows of the dataset, which did not run correctly due to API/data volume constraints.
* V2 of The Data QA / Ingestion Notebook can be found [here](01_data_ingestion_v2.ipynb). This is my revised notebook that downloads the latest 1,000 rows of the dataset.
* The EDA Notebook can he found here [here](02_eda.ipynb), which produces 3 visuals from the latest 1,000 rows of the dataset.

## Data Methodology: 

* Data Description: This dataset represents all NYC 311 Service Requests from 1/1/2010 onwards, provided by NYC 311. Only service requests that can be directed to specific agencies are included.
  
* Publishing Frequency: The dataset is refreshed and updated daily. Note that values for many fields may change over time. 
  
* Unique Limitations / Risks: This dataset does not include inquiries, some of which appear in the 311 Call Center Inquiry dataset or requests to agencies which have their own customer service response systems, like the New York City Housing Authority (NYCHA) or New York City Department of Corrections (DOC). This data has been geocoded before being published to NYC Open Data. Certain fields have been added to provide additional geospatial references, using GeoSupport and the street address provided in the original service request.  The complete list of geocoded fields in this dataset could not be verified. Additionally, keep in mind, this data represents complaints about the city, as opposed to objective snapshots of city services. For example, if a significant number of noise complaints come from one neighborhood, it doesn’t mean it’s the noisiest neighborhood in the city -- rather, that more people are complaining about noise there.

## Key Takeaways / Questions 

#### 1. Which borough has the most 311 service requests?
According to the latest 1,000 rows of data, The Bronx has the most 311 Service Requests. 

<img width="452" height="429" alt="image" src="https://github.com/user-attachments/assets/4dc74806-7249-45ea-8e06-c03925e65591" />

#### 2. Does 311 request volume correlate with borough population?
Yes, there appears to be a strong correlation between borough population and the amount of 311 service requests, although the Bronx is an outlier with higher-than-expected volume.

<img width="451" height="358" alt="image" src="https://github.com/user-attachments/assets/02094336-ce36-4f66-9ef9-be8dd83a14a8" />

#### 3. What are the most common 311 service complaint types?
Noise - Street/Sidewalk and Noise - Residential are the most frequent complaint types.

<img width="452" height="502" alt="image" src="https://github.com/user-attachments/assets/8c35b368-892f-45fd-9f85-e6dde7ac9804" />

## Other Questions This Data Could Answer 
#### 1. How have NYC 311 service requests grown over time? 
#### 2. Which months typically have the most 311 service requests (i.e. are there seasonal trends)?
#### 3. What is the average time it takes to resolve a 311 service request?
#### 4. Which types of 311 service complaints take the longest to resolve?
#### 5. What percentage of 311 service requests remain unresolved or have no recorded close date?
#### 6. What percentage of 311 service requests are likely duplicates or overlapping (i.e., similar complaints made in the same area within a short timeframe)?

## Sources
Given my limited Python experience, I relied heavily on the guides below (amongst other sources) to learn how to ingest, clean and wrangle the data:
* Rob Mulla - [Exploratory Data Analysis with Pandas Python](https://www.youtube.com/watch?v=xi0vhXFPegw&t=1279s)
* Keith Galli - [How to work with big data files (5gb+) in Python Pandas!](https://www.youtube.com/watch?v=l34l-90UF7U&t=136s)
* Misra Turp - [How to Do Data Cleaning (step-by-step tutorial on real-life dataset)](https://www.youtube.com/watch?v=qxpKCBV60U4&t=532s)
* Corey Schafer - [Python Pandas Tutorial (Part 2): DataFrame and Series Basics - Selecting Rows and Columns](https://www.youtube.com/watch?v=zmdjNSmRXF4&t=799s)
* Python Simplified - [Read Giant Datasets Fast - 3 Tips For Better Data Science Skills](https://www.youtube.com/watch?v=x2DxiL8WOmc&t=640s)






