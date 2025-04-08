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

## Tools used

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


## Forecasting

### - Forecast model on the predicted crime trend in LA
  
The data forecast/model, as seen below, indicates crime is not going anywhere unless there is something done. The forecast is telling us that the crime trend looking to at least maintain the volume it is at now. This gives us a basis to look for actionable insights.

![image](https://github.com/user-attachments/assets/af605ad2-f3e0-4144-895f-48e1fb33c22b)


## Results/Findings (Answering the previous buisness questions)

### - What crimes are being committed most?

Crimes committed per month
![image](https://github.com/user-attachments/assets/89c7adef-756b-4eaf-8990-f718b3e09652)

Stolen vehicles are the number 1 crime being committed in LA, and by quite a margin. Following that is battery (making intentional and offensive physical contact with another person without their consent), identity theft, 2 types of burglary,


### - When do crimes occur?

Time of day crimes are committed (Military time)
![image](https://github.com/user-attachments/assets/a430d890-0ccb-494d-8630-51417cc15bbc)

We can see that the data reported gives a trend to reporting crimes at the top of the hour, so that is why you see so many ups and downs so the biggest takeaway you want to see here is the trend, and how the peaks are viewed. The graph tells us that crimes are mostly committed around 12:00 PM, in the middle of the day. It seems to drop off a bit and pick up later into the night where crime drops to the lowest in the early hours of the morning.


### - Where do crimes occur?

Where crimes are being committed.

![image](https://github.com/user-attachments/assets/df40884c-20be-4451-8a28-5f1b2845f3ad)

With the LA crime data “area” as our location indicator, the Central area is seeing the most crime per month, with 77th street and Pacific following. 

For info on the “area” identifier, it comes from the LAPD definition of how they send out police patrols, defined as “The 21 Geographic Areas or Patrol Divisions that are also given a name designation that references a landmark or the surrounding community that it is responsible for” (Los Angeles Police Department, 2024).


### - Who are crimes being committed against?

Victim Age
![image](https://github.com/user-attachments/assets/6c90bbc7-7e60-45b6-b29c-5e0eca06a15a)

Victim Sex

![image](https://github.com/user-attachments/assets/67490c46-3126-43a9-b099-a1af51f9be54)

Victim Sex and Descent
![image](https://github.com/user-attachments/assets/f89d3b1d-adb6-4657-853b-febc724e2a69)

The ages between 25 and 35 see most victims, and that is a valuable insight going forward. We can also see there is a high number of Latin/Hispanic Victims followed by White and Black ethnicity, this is predictable as it follows the ethnicity population in LA. As for the Victim Sex, 47% male, 42% female, and the rest unknown. The gender and descent findings are not as valuable as the others and can be seen as the most predictable of the lot. 


## Recommendations

The recommendations are, based on the analysis/forecasting models, are that the police force should up their workforce and patrol the designated areas more; Central, 77th Street, and Pacific. The Police force should be conscious of peak times like 12:00 PM, 6:00 PM, and anywhere in between that. Using these methods, or even being conscious of the analysis and forecasts should help the city in the battle against crime in the coming years. 


