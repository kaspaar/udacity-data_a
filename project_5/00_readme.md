# Flights data exploration
## by Kacper Fiszer


## Dataset

#### Gathering
For this project I used US flights data pack.  
It is described here: [http://stat-computing.org/dataexpo/2009/the-data.html](http://stat-computing.org/dataexpo/2009/the-data.html)

The data was supposed to be available under the above link, but wasn't.  
Downloaded the same file from: [https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/HG7NV7](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/HG7NV7)

Extracted files are in the csv format, year by year. I put them all in `data` directory.

The whole data available consisted of years 1987-2008.  
For this particular project I've picked years 2005-2007 (2008 had data only for the first months).

#### Cleaning
Cleaning is documented in `01_flights_wrangling.ipynb` notebook and `01_flights_wrangling.html`.

#### Output
For further analysis I used cleaned files:
- `flights_clean.csv`
- `flights_cancelled.csv`  

They are zipped and can be downloaded from here:  
[https://www.dropbox.com/sh/dlhlij00h43naw5/AADFNNeEVtPDRXZqZAX2iImqa?dl=0](https://www.dropbox.com/sh/dlhlij00h43naw5/AADFNNeEVtPDRXZqZAX2iImqa?dl=0)

## Summary of Findings
Exploration is documented in `02_flights_exploration.ipynb` notebook and `02_flights_exploration.html`.

I have looked at the following relations and included most of them in the final presentation.
It would be interesting to dig deeper and look for more low-level possible delay relations, eg. with carriers or particular airports.

#### All flights (sample)
- Relation between distance and arrival delay (bivariate)
- Relation between departure delay and arrival delay (bivariate)
- Relation between scheduled flight time and actual elapsed flight time (bivariate)  
  
  
- Relation between departure delay and arrival delay + categorical distance (univariate)
- Relation between scheduled flight time and actual elapsed flight time + categorical distance (univariate) 

#### Cancelled/diverted flights subset:
- Count of cancelled or diverted flights by year (univariate)  
To see if there are significant changes year-to-year
- Count of cancelled or diverted flights by month (univariate)  
Potential correlation might indicate seasonal cause-effect
- Count of cancelled or diverted flights by day of week  
Are there more cancelled or diverted flights during specific week days?
- Count of cancelled or diverted flights by distance (univariate)  
Could flight distance influence cancellations or diverting?
- Proportion of cancellation codes (univariate)  
To see what are the most frequent reasons of flight cancellation.
  
  
- Count of cancelled or diverted flights by year and month or month and day of week (bivariate)  
To better understand time-related trends.
- Cancellation codes in relation to flight distance (bivariate)
Could these be related?


## Key Insights for Presentation
The presentation notebook is `03_flights_slidedeck.ipynb` and the slides are stored as `03_flights_slidedeck.slides.html`.

Key points are:
- High-level overview of how delays relate to other variables.  
This doesn't provide anything ground breaking, but realising that there is no significant relationship is often equally important.
- Demonstration of how cancelled/diverted flights spread across months and days of week.
- Wrapping up with a look at different cancellation reasons and how they span.