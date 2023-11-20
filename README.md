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
The US Census Bureau creates population statistics every 10 years. We were able to use their population estimates for 2020 and 2021 to create per-capita data. From the US Census Bureau, we were able to collect the following dataset via CSV:
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
3. Using Pandas we cleaned the data from the COVID Tracking Project to isolate only the variables of interest from both US and NC. We also added population estimates from the US Census Bureau We then merged all this data to create the combined CSV that can be found in Resources under "US_NC_Combined". Code for data cleaning can be found in "adding_populatin_columns.ipynb".
4. Using matplotlib, we created charts to analyze data and uncover trends.

## How did North Carolina and United States COVID-19 data compare over time?
### Positive Cases per capita
#### Code for charts can be found in "MS_Timeline1a_1b.ipynb"
* In order to have an overview of the evolution of COVID-19 in US and NC we created a timeline chart of the Positive Cases over time, our analysis started in January 2020 and ended in March 2021. It is possible to identify the same evolution for NC and US, because the curves have the same shape, although NC showed fewer cases per capita than the national ratio.

### Tests per capita
#### Code for charts can be found in "MS_Timeline1a_1b.ipynb"
* Comparing the performed tests per capita we can identify that NC performed fewer tests than the US, and this difference was increased over time, which can be confirmed by the increasing angle between the curves as time passes by.

### Hospitalizations and Deaths per capita
#### Code for charts can be found in "GoughE_NCvUS_TimelineTrends.ipynb".
* After creating per capita variables for the increase in COVID-19 hospitalizations and COVID-19 related deaths, we were able to find that North Carolina performed slightly better than the nation as a whole. NC was not subject to the two peaks in hospitalizations that occurred in the US in May 2020 and July 2020, but roughly mirrored the US's pattern after that, while mostly remaining below the US's hospitalization rates.
* A first attempt at graphing the increase in COVID-19 related deaths created unreadable data due to the variability. As a result, data was grouped by the sum of deaths per month. The US and NC's COVID-19 related death pattern over time is very similar to the hospitalization rate. A very notable difference is that for September and October 2022, NC had more deaths per capita than the US.

## Is there a correlation between positive COVID tests and hospitalizations?
#### Code for charts can be found in "...".
* KM analysis

## Is there a correlation between the number of tests administered and deaths?
#### Code for charts can be found in "...".
* JA analysis

## Is there a correlation between positive COVID test and temperature?
#### Code for charts can be found in "corr_poscases_temp.ipynb"
* 

## What was the ratio of viral tests to antigen tests in North Carolina, and did the 9/30/20 introduction of antigen tests impact the state’s overall negative testing rate?
#### Code for charts can be found in "Austin-Group-Project-Code.ipynb".
* After comparing North Carolina's COVID-19 data to the nation as a whole, we decided to focus on the number of viral and antigen tests administered in the state from the beginning of the pandemic to spring 2021. Viral tests are the traditional molecular tests that became the early standard for testing nationwide, while antigen tests are the rapid, at-home version that arrived later in the year 2020. Our initial pie chart was created by comparing the total number of viral and antigen tests administered in the time period, which showed that over 92% of tests were in the "viral" category.
* A closer look at the data revealed that antigen testing arrived in North Carolina on September 30, 2020, which gave us the opportunity to do a before-and-after comparison of testing rates around the introduction of a new test type. Based on prior knowledge, we know that rapid at-home tests tend to be less reliable than the original viral tests and that they have a tendency to produce false negative results at a higher rate. With this in mind, we thought it would be interesting to compare the negative daily COVID-19 testing rate in the time periods before and after September 30, 2020.
* Because there was no column for the negative testing rate, we started by calculating this number for each date via the total number of tests and the increase in positive results. Once we calculated the negative testing rate throughout the time period, we dropped any days where zero tests were administered and changed all NaN values to zeroes. After plotting a simple line graph for the entire period and marking the last date prior to antigen testing with a red line, we thought it would be useful to create two separate scatter plots for the before-and-after comparison complete with lines of regression.
* In order to successfully plot lines of regression, we researched how to convert dates to date ordinal numbers and plotted the dates on the x axis in this manner. In the end, the "before" plot showed a slightly positive regression in the negative COVID-19 rate leading up to the introduction of antigen testing in North Carolina, and a slightly negative correlation following the introduction of antigen testing.
* These results actually go against the theory that the increased propensity for antigen tests to produce false negatives would lead to a higher overall negative COVID-19 testing rate in the state. However, a closer look at the graphs shows there were other major factors at play, namely the holiday season of 2020 when positive cases spiked due to large group gatherings. Furthermore, as seen in a previous graph, overall access to testing was increasing at a swift rate and likely had an impact on the positive/negative rates.

## How do mortality rates in North Carolina compare between different racial/ethnic groups? Is there a correlation between the total of cases to deaths?
#### Code for charts can be found in "...".
* JL analysis

## Data Limitations
* The US Census didn't have consistent month by month estimates for the date ranges we were looking for, and as a result, the same population number was used for all 2020 data, and all 2021 data. With more robust population data, the analysis would be more accurate.
* The biggest limitation when examining North Carolina's viral vs. antigen testing data was the lack of a test type designation for each positive test. Because we were unable to see specific negative testing rates per test type, we were forced to speculate on the impact of the introduction of antigen testing by using the overall negative testing rate for the state. If we had access to more detailed data for each test type, it would be much easier to evaluate the true impact of antigen testing.
* MdS analysis on OpenWeatherAPI

## Conclusions
* Looking at contextualized per capita data over time NC COVID-19 numbers were slightly better than the US as a whole, excluding a couple of months where our numbers were worse.
* MdS conclusions
* KM conclusions
* JA conclusions
* The percentage of negative tests in North Carolina actually decreased following the introduction of antigen testing, but it is likely that the spike in positive cases around the 2020 holiday season and increased access to testing played major roles in this shift.
* JL conclusions

### Group Members
* Everette Gough
* Austin McConnell
* Keisha Maldonado
* Joanna Lewis
* Michele di Sanctis
* Joseph Anthony

### Additional Help Provided by:
* Teaching Assistants
  * Antonio Laverghetta Jr.
  * Arda Sertel
* AskBCS
* StackOverflow
