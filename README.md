# Factors and Impacts of Greenhouse Gas Emissions


## Summary

This repository was created for the course project of ENV 872L Environmental Data Analytics course at Duke Nicholas School of the Environment in Spring 2020. 

Global warming resulted from greenhouse gas (GHG) emissions is one of the biggest challenges to human beings. While IPCC in its latest special report warns people the critial consequences of 1.5-degree-Celcius temperature increase from the pre-industrial level, the average global temperature on Earth has already increased by about 0.8° Celsius (1.4° Fahrenheit) since 1880. 

In the United States, in the period of 1990-2017, the temperature increase and GHG emissions have been greatly contribetd by the energy sector. This was attributed to the increase electricity consumptions in all sectors by more people, and electricity generation primarily relies on fossil-fuel combustions. In addition to temperature increase, the economic features also have significant changes along the increasing GHG emissions and electricity consumption in the meantime. Understanding environmental and socioeconomic impacts of GHG emissions is significant to policy makers to consider long-term decision making. Therefore, this project examines the impacts of energy consumptions and demographic changes on GHG emissions, as well as further investigates the environmental and economic effects of GHG emissions in the United States from 1990 to 2017. 

Specifically, this project aims to study factors that might contribute to GHG emissions guided by the following questions:

1. How did the GHG emission trend vary with the US electricity consumption changes from 1990 to 2017? Which sector was the biggest contributor to GHG emissions in these 18 years?
2. Was the population growth a signifant factor in the energy consumption development and then affecting GHG emissisions in this period?

Following up with GHG emission causes, this project will then explore the impacts of GHG emissions in US from 1990 to 2017 guided by the following questions: 

3. Which greenhouse gas was most responsible for temperature anomalies in this period?
4. Was the economic development in this period, namely gross domestic product (GDP) and personal consumption expenditures, significantly realted to the GHG emissions? 

This repository contains raw data, proecessed data, codes, outputs, and a report involved this project.

## Investigator

Vicky Jia

Nicholas School of the Environment, Duke University, Durham, NC 27705

fanqi.jia@duke.edu

## Keywords

GHG, emissions, energy consumption, popolation growth, temperature anomaly, economic development, US

## Database Information

