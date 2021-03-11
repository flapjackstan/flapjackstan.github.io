---
layout: project
title: Twitter Sentiment Analysis
summary: Time Series, GAM, R 
category: Time Series, GAM, R
---

#### **Background**
This data was originally posted by Crowdflower in 2016 and includes tweets about 6 major US airlines. Additionally, Crowdflower had their workers extract the sentiment from the tweet as well as what the passenger was dissapointed about if the tweet was negative.

##### Summary

**The airline industry was found to have distinct "prime" tweet hours between 8am and 6pm where passengers were more likely to share opinions about their flights and interactions with airlines.** Using this temporal tweet history, we are able to forecast the hour that each airlines will receive tweet mentions, and more interestingly, analyze the hour of negative and positive interactions with tweeters that can serve as proxy to customer service quality.  

<div align="center">
<iframe
    width="600"
    height="400"
    src="../files/delta.html"
    src="https://flapjackstan.github.io/files/delta.html"
    frameborder="1px"
    allowfullscreen
></iframe>
</div>



<br/><img src='/images/delta_table.png'>
    


<br/><img src='/images/delta_trends.png'>

##### Reccomendations
Consider the validity of using tweets as a basis to drive decision making. If there is viable evidence showing that tweets are representative of real world customer satisfaction the best action would be to take a look at staffing during these hours and commit to fixing some of the issues that were present in the data such as baggage loss and delayed flights.

##### Analyst Notes
The forecasts were generated with a generalized additive model using hourly aggregated sentiment classified tweet data. Validity of the model is expressed in the MAPE graph below that does an excellent job in showing the error in our moedel when it encountered the spike of tweets around February 22nd. Seasonality was also present in our data signaling further tuning is possible to account for this. 

<br/><img src='/images/mape.png'>
