---
layout: post
title:  "How to Build an Effective KPI Dashboard in Tableau"
description: Turn raw data into actionable insights presented in a beautifully formatted dashboard for stakeholders to interact with.
image: /assets/img/Tableau-Logo.jpg
display_image: true
---

#### What are KPIs?

A KPI is a Key Performance Indicator. KPIs are measurable factors that can demonstrate the success of an organization in achieving their goals. KPIs come from data, and they allow teams to make data-driven decisions about how to move forward. Some examples of KPIs in business include:

- Revenue Growth
- Average Order Value (AOV)
- Profit Margin
- Customer Lifetime Value (CLV)

There are many KPIs depending on the businuss or organization. In order to be an effective KPI, a measure should be specific, relevant, and achievable.

#### Why Tableau?

One extremely effective way to communicate KPIs to stakeholders is Tableau. Tableau allows data analysts to communicate findings in a clear, visually appealing, and interactive format. This is done through dashboards. Dashboards are your new best friend!

The benefits of using a Tableau dashboard to communicate KPIs can't be overstated. Using dashboards, you can create tables and visualizations with filters that stakeholders can interact with. Additionally, Tableau can be connected to a database or spreadsheet and automatically refresh as new data becomes available.

One of the best things about Tableau is that the visualizations you can create with it are ***simply beautiful***. In a matter of minutes, you can produce charts and graphs that are sleek, professional, and very aesthetically pleasing.

So follow along with me as we create a simple KPI dashboard using Tableau's built in practice data, the Superstore dataset!

#### Step 1: Import the Data

For this tutorial, we'll be using the Superstore dataset. It's built in with every Tableau installation.

When you open Tableau, you'll see this homescreen:

![Figure 1]({{site.url}}/{{site.baseurl}}/assets/img/tab-1.png)

You have many different options for where to source your data from. Click the "Sample-Superstore" dataset.

The next screen Tableau will give you is the Data Source tab:

![Figure 2]({{site.url}}/{{site.baseurl}}/assets/img/tab-2.png)

This tab gives you a chance to look over your data, and make sure it looks how you expected it to. 

Check to see if qualitative variables are in blue. Tableau calls these dimensions. Quantitative variables, or measures as Tableau refers to them, should be displayed in green.

You can also use this tab to make connections between multiple dataframes, which Tableau has automatically done for the three Superstore tables, People, Orders, and Returns.

#### Step 2: Create Visualizations