# The Fight Against Crime in LA

### Project Overview
## A technical report on crime data in the city of Los Angeles 
Los Angeles, one of the biggest and most prominent cities in the world. With a population nearing almost 4 million people, the city of Los Angeles has gone from a popular city in the United States to a renowned city across the world, known for its huge variety in diversity and culture, being a hot spot for everything entertainment in the world, and with its always perfect weather. Though the city of LA has many benefits and good things to talk about, it also has about as many problems as well. A huge issue in LA is the crime rate. With a city so large, the crime is also large. The Los Angeles government and its police force have been in a constant war against crime, and ever since the COVID pandemic, the war has only worsened. The city of Los Angeles and its police force has investigated many practical solutions on how to manage crime in the city, with most having varied results. Now, with data analysis and predictive analytics being such a huge industry, the LA government has decided to attempt to use data driven problem solving and solutions to attempt to combat the crime in the city of Los Angeles.


## Business Questions

1. What crimes are being committed most?

2. When do crimes occur?

3. Where do crimes occur?

4. Who are crimes being committed against?

## Data sources

Crime data: "Crime Data from 2020 to Present" taken from data.gov

### Tools used

- SAS - ETL, Data Analysis
- Tableau - Data Analysis, Data Reporting


SAS code used:
```
data crimeD;
set work.import;
run;

proc contents data=crimed;
run;

proc means data=crimed; 
run;

proc freq data=crimed order=freq;
TITLE "Victim frequency info";
tables
'vict age'n 'vict sex'n 'vict descent'n  ;
run;

proc freq data=crimed order=freq;
tables
'premis desc'n 'weapon desc'n ;
run;

proc univariate data=crimed;
histogram;
var 'Vict age'n;
run;

```


### Forecasting



### Results/Findings



## Recommendations

The recommendations that we are giving, based on the analysis, are that the police force should up their workforce and patrol the designated areas more; Central, 77th Street, and Pacific. The Police force should be conscious of peak times like 12:00 PM, 6:00 PM, and anywhere in between that. Using these methods, or even being conscious of the analysis and forecasts should help the city in the battle against crime in the coming years. 


