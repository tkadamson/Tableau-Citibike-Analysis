# Tableau-Citibike-Analysis

### Summary | GRADE: A+

For this project, I was given an open-ended assignment to visualize NYC Citibike Trends in Tableau. The data is publically available in the form of csv's for each month. I chose to analyze ridership by age and by sex, from January 2020 to present.

### Project Writeup
Visualizations for this project can be viewed in Tableau Public here: https://public.tableau.com/views/CitibikeAnalysis_16207656330520/FullCitibikeAnalysis?:language=en&:useGuest=true&:display_count=y&:origin=viz_share_link

The landing page is the storyboard presentation for all data. Also included are two dashboards: one on ridership based on sex (Metrics on Sex), and one on ridership based on age (Metrics on Age). Lastly, there is a sheet containing a map of all ridership over the defined time period (Station Map by total Ridership).

The analysis is divded into five sections:
* Overview
* Ridership by Starting Station
* Ridership by Sex
* Ridership by Age
* Data Constraints

#### Overview
Citibike is New York City's rideshare program sponsored by CitiBank. Riders have the option to either pay a monthly membership for unlimited rides or pay for each ride individually. For point of service purchases, there is a flat rate for the first 30 minutes and then a small per minute increate after the first thirty. Riders can end at any station they wish rather than returning the bike to its original location.

For the time period analyzed, January 2020 to April 2021, ridership clearly suffered a dramatic decline during the COVID-19 lockdown in New York City, dropping about 75% between March 11, 2020 and March 31, 2020. However, ridership mostly rebounded by summer, and then entered it's presumable decline over the winter months. 

In January 2021, there was a noticable increase in ridership which then dips agin in February. This may be due to an unseasonably warm January, with temperatures dipping again the next month. As winter has transitioned into spring 2021, ridership has rebounded.

![Total](/Images/TotalRiders.png)

#### Ridership by Location
Four out of the five New York City boroughs have Citibike stations. Manhattan has stations throughout the island, while stations in Brooklyn, Queens, and the Bronx are generally concentrated closer to Manhattan and do not extend fully into those boroughs. 

South and midtown Manhattan have the highest ridership levels, with some stations exceeding 50,000 rides over the entire time period analyzed. While not all the stations in those areas are heavily used, the concentration of heavily used stations is greatest there. 

Outside Manhattan, the most popular stations are consentrated by the Brooklyn and Williamsburg Bridges, suggesting that there is a significant number across those bridges into Manhattan. After those hotspots, ridership tends to decrease into the low thousands or even hundreds as you go further into the outer boroughs. 

Overall, Manhattan is the clear location for most riders, even though it has a lower population than the other boroughs. This trend holds for both customers and subscribers. The reasoning behind the concentration behind these two groups may be different, however. For subscribers, most likely to be local users, a high concentration in Manhattan may be beccause Citibike is used more as a commuting tool than for leisure, as many people work in Manhattan and live in outer boroughs or suburbs. For customers, the logic may be that Manhattan is the largest borough for tourism (Times Square, Madison Square Garden, etc) and so Citibike may be a draw for tourists. More data is needed to determine the breakdown in ridership purpose between these groups. 

![Stations](/Images/StationMap.png)

#### Ridership by Sex
When breaking down ridership by sex, the data clearly show that the majority of subscribers are men, and the majority of customers decline to report their sex. Until early February 2021, men made up the greatest number of riders. 

After February 2021, those who decline to report their sex made up a majority of riders. This indicates a strong uptick in rides among customers rather than subscribers. This is also highly coorelaterd with age (see below) as those 45-54 are less likely to report their sex. The reason for this age group not reporting their sex is unclear, though it may be that people are less likely to report their sex when they are purchasing a rid at a station as opposed to when they are signing up for a long-term membership online.

Average ride duration also varies by sex, with females' average ride being about 4 minutes longer than mens'. This may be an anomoly, or it may indicate that, while man made up the majority of ridership, they are taking shorter trips. Those who declined to report their sex had a greater average ride time than either males or females. Notably, their average time clocked in at over 30 minutes, the threshold for paying an additional fee above the baseline price. Again, it is not clear why this is taking place. A longer time horizon may reveal if this is a long-term trend or if it is simply related to an unusual number of people not reporting their sex. 

![Sex](/Images/SexDashboard.png)

#### Ridership by Age
When breaking down ridership by age, those age 25-34 made up the greatest number of riders until February 2021, when rides among those 55-54 took off, while other age groups' ridership plummeted. Once again, the reason for this in unclear. One possible explanation is that older age groups were the first to be vaccinated against COVID-19, making them more willing to venture outside. However, one would expect to see other age groups rising as vaccination eligibility expanded, which has not happened at this point. Another explanation is that age is self-reported (see below on how this may affect the data). If there are Citibike perks for those over 45, such as discounts. In this case, younger groups may be self-reporting as older to take advantage of those perks. 

In terms of ride duration, younger age groups stand out as riding longer, which would make sense as they are generally in better physical shape. Ride duration generally levels off in the middle age groups and then declines again in late age. One anomoly in the data is at age 51, which aligns more with those in younger age groups (see below for likely explanation here)

![Age](/Images/AgeDashboard.png)

#### Data Constraints
There are several constraints both inherant to the dataset and also to how I set up my analysis.

The first thing to note is that this data is a sample. Because Tableau Public can ony handle so many rows of data, I needed to cut down on the very large dataset before building any visualizations. To achieve a smaller sample, I first searched for a random sampling feature in Tableau, but it does not seem to be able to generate a random sample on the Data Source page. Instead, I cut off bikeids at the highest end, until I achived a sample size Tableau could handle. By cutting off bikeids in this way, my sample is not exactly random. However, there seems to be enough churn among the bikes' location I believe that my results and analysis are still statistally sound. That said, it may have distorted a full picture of the data. 

One of the biggest complications of the dataset are that sex and birth year are self-reported. Citibike either has no way to verify this information or simply doesn't bother. This means that any analysis based on age or sex must be viewed with some skepticism. 

Of interest in my analysis is the large amount of data concentrated around age 51. This phenomenon is most likely due to the fact that younger riders think it is amusing to enter their birth year as 1969. Substracting 1969 from 2020 yields age 51, meaning that much of the data in this age group may well be younger riders. It is unclear if this is what is driving the current surge seen in the data of ridership among those age 45-54, but it almost certainly plays some part in these observations. 

