---
layout: post
title:  "Scoring Big with Super Bowl Ad Data: Web Scraping, APIs, and More!"
description: Curating the perfect dataset to answer marketing questions doesn't have to be complicated. In this post, I'll let you in on the techniques I used to create my Super Bowl Ad dataset.
image: /assets/img/Super_Bowl-Logo.png
display_image: true
hide_title: true
---
### The Big Game

Making it to the Super Bowl is the dream of many athletes, but it's also a coveted night for marketing professionals. Every year, brands line up to fork over millions of dollars for a chance to have a 30-second ad spot during the event, which an estimated 127.7 million viewers tuned in for in 2025. Advertisers aim to capitalize on the large audience, and Super Bowl ads have become a part of the Big Game experience. Many people even watch just to enjoy the ads, polling shows. But is the price of the ad spot, production, and extravagant celebrity endorsements actually worth it for the companies?

### Data Science Question

To answer this broad question, I narrowed it down to something specific, measureable, and feasible for me to collect data on. All good data science starts with a good question. Given the recency of the 2025 Super Bowl, I chose to use data from the 2024 Super Bowl where the dust has already settled. I thought about the data I had access to, and what it could tell me. My question of interest became:

#### How did Super Bowl 2024 ads affect short-term brand reach and influence?

Using data from Youtube, Google, Wikipedia, marketing reports, and my own observations, I set out to answer this question.

### The Ethics of Data Collection

Data is power. That's why it's important to be ethical about the way we collect it, especially through web scraping. Before webscraping, it's important to check out the robots.txt page on the site of interest. Because I was going to scrape from Wikipedia, I used [their robots.txt page](https://en.wikipedia.org/robots.txt) to make sure I was allowed to do so. Here is what that looks like:

![Figure 1](https://sofiadscribner.github.io/insights-unlocked-blog/assets/img/robots.png)

This is just the first few entries, but as you can read, Wikipedia has a pretty tolerant policy for web scraping. They have listed a few specific bots that they want to disallow for bad behavior, but a small project like mine was aligned with their policies.

I also used Youtube's API to gather information about the view and like counts for the 2024 Super Bowl ads. As with most well-documented APIs, Youtube has clear policies for the use of their data. The data I gathered was aggregated data, rather than user-specific information about who watched the videos. APIs are a great way to ensure the ethical use of data.

I planned to use some polling data from YouGov, but I wanted to make sure it was allowed by their [policies](https://business.yougov.com/public-data-license). These policies state "You may: Use, share, and adapt the Licensed Data for non-commercial purposes (e.g. academic research, journalism, critique, personal blogs, and newsletters)." So I knew it was ethical for me to move forward.

### Web Scraping (Wikipedia)

First, I wanted a list of all the ads from the 2024 Super Bowl, along with descriptions of them and other general information. To get this list, I chose to scrape a table from [this Wikipedia page](https://en.wikipedia.org/wiki/List_of_Super_Bowl_commercials). 

![Figure 2](https://sofiadscribner.github.io/insights-unlocked-blog/assets/img/wikipedia.png)

Wikipedia articles often have a variety of tables that are pretty simple to web scrape. My python code for scraping this particular table can be found in the GitHub repo for this project, which I'll be linking at the end of this post. 

Because this Wikipedia table had sub-categories for each type of product being advertised, I had to adjust my code a few times to make sure I included those correctly in my dataframe. I also had to manually correct a few lines of my data. Web scraping is rarely perfect, because the source html is rarely perfect, but it's a very useful tool for quick data collection.

### APIs (Youtube)

APIs or Application Programming Interfaces are a set of protocols that allow applications to communicate with each other. In my case, I wanted to communicate with Youtube's API to download data for many videos in a quick and effective way. Youtube has a very extensive and well documented API, which you can find linked [here](https://developers.google.com/youtube/v3/docs/). I created my own developer portal and generated an API key, which allowed me to access the API.

In order to get the data I wanted, I went to Youtube and gathered the video IDs of the videos I was interested in. I then used Python to loop through the video IDs, making requests to the API and gathering the stats I was interested in. That code can be found in the project repo.

The main challenge with this method is just making sure to understand the different endpoints of the API you want to use. An endpoint is a URL that corresponds to a function or resource within an API. Every API's endpoints are different, and each require different parameters. A really helpful video for understanding Youtube's API can be found [here](https://youtu.be/D56_Cx36oGY?si=em14cpnwbhVNsQjj) One thing I had to adjust for was that Youtube only allows 50 video IDs at a time to be requested, so I had to break my videos into two chunks. However, once I understood Youtube's videos endpoint, getting the data I needed was simple.

### Google Trends

One of my favorite data sources for this project was Google Trends.