###BEA_GDP_raw.csv:
US annual gross domestic production and personal consumption expenditures data from 1990-2017.Data were retrieved from US Bureau of Economic Analysis National Income and Product Accounts (NIPA) Interactive Data Tables tool. Data were transposed by the investigator.
(https://apps.bea.gov/iTable/iTable.cfm?reqid=19&step=2#reqid=19&step=2&isuri=1&1921=survey accessed on 2020-04-11.)

The following selections were made: 
*First Year: 1990-A&Q
*Last Year: 2017-A&Q
*Scale: billion
*Series: Annual


EIA_electricity-consumption_sector_raw.csv:
The annual retail sales of electricity to ultimate customers by sector, by state, by provider from 1990 to 2018 in US. The data was retrieved from Annual Electric Power Industry Report, Form EIA-861 detailed data files from US Energy Information Administration.

(https://www.eia.gov/electricity/data/state/sales_annual.xlsx accessed on 2020-04-11.)


EPA_GHG_Gas_raw.csv
US GHG emission data by gas types in all sectors from 1990-2017 provided by EPA's annual Inventory of U.S. Greenhouse Gas Emissions and Sinks. Data was retrieved from US EPA Greenhouse Gas Inventory Data Explorer. Data were transposed by the investigator.
(https://cfpub.epa.gov/ghgdata/inventoryexplorer/#allsectors/allgas/gas/all accessed on 2020-04-11.)
The following selections were made: 
*Sector: All sectors
*Greenhouse gas: All gases
*Break out by: Gas
*Year: All years

EPA_GHG_Sector_raw.csv:
GHG emission data by economic sectors for all greenhouse gases from 1990-2017 provided by EPA's annual Inventory of U.S. Greenhouse Gas Emissions and Sinks. Data was retrieved from US EPA Greenhouse Gas Inventory Data Explorer. Data were transposed by the investigator.
(https://cfpub.epa.gov/ghgdata/inventoryexplorer/#allsectors/allgas/econsect/all accessed on 2020-04-11.)
The following selections were made: 
*Sector: All sectors
*Greenhouse gas: All gases
*Break out by: Economic sector
*Year: All years

NOAA_temp_raw.csv:
US mean annual temperature and temperature anomalies from 1990 to 2017. Data was retrieved from NOAA National Centers for Environmental Information Climate at a Glance.
(https://www.ncdc.noaa.gov/cag/national/time-series/110/tavg/ann/12/1990-2017?base_prd=true&begbaseyear=1901&endbaseyear=2000, accessed on 2020-04-11.)
The following selections were made:
*Parameter: Average Temperature
*Time Scale: Annual
*Start Year: 1990
*End Year: 2017
*Display Base Period: Start: 1990, End: 2017

WB_pop_raw.csv:
Total annual population data from 1960-2018 retrieved from World Bank dataset. Data were transposed by the investigator.
(https://data.worldbank.org/indicator/SP.POP.TOTL?locations=US accessed on 2020-04-11.)
The following selections were made in the searching window:
*Population, total
*United States


## Folder structure, file formats, and naming conventions 

Raw Data - all raw data in csv files collected from the datasets above
Processed Data - processed data in csv files via wrangling, data exploration, and data analysis
Code - R markdown files for each step of analysis
Output - output figures from analyses

Files are named according to the following naming convention: `databasename_datatype_details_stage.format`, where: 

**databasename** refers to the database from where the data originated

**datatype** is a description of data 

**details** are additional descriptive details, particularly important for processed data 

**stage**refers to the stage in data management pipelines (e.g., raw, cleaned, or processed)

**format** is a non-proprietary file format (e.g., .csv, .txt)

## Metadata

BEA_GDP_raw.csv:
US annual gross domestic production and personal consumption expenditures data from 1990-2017. Values are in the units of "billions of dollars".
Column names without descriptors are self-explanatory.
Year: 1990-2017
1 Gross domestic product
2 Personal consumption expenditures
3 Goods
4 Durable goods
5 Nondurable goods
6 Services
7 Gross private domestic investment	    
8 Fixed investment	        
9 Nonresidential	            
10 Structures	            
11 Equipment	            
12 Intellectual property products	        
13 Residential	    
14 Change in private inventories	
15 Net exports of goods and services	    
16 Exports	        
17 Goods	        
18 Services	    
19 Imports	        
20 Goods	        
21 Services	
22 Government consumption expenditures and gross investment	    
23 Federal	        
24 National defense	        
25 Nondefense	    
26 State and local

EIA_electricity-consumption_sector_raw.csv:
The annual electricity consumptions from 1990 to 2018 in US by state, by  sector, and by provider. Sales to ulimate customers are used as eletricity consumptions in that sector.
Column names without descriptors are self-explanatory.
Year: 1990-2018
State: 50 states + District of Columbia + US total
Industry Sector Category:
"Energy-Only Providers": Only energy service without delivery
"Full-Service Providers": Energy and delivery services
"Total Electric Industry": Sum of both providers above
Residential: Megawatthours of electricity sold to the residential sector
Commercial: Megawatthours of electricity sold to the commercial sector
Industrial: Megawatthours of electricity sold to the industrial sector
Transportation: Megawatthours of electricity sold to the transportation sector
Other: Megawatthours of electricity sold to other sectors not fallen in above categories
Total: Sum of megawatthours of electricity above

EPA_GHG_Gas_raw.csv:
US GHG emission data by gas types in all sectors from 1990-2017 provided by EPA's annual Inventory of U.S. Greenhouse Gas Emissions and Sinks.
Column names without descriptors are self-explanatory.
Year: 1990-2017
Carbon dioxide: Concentration of CO2 in the unit of million metric tons of carbon dioxide equivalents
Methane: Concentration of CH4 in the unit of million metric tons of carbon dioxide equivalents
Nitrous oxide:Concentration of N2O in the unit of million metric tons of carbon dioxide equivalents
Fluorinated gases: Concentration of fluorinated gases in the unit of million metric tons of carbon dioxide equivalents
Total: sum of all gases above for that year

EPA_GHG_Sector_raw.csv:
US GHG emission data by economic sectors for all greenhouse gases from 1990-2017 provided by EPA's annual Inventory of U.S. Greenhouse Gas Emissions and Sinks.
Column names without descriptors are self-explanatory.
Year: 1990-2017
Transportation: GHG emissions in the unit of million metric tons of carbon dioxide equivalents in the transportation sector
Electricity generation: GHG emissions in the unit of million metric tons of carbon dioxide equivalents in the electricity sector
Industry: GHG emissions in the unit of million metric tons of carbon dioxide equivalents in the industrial sector
Agriculture: GHG emissions in the unit of million metric tons of carbon dioxide equivalents in the agriculture sector
Commercial: GHG emissions in the unit of million metric tons of carbon dioxide equivalents in the commercial sector
Residential: GHG emissions in the unit of million metric tons of carbon dioxide equivalents in the residential sector 
U.S. territories: GHG emissions in the unit of million metric tons of carbon dioxide equivalents in all U.S. territories
Total: sum of emissions from all sectors above for that year

NOAA_temp_raw.csv:
US mean annual temperature and temperature anomalies from 1990 to 2017.
Column names without descriptors are self-explanatory.
Date: YearMonth
Value: mean annual temperature in fahrenheit
Anomaly: Difference from mean (53.26F) in 1990-2017 base period

WB_pop_raw.csv:
Total annual population data from 1960-2018 retrieved from World Bank dataset.
Column names without descriptors are self-explanatory.
Year
Population by country

## Scripts and code

<list any software scripts/code contained in the repository and a description of their purpose.>
To be updated.

## Quality assurance/quality control

To ensure the quality of this project, this project was developed from a tree graph - starting with a topic of interest, which is GHG emissions here, and exploring its resposible factors, such as population and electricity consumption, and then proceeding to another direction to consider potential impacts of this topic, which refers to economic development and temperature changes - to make sure all variables involved in this project are related to the topic, and also to conduct a comprehensive and complete project about GHG emissions.
One essential rule to follow when collecting data among diverse sources of database is the temporal and geograhic scale of the dataset, that is all data must in the format of annual basis and cover the entire US. Monthly or daily and state-level data are also acceptable, but are at the lower priority than those data originally formatted as annual scale at the country level. 
To avoid errors and mistakenly using data, before conducting the data analysis, a boxplot is created for each dataset to detect outliers. If data for certain year or certain sector is missing, the entire year will be considered in all dataset to keep the consistency of the analysis.