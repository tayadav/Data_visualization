# Data Visualization Group Project
This is the summary of the group project delivered by Study Group 1 for the Data Visualisation Module.

## Background
Due to incredibly large distances in the US, many more of the routes are covered by airplane compared to train in Europe, for example. Naturally travelling across the country can quickly become quite expensive, unless you are one of the "travel hackers".  

With many LBS students travelling to the US for their GIFTs, and potentially wanting to travel around before/after the GIFTs, we thought it would be interesting to analyze travel hacks to suggest options for low-cost air travel. Some members of our group recently received monetary compensation for delayed flights, thus we asked ourselves whether it is possible to deliberately identify flight delays, receive monetary compensation and consequently travel with a low budget.

## Dataset selection
We decided to focus our efforts on air travel starting in New York City. With 3 large airports spread around the city, the world's financial center is well connected across the US with 16 million passengers solely going through JFK airport.  (<https://www.statista.com/statistics/962767/passenger-traffic-new-york-john-f-kennedy-type/>).  
Therefore, we decide to analyse airport activity in JFK, LaGuardia and Newark Airport in New York in 2013 for inland flights across the US. These 3 airports on the Eastern coast are perfect for LBS students coming from London to use as an interchange point for flights to either Austin or San Francisco. This data was the most recent data available for United States travel and delays. While it may not be representative of a post-Covid era, it should be sufficient to recognize common patterns of when flights are more likely to be delayed.

Dataset: <https://www.kaggle.com/sveneschlbeck/new-york-city-airport-activity> 

## Cleaning 
The first step of this project was ensuring consistency among the data. Furthermore, categorical variables were added (e.g. daytime, season, time caught up, etc.) to better assess the difference in delays between flights, but also to improve visualization opportunities through converting airport codes into actual city names including coordinates.  

## Statistical Significance
Before any analysis could be conducted, we had to assess whether there is actually a statistically significant difference between different flight delay times according to their parameters. Naturally, we only focused on variables that can be influenced by travelers, as the goal is helping travelers like us to find delayed flights. 
For example, are flights during the evening more delayed than during the morning, or are any of the three airports in NYC specifically dominant when it comes to delays?  

Several hypothesis tests and confidence intervals were conducted with the final insight that arrival delays can actually be explained by several variables from the dataset. 
Such variables are:

- Season of the year
- Time of day
- Airlines
- Airport
- Destination

## Analysis
Once we confirmed the statistically significant difference among variables with respect to flight delay, we started thinking about an approach for choosing the optimal flights. Similar to the overall approach of our project, we decided to go with a sequential Top-Down approach. This implies that we started with broad parameters and further narrowed it down, while incorporating previous decisions on parameters in selecting the next value.   

As an example, we started by identifying the season and daytime with the largest average arrival delays, which occur on Summer Evenings. The next step was identifying the airport with the largest average delay, but instead of general delays per airport, we only assessed the average delay per airport during Summer Evening.   

This process runs through our entire analysis which each decision depending on the previous selection of parameters.  

## Conclusion and Recommendation
The end result is a recommendation of one flight for short-, mid-, and long-term distance where travellers are likely to experience large delays, and thus a cash reimbursement.  

All flights are going from **Newark Airport** during **Summer Evening (6pm - 12pm)**.

Short-distance flight: **Columbus, OH (ExpressJet)**

Mid-distance flight: **Minneapolis, MN (ExpressJet)**

Long-distance flight: **San Francisco, CA (Virgin America)**
