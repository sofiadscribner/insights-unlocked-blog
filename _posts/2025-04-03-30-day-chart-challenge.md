---
layout: post
title:  "The Art of Data Visualization: My 30 Day Chart Challenge!"
description: I was inspired by the 30 Day Chart Challenge account on LinkedIn. Can I make a data visualization each day in April that I'm proud to show off?
image: /assets/img/30daycc-logo.png
display_image: true
hide_title: true
---

## The Challenge

Each April, data viz professionals from around the world participate in the [30 Day Chart Challenge](https://www.linkedin.com/company/30daychartchallenge/posts/?feedView=all). This challenge has been going on for several years, and according to their page, it was created by Cédric Scherer and Dominic Royé, supported by Wendy Shijia and Ansgar Wolsing. This year, the prompts are as follows:

![Figure 1](https://sofiadscribner.github.io/insights-unlocked-blog/assets/img/prompts.jpg)

Because I've recently learned Tableau, as well as becoming more confident in my data visualization skills in Python, I was inspired to participate in the challenge! Even though half of this month is going to be consumed by my final exams for school, I still wanted to have a personal project that would remind me why I'm studying statistics and that data can be fun! We will see how this goes. I think it will also be a good test of my diligence.

I will display each chart and my explanations here, and I'll list the data sources and the software used to create each on at the bottom. Additionally, [this Github repo](https://github.com/sofiadscribner/30-day-chart-challenge) contains all the code and data.

### Category 1: Comparisons

#### Day 1 - Fractions

![Figure 2](https://sofiadscribner.github.io/insights-unlocked-blog/assets/img/day-1.png)

For the first prompt, I chose to visualize data about the increasing importance of influencer marketing for Gen Z. When I thought of the prompt "fractions," a stacked bar chart immediately came to mind. These charts are great for comparing proportions among different populations.

#### Day 2 - Slope

![Figure 3](https://sofiadscribner.github.io/insights-unlocked-blog/assets/img/day-2.png)

For day two, I'll be honest, I forgot a little bit about the overarching category of comparisons. I focused a lot on "slope." I'm still getting the hang of how this challenge works! For today's chart I chose to visualize the relationship between the basketball ability of an NBA player and the size of their Instagram following, with a focus on the players that had an unusually low or unusually high number of followers for their skill level.

#### Day 3 - Circular

![Figure 4](https://sofiadscribner.github.io/insights-unlocked-blog/assets/img/donut.png)

For today's chart challenge, I chose to use a donut chart to compare the way I allocate my time to each category on Thursdays. Donut charts are a more palletable version of a classic pie chart, in my opinion, but still not the most visually interpretable.

#### Day 4 - Big or Small

![Figure 4](https://sofiadscribner.github.io/insights-unlocked-blog/assets/img/gdp.png)

For today's prompt, I wanted to visualize the difference in per capita GDP between the richest and poorest country. I also added the United States as a point of reference. I played around with the colors and labels a bit on this one, and I'm happy with how it turned out. I think it communicates the message clearly.

#### Day 5 - Ranking

![Figure 5](https://sofiadscribner.github.io/insights-unlocked-blog/assets/img/byu_plot.png)

My visualization for today ranks the top 5 most popular fields people graduate in at my school, Brigham Young University. This bar chart ended up being surprisingly tricky to do in R because of the extra details I wanted to add, and it was my first time using the ggimage package to include an image, so I learned a lot.

#### Day 6 - Florence Nightingale

![Figure 6](https://sofiadscribner.github.io/insights-unlocked-blog/assets/img/crime.png)

Today's visualization, inspired by Florence Nightingale's famous Crimean War chart, represents the distribution of violent crime types over the past year in Baltimore. These rose charts are very aesthetically pleasing and I think they communicate well. However, they're limited by the lack of numerical labeling. In the future, I'd make a tooltip to help with that.

### Category 2: Distributions

#### Day 7 - Outliers

![Figure 7](https://sofiadscribner.github.io/insights-unlocked-blog/assets/img/gini.png)

While they can be a little tricky for people less fluent in data to conceptualize, I still think boxplots are a great way to clearly show outliers. This visualization shows the distribution of the Gini coefficient among the countries of the world, with four clear outliers.

##### Footnotes

*Day 1: I used Tableau to create the chart, and I got the data from [this KS&R article about influencer marketing](https://www.ksrinc.com/how-much-influence-influencers-have/).*

*Day 2: The player performance data was from the [Official NBA Stats site](https://www.nba.com/stats), and the Instagram data was from [this website](https://www.popularbasketballers.com/), which gathers Instagram data for popular basketball players and is updated regularly. The visualization was made using Tableau.*

*Day 3:  I used the seaborn package in Python to create this chart, and the data was calculated from my own life experiences.*

*Day 4: I used Tableau to create the visualization, and the data came from this indicator on [data.worldbank.org](https://data.worldbank.org/indicator/NY.GDP.PCAP.CD).*

*Day 5: I used ggplot in R to create the visualization, as well as adding the BYU logo using ggimage. The data came from [BYU's official data page](https://data.byu.edu/0000018f-0714-d406-a19f-c75e9aca0000/cds-2023-2024-pdf),*

*Day 6: I used Python to wrangle the data and create the visualization, and the Baltimore crime data can be found at [this link](https://data.baltimorecity.gov/datasets/baltimore::nibrs-group-a-crime-data/about).*

*Day 7: I used Tableau for the visualization, and the Gini index data was downloaded at [this link](https://worldpopulationreview.com/country-rankings/gini-coefficient-by-country).*