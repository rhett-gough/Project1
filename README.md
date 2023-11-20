# COVID-19 Statistics in North Carolina and the United States

## Big Picture Question:
### What trends in North Carolina COVID-19 data can we measure, and how do they compare and contrast with National COVID-19 data?

## Data Sources:
### The COVID Tracking Project
The COVID Tracking Project is an initiative by the Atlantic Monthly Group to collect and aggregate COVID-19 related data for analysis. They measured for things like COVID-19 related hospitalizations, testing, deaths, and more. From the COVID Tracking Project, we were able to obtain the following datasets via CSV:
* US-level summary data from January 2020 to March 2021 (https://covidtracking.com/data/download/national-history.csv)
  * This is located in the Resources folder under "national-history.csv"
* NC-level summary data from March 2020 to March 2021 (https://covidtracking.com/data/download/north-carolina-history.csv)
  * This is located in the Resources folder under "north-carolina-history.csv"
* NC-level race and ethnicity data (https://covidtracking.com/data/state/north-carolina/race-ethnicity)
  * This is located in the Resources folder under "north-carolina-race-ethnicity-historical.csv"
 
### US Census Bureau
The US Census Bureau creates population statistics every 10 years. We were able to use their population estimates for 2020 and 2021 to create per-capita data. From the US Census Cureau we were able to collect the following dataset via CSV:
* Estimated population data for 2020 through 2022 (https://www2.census.gov/programs-surveys/popest/datasets/2020-2022/state/totals/NST-EST2022-ALLDATA.csv)
  * This is located in the Resources folder under "NST-EST2022-ALLDATA.csv"
 
### OpenWeatherAPI
The OpenWeatherAPI allows you to pull in many weather related statistics for analysis. We attempted to pull average temperature data from the OpenWeatherAPI to see if temperature had a role in COVID-19 outcomes. (https://openweathermap.org/)

## Questions to Answer
* How did North Carolina and United States COVID-19 data compare over time?
* Is there a correlation between positive COVID tests and hospitalizations?
* Is there a correlation between the number of tests administered and deaths?
* Is there a correlation between positive COVID test and temperature?
* What was the ratio of viral tests to antigen tests in North Carolina, and did the 9/30/20 introduction of antigen tests impact the state’s overall negative testing rate?
* How do mortality rates in North Carolina compare between different racial/ethnic groups? Is there a correlation between the total of cases to deaths?

## Data Data Retrieval and Assembly
1. We downloaded the data from The COVID Tracking Project and the US Census Bureau to include in our repository for analysis.
2. We obtained an API key from OpenWeatherAPI to access average temperature data.
3. Using Pandas we cleaned the data from the COVID Tracking Project to isolate only the variables of interest from both US and NC. We also added population estimates from the US Census Bureau We then merged all this data to create the combined CSV that can be found in Resources under "US_NC_Combined". Code for data cleanging can be found in "adding_populatin_columns.ipynb".
4. Using matplotlib, we created charts to analyze data and uncover trends.

## How did North Carolina and United States COVID-19 data compare over time?
### Tests per capita
#### Code for charts can be found in "..."
* MS analysis

### Hospitalizations and Deats per capita
#### Code for charts can be found in "GoughE_NCvUS_TimelineTrends.ipynb".
* After creating per capita variables for the increase in COVID-19 hospitalizations and COVID-19 related deaths, we were able to find the North Carolina performed slightly better than the nation as a whole. NC was not subject to the two peaks in hospitalizations that occurred in the US in May 2020 and July 2020, but roughly mirrored the US's pattern after that, while mostly remaining below the US's hospitalization rates.
* A first attempt at graphing the increase in COVID-19 related deaths created unreadable data due to the variability. As a result, data was grouped by the sum of deaths per month. The US and NC's COVID-19 realted deaths pattern over time is very similar to the hospitalization rate. A very notable difference is that for September and October 2022 that NC had more deaths per capita than the US.

## Is there a correlation between positive COVID tests and hospitalizations?
#### Code for charts can be found in "...".
* KM analysis

## Is there a correlation between the number of tests administered and deaths?
#### Code for charts can be found in "...".
* JA analysis

## Is there a correlation between positive COVID test and temperature?
#### Code for charts can be found in "...".
* MS analysis

## What was the ratio of viral tests to antigen tests in North Carolina, and did the 9/30/20 introduction of antigen tests impact the state’s overall negative testing rate?
#### Code for charts can be found in "...".
* AM analysis

## How do mortality rates in North Carolina compare between different racial/ethnic groups? Is there a correlation between the total of cases to deaths?
#### Code for charts can be found in "...".
* JL analysis

## Data Limitations
* The US Census didn't have consistent month by month estimates for the date ranges we were looking for, and as a result the same population number was used for all 2020 data, and all 2021 data. With more robust population data, the analysis would be more accurate.
* 
