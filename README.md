# Exploring the Medicare Shared Savings Program

## Background

Economists and policymakers have long debated the optimal method to pay for the delivery of healthcare. Ever since Medicare ceased to reimburse providers for their reported costs and instead decided to set prospective rates for health services, a key question in this debate has been the correct unit of analysis. For several decades the dominant models were Fee For Service (FFS), where providers are paid a fixed fee for every service provided and thus face incentives to provide as many services as possible, and Diagnosis Related Groups (DRGs), where providers are paid a fixed sum for all of the care a patient receives for a given condition and thus face incentives to code more and more severe diagnoses but potentially under provide care within each episode to increase their profit margins. However, some researchers have long believed that it would be best to reimburse providers for people rather than services and thus incentivize them to focus on value across every margin. As part of the Affordable Care Act, the Medicare program was authorized to create a program experimenting with these “capitation” models. Providers who wanted to participate in the Medicare Shared Savings Program (MSSP) would form a larger entity, known as an Accountable Care Organization (ACO), and agree to take a fixed lump sum payment (known in the program as the benchmark) for an entire population of Medicare Beneficiaries. Though the program has grown substantially since its initiation in 2013, many questions remain about the structure and consequence of these organizations. 

## Web Application 

This repository contains code to create the MSSP Exploration shiny web application found [here](https://andres-deloera.shinyapps.io/ACO_Exploration/). This web application was created by Andres de Loera-Brust in the spring of 2019 to explore the publically available data on ACOs in the MSSP. It looks at data at two levels of observation: the ACO level and the county level. Several reactive plots allow the user to explore how organizational variables relate to each other for organizations in the MSSP. Other, also reactive, plots and maps allow the user to explore the distribution of ACO beneficiaries and how ACO prominence relates to other county level Medicare characteristics. 

## Insights

Since there are so many choices for what to explore it may be difficult to identify the most interesting insights. Below are just a few relationships revealed in the app that may be of interest to anyone curious about ACOs and the MSSP:  
* The savings/losses generated by ACOs in the program become more variable as time goes on (Note that these aren’t necessarily the “true” savings of the program because they are defined relative to the ACOs benchmark rather than the counterfactual where the providers don’t participate in the program.)
* Longer operating ACOs have higher quality scores, shared savings rates, and generate and earn more savings. However, it is unclear if performance increases over time or if the worse performing ACOs exit. 
* Larger ACOs have lower per capita benchmark and lower per capita expenditures, which may suggest benefits of scale. 
* There appears to be little relationship between number of ACO beneficiaries in a country and the ACO participation rate in that county. 
* ACO participation rate seems to have little relationship with average cost per beneficiary (though perhaps ACOs are simply more appealing in high cost areas and they help lessen variation). 
* Entering ACOs all get low quality scores but exiting ones do not. 
* Entering and exiting ACOs have smaller beneficiary populations than continuing. 

## Data Sources

* Detailed ACO-level data comes from Shared Savings Program Accountable Care Organizations (ACO) Public-Use Files, made available by CMS [here](https://www.cms.gov/Research-Statistics-Data-and-Systems/Downloadable-Public-Use-Files/SSPACO/index.html). 
* County-level ACO beneficiary data comes from the Number of ACO Assigned Beneficiaries by County Public-Use Files, available in as part of the Shared Savings Program Benchmark Rebasing PUFs found [here](https://www.cms.gov/Research-Statistics-Data-and-Systems/Downloadable-Public-Use-Files/SSPACO/SSP_Benchmark_Rebasing.html). 
* County-level Medicare data comes from the State/County Table on All Beneficiaries in the Medicare Geographic Variation Public Use Files found [here](https://www.cms.gov/Research-Statistics-Data-and-Systems/Statistics-Trends-and-Reports/Medicare-Geographic-Variation/GV_PUF.html).
* The US county map shapefile comes from the Census Bureau’s Cartographic Boundary Files, available [here](https://www.census.gov/geographies/mapping-files/time-series/geo/carto-boundary-file.2016.html).

