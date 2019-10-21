# Introduction

Drinking alcohol excessively impairs a person’s judgement and increases the risks of aggressive behaviors. There are studies that suggest engaging in prolonged drinking significantly increases a person’s risk of committing violent offenses. Those studies have shown correlation between drinking alcohol and crime, but what about the impact of the availability of alcohol? Alcohol is available from small neighborhood shops like liquor store and convenient store to most dine-in restaurants and bars. Does the availability of alcohol play a role in neighborhood crimes? If a strong correlation between alcohol vendors and crime is suggested, the results can be used in city neighborhood planning and help city governments make smarter decisions. It can also help home shoppers and renters that want to avoid high crime areas to correctly access neighborhoods.


# Data

New York City is the most populous and the most densely populated city in the United States, and the New York City Police Department has publicly available crime statistics by borough and precinct. This project will utilize the crime data by precinct on the NYPD website, and the Police Precincts data set on the NYC OpenData website, as well as the FourSquare venue data (specifically the venues where alcohol is available). 

Firstly, the NYPD crime data by precincts contains seven major felony offenses statistics in each precinct from 2000 to 2018. This project will extract and only uses the 2018 data. The seven major felony offenses in the dataset are murder & non negligent manslaughter, rape, robbery, felony assault, burglary, grand larceny, grand larceny motor vehicle. Secondly, the Police Precincts data set is the location data of the New York City precincts. The locations of the precincts are in the GeoJson multi-polygon format, which will require simplification for this project during data transformation. Lastly, the FourSquare venue data is acquired through the FourSquare Places API. Whether a venue offers alcohol is inferred from the category and/or the name of the venue.

The precincts location data is needed to perform the Foursquare Places API venue search, in order to obtain the data of alcohol vendors in each precinct, which is further modeled in conjunction with the crime data to determine if there is a strong correlation between the availability of alcohol and crime.
