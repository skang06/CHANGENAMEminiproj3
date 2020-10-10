# Factors Affecting Number of Impressions on Snapchat Political Ads in the United States for the 18-40 Age Range
## Background
Recently, Snapchat has been "actively going after" political ads, according to Jeremi Gorman, Snap's chief business officer, in an Earnings call in July 2020. According to the [article](https://mashable.com/article/snapchat-political-ads-q2-2020-earnings/), Snapchat's predilection for political ads goes against peer social media companies, like Twitter. It would be interesting to see how effective they may be with voters, especially with an upcoming election. 

18-40 year olds are currently eligible to vote, in terms of age, and will also remain voters for the next couple years. Looking into them will prove useful. Psychologically, starting the ad on a weekend might affect number of impressions, given that people will be on their phones more perhaps. How much is spent and how long the ad is live for may increase the number of impressions as they may be more high quality and available for longer.

A look into data from [Snap Political Ads Library](https://www.snap.com/en-US/political-ads/) will help us understand the reach and scope of Snapchat ads.

## Business Question
___How to determine engagement for political ads on Snapchat for the 18-40 age range in the United States?___

## Open Data 
__Snap Political and Advocacy Ads Library:__ this library contains all the political and advocacy ads that Snap runs on their platform. A full data dictionary of column variables can be found [here.](https://github.com/skang06/snapchat_political_ads_2020/blob/master/readme.txt)
- [Snapchat Political Ads 2020](https://github.com/skang06/snapchat_political_ads_2020/blob/master/PoliticalAds.csv): Dataset containing original data source. This data was [cleaned](https://github.com/skang06/snapchat_political_ads_2020/blob/master/Snapchat_data_cleaned.xls) to contain only those in the 18-40 age range in the United States.

## Data Analysis 

1.__How does the number of days the ad was live affect the number of impressions?__
![alt text](https://github.com/skang06/snapchat_political_ads_2020/blob/master/days_used.png)

The simple linear regression line only accounts for approximately 3% (R squared value of .03) of the data, so a multiple linear regression was modelled.

2. __Can you predict the number of impressions for an advertisement based on whether it starts on the weekend, amount spent on the ad, and days it was used?__

A multiple linear regression found that starting on a weekend was insignificant because it had a p-value of .74 (which is greater than .05). Thus, there is reason to believe that the null hypothesis (that there is no relationship between starting on a weekend and number of impressions) is true. 

_Another multiple linear regression was taken with amount spent and the days used (since weekend start was insignificant)._ 

![alt text](https://github.com/skang06/snapchat_political_ads_2020/blob/master/stats.png)

__Number of impressions = -331958 + 294 * amount spent + 8455 * days used.__

The p-values for spending and days used are both less than .05, so amount spent and days live are both statistically significant variables that affect the number of impressions. Additionally, a low F-significance level indicates that the probability that these two variables do not matter at all in determining number of impressions is basically 0. There is a standard error (which indicates how the data is distributed around the multiple regression line) of 1,724,551 impressions, which seems rather large since the average number of impressions on an ad was 836,175 impressions.

The R Square value of .788 means 78.8% of the number of impressions could be attributed to the multiple linear regression line with spending and the days live as the two independent variables. The high R Square value shows that the number of impressions can be predicted pretty well by this model. The coefficient in front of amount spent signifies that a one dollar increase in amount spent will increase the number of impressions by 294, holding amount of days used constant. The coefficient in front of days used signifies a one day increase in days used increases the number of impressions by 8455, holding amount spent constant. The days used is more significant in increasing the number of impressions, relative to price. 

## Summary
The analysis can help political organizations more confidently predict how much to spend on an ad and how many days to use an ad to increase the number of impressions on 18-40 year olds, and thus its effectiveness on them. This confidence may lead more organizations to utilize Snapchat in posting ads, generating revenue for the company. Moreover, this analysis is particularly important and of use now. Given how close we are to election day, it could help organizations predict whether or not it is worth it to release ads now and whether they should possibly spend more, given the time constraint. The analysis shows that, for the future, there is a benefit to political organizations in rolling out these ads early. 
Finally, looking into other variables that could lower the standard error would help political organizations increase engagement with their election ads.
