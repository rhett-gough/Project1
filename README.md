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

