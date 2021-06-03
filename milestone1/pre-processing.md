# Project of Data Visualization (COM-480)

| Student's name | SCIPER |
| -------------- | ------ |
| Charlyne Bürki | 261415 |
| Arnaud Dhaene  | 269883 |
| Marijn van der Meer | 247273 |

## Pre-processing for Milestone 1: 

### Dataset

> Find a dataset (or multiple) that you will explore. Assess the quality of the data it contains and how much preprocessing / data-cleaning it will require before tackling visualization. We recommend using a standard dataset as this course is not about scraping nor data processing.
>
> Hint: some good pointers for finding quality publicly available datasets ([Google dataset search](https://datasetsearch.research.google.com/), [Kaggle](https://www.kaggle.com/datasets), [OpenSwissData](https://opendata.swiss/en/), [SNAP](https://snap.stanford.edu/data/) and [FiveThirtyEight](https://data.fivethirtyeight.com/)), you could use also the DataSets proposed by the ENAC (see the Announcements section on Zulip).

The chosen dataset contains listings and reviews of Airbnb listings in Switzerland. The data is pulled from [Inside Airbnb](http://insideairbnb.com/get-the-data.html) for regions specified in [Project organization](##project-organization).

#### Structure of the data files

The latest data is updated on [Inside Airbnb](http://insideairbnb.com/get-the-data.html) every so often for each available region. The dataset that was processed in the framework of Milestone 1 consists of a merged dataset of the following regions:

* Geneva (2072 listings), data compiled on February 25, 2021
* Vaud (4344 listings), data compiled on February 04, 2021
* Zurich (1806 listings), data compiled on February 26, 2021

Each of the above-mentioned regions contains the following information:

* Detailed Listings data, found in `listings-detailed.csv`
* Detailed Calendar data, found in `calendar.csv`
* Detailed Review data, found in `reviews-detailed.csv`
* Summary information and metrics for Listings, found in `listings.csv`
* Summary Review data and Listing ID, found in `reviews.csv`
* Neighbourhood list for geo filter, found in `neighbourhoods.csv`
* GeoJSON file or neighbourhoods of the region, found in `neighbourhoods.geojson`

In addition to this, archived data going back to January 2020 is available for some of the datasets. 

### Listings

##### Pre-processing

The listings table is relatively clean when downloaded from [Inside Airbnb](http://insideairbnb.com/get-the-data.html). Some routine formatting includes formatting the dates into a readable datetime format, parsing the price, counting the amount of amenities, and reducing the amount of possible property types from 68 to one of {Entire place, Private room, other} using simple parsing.

Additionally, a feature is added that contains the days a listing's host has been a Airbnb host.

The features for the available listings are: 

* Scraping (ID, timestamp)
* Listing (name, description, price)
* Neighborhood
* Host (name, signup date, location, about, response time, response rate, acceptance rate, superhost, thumbnail, picture, neighboorhoud, amoung of lisitings, verifications, verified)
* Location (longitude and latitude)
* Property (beds, bedrooms, bathrooms, amenities)
* Reviews (rating, accuracy, cleanliness, check-in, communication, location, value, amount of reviews per month)
* Availability (minimum and maximum number of nights, availability for the next 30, 60, 90, and 365 days)

### Calendar

##### Pre-processing

The calendar data contains price per night predictions and availabilities for listings a few months into the future. The price was formatted into parseable data and all dates were changed into readable datetime format. 

The features for the calendar data after pre-processing are: 

* Time-stamp
* Listing ID 
* Availability on a date
* Price [$/night]
* Max/Min nights

### Reviews

##### Pre-processing

The reviews data contains the listing ID and the date at which a review was made. All dates were changed into readable datetime format.  

The features for the reviews data after pre-processing are: 

* Time-stamp
* Listing ID 
