# Prediction of energy consumption of daily energy demand and market price in Spain

Data Science project of daily energy price and demand in Spain. The implementation can be found here: https://github.com/ca-schumacher/pred_Energy/blob/master/data_analysis.ipynb

**July 2019**

## Introduction

**Project Description:**

We will use this dataset to analyse and predict the energy demand in Spain. Further we will look at the development of the daily market price. While this might sound easy, it is actually a quite hard task since the whole country undergoes a variety of seasonal (repetitive) and non-seasonal (discrete) flucutations, caused e.g. by weather seasons, by political events / decisions or societal influences.

**Data Description:**

This notebook deals with the analysis of a daily time series of electricity demand, generation and prices in Spain from 2014 to 2018. The data (including its documentation) is accessible through kaggle: https://www.kaggle.com/manualrg/spanish-electricity-market-demand-gen-price

## Approach

After cleaning the dataset, I will visualize the daily energy demand for different days of the week, weeks of the year to gain knowledge about the different trends of energy demand.
For this timeseries analysis I will use facebook's Prophet toolbox that is particulary interesting for timeseries with fluctations on different time-levels (seasonal, mothly, weekly etc.). 
I will apply this technique to predict the daily energy demand and the market price for a period of one year ahead.

## Modelling

Open the Notebook (https://github.com/ca-schumacher/pred_Energy/blob/master/data_analysis.ipynb) to see the data analysis, modeling and predicted results.

## Results and Conlcusions

The following trends of the energy demand were found:
- the demand seems to be strongly influenced by the days of the week (drops on weekends)
- during summer and winter, a higher energy demand was found, probably due to increased usage of air conditioning and heating during these periods
- over the years 2014 to 2018, no substantial changes in energy demand were found

In comparison, other trends were observed for the price development:
- prices remained quite similar during different days of the week and weeks of the year
- the main change of the market price was on a yearly timescale

The prophet model did well to predict the energy demand (Mean Absolute Percentage Error: 4.6) that is influenced by weather (temperature, wind speed, precipitation, etc.) and the intensity of business and everyday activities (on-peak vs. off-peak hours, weekdays vs. weekends, holidays, etc.). However, this model did not work for the energy price (MAPE: 27.9). This could due to the fact that the energy price is influenced by economic mechanisms and fluctations also, e.g. stock market developments etc.




---


### Translation of column names

**Demanda programada PBF total (MWh):** Schedulled Total Demand

**Demanda real (MW):** Actual demanded power

**Energía asignada en Mercado SPOT Diario España (MWh):** Energy traded in daily spot Spanish market (OMIE)

**Energía asignada en Mercado SPOT Diario Francia (MWh):** Energy traded in daily spot French market

**Generación programada PBF Carbón (MWh):** Schedulled Coal electricity generation

**Generación programada PBF Ciclo combinado (MWh):** Schedulled Combined Cycle electricity generation

**Generación programada PBF Eólica: (MWh):** Schedulled Wind electricity generation

**Generación programada PBF Gas Natural Cogeneración (MWh):** Schedulled Natural Gas electricity Co-generation

**Generación programada PBF Nuclear (MWh):** Schedulled Nuclear electricity generation

**Generación programada PBF Solar fotovoltaica (MWh):** Schedulled Photovoltaic electricity generation

**Generación programada PBF Turbinación bombeo (MWh):** Schedulled Reversible-Hydro electricity generation

**Generación programada PBF UGH + no UGH (MWh):** Schedulled Total Hydro electricity generation

**Generación programada PBF total (MWh):** Schedulled Total electricity generation

**Precio mercado SPOT Diario ESP (€/MWh):** Daily spot Spain market price

**Precio mercado SPOT Diario FRA (€/MWh):** Daily spot France market price 

**Precio mercado SPOT Diario POR (€/MWh):** Daily spot Portugal market price

**Rentas de congestión mecanismos implícitos diario Francia exportación (€/MWh):** Daily spot export from France price

**Rentas de congestión mecanismos implícitos diario Francia importación (€/MWh):** Daily spot import to France price

**Rentas de congestión mecanismos implícitos diario Portugal exportación (€/MWh):** Daily spot export from Portugal price

**Rentas de congestión mecanismos implícitos diario Portugal importación (€/MWh):** Daily spot import to Portugal price
