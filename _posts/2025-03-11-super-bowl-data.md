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

Using data from Youtube, Google, Wikipedia, marketing reports including YouGov and Harris, and my own observations, I set out to answer this question.

### The Ethics of Data Collection

Data is power. That's why it's important to be ethical about the way we collect it, especially through web scraping. Before webscraping, it's important to check out the robots.txt page on the site of interest. Because I was going to scrape from Wikipedia, I used their robots.txt page to make sure I was allowed to do so. Here is what that looks like:

![Figure 1](https://sofiadscribner.github.io/insights-unlocked-blog/assets/img/robots.png)

This is just the first few entries, but as you can read, Wikipedia has a pretty tolerant policy for web scraping. They have listed a few specific bots that they want to disallow for bad behavior, but a small project like mine was aligned with their policies.

I also used Youtube's API to gather information about the view and like counts for the 2024 Super Bowl ads. As with most well-documented APIs, Youtube has clear policies for the use of their data. The data I gathered was aggregated data, rather than user-specific information about who watched the videos. APIs are a great way to ensure the ethical use of data.