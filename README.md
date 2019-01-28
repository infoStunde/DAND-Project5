# Data Exploration of Ford Go Bike System for 2018 

## SETUP
1. Create folder in the project: /data/bike/

2. Download in that bike folder the .zip data from https://stackoverflow.com/questions/20906474/import-multiple-csv-files-into-pandas-and-concatenate-into-one-dataframe

3.  Set in DownloadAndCleanData.ipynb the var to tTrue

> doExtract = True
> readInFileByFile = True

4. Run the DownloadAndCleanData.ipynb

5. Run exploration.ipynb

6. Run slide_deck.ipynb


## Dataset

The data consists of 1740396, including
19 anonymized features

Trip Duration (seconds)
Start Time and Date
Start Station ID
Start Station Name
Start Station Latitude
Start Station Longitude
End Time and Date
End Station ID
End Station Name
End Station Latitude
End Station Longitude
Bike ID
User Type (Subscriber or Customer – “Subscriber” = Member or “Customer” = Casual)
Member Year of Birth
Member Gender
Derived features

User Age
Start Daytime
End Daytime
Start Month


Most variables are nominal in nature, but the variables duration and age are numeric variables. The ordinal variable user_type, start_month are ordered with the following levels:

User Type: Customer -> Subscriber

Start/End Daytime: 'morning' ->'afternoon' -> 'evening' -> 'night'

Start Month: 1 -> ... -> 12

## Summary of Findings

In the exploration, I found that there was a relationship between age and duration. 
The distribution for age and duration is strongly right skewed. 
The distribution of the categorical vars shows that the common user is a male subscriber without sharing the bike for all trip.
With an average age of 33 the usual custumer is a subscriber.
In the distribution of duration of rides the most rides are taking less then 64 min. 



## Key Insights for Presentation

For the presentation, I focus on the duration of rides  
and leave out most of the derivations. I start by introducing the
distribution of duration (using a histogram) zooming in to the difference by user type (using a violin plot), followed by the distribution of locations.

Afterwards, I introduce a FacetedPlot ploting duration vs month in 2018. 
Inside I use pointplot to point out the average development of the duration during separeted by location.
