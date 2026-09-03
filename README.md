# COVID-19 Global Data Tracker

A comparative data analysis of COVID-19 case growth, mortality, and vaccination trends across **Kenya, India, the United States, and China**, built with Python and Pandas.

##  Overview

Raw COVID-19 statistics are easy to find but hard to compare meaningfully — a country with more total cases isn't necessarily "worse off" once you account for population size, testing capacity, and reporting standards. This project goes beyond headline numbers to look at how the pandemic's *shape* differed across four countries with very different populations, healthcare systems, and government responses.

**Question this project answers:** How did the trajectory of COVID-19 — cases, deaths, and vaccination — actually differ across countries with very different contexts, and what patterns emerge when you look at the full timeline rather than a single snapshot?

##  Tools & Libraries

- Python
- Pandas
- Matplotlib
- Seaborn
- Plotly Express

##  Dataset

[Our World in Data COVID-19 dataset](https://ourworldindata.org/covid-deaths) (`owid-covid-data.csv`) — 429,435 rows across 67 columns covering cases, deaths, testing, vaccinations, and demographic/health indicators for every country from January 2020 through August 2024.

##  Data Preparation

- Converted the `date` column from string to `datetime` for time-series plotting
- Filtered the dataset down to four countries: Kenya, India, United States, China
- Dropped rows with missing `total_cases`
- Filled remaining missing values with 0

After cleaning: **6,696 rows**, no missing values, across all 67 original columns.

##  Analysis & Visualizations

- **Total Case Growth Over Time** — line chart comparing cumulative cases per country
- **Death Rate Over Time** — `total_deaths / total_cases`, plotted to reveal how case lethality shifted across pandemic waves
- **Vaccination Rollout** — cumulative vaccinations per country over time
- **Global Case Map** — choropleth map (Plotly) showing total cases by country at the most recent date in the dataset

##  Key Insights

- **United States** — highest total case counts of the four countries, fastest early vaccine rollout
- **India** — major case surges, most notably during the mid-2021 wave
- **Kenya** — fewer total cases overall, but a relatively higher death rate during peak periods
- **China** — consistently low, near-flat case curve for most of the timeline
- **Vaccination pace** — fastest in China and the U.S., with Kenya lagging behind both

##  Takeaways

Raw case counts alone can be misleading — a country's testing capacity, reporting infrastructure, and population size all shape the numbers you see. Looking at *rates* (like death rate) and *trends over time*, rather than single totals, gives a more honest picture of how the pandemic actually affected each country.

**Possible next steps:**
- Normalize all metrics per capita (cases/deaths/vaccinations per million) for a fairer cross-country comparison
- Incorporate the `stringency_index` column to correlate policy strictness with case trajectories
- Extend the country list to a full regional comparison

##  Author

**Brian Muema**
Data Analyst / Data Scientist
📧 brianmuema928@gmail.com
