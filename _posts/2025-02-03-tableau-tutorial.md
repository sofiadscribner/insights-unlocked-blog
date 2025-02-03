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

![Figure 1](https://sofiadscribner.github.io/insights-unlocked-blog/assets/img/tab-1.png)

You have many different options for where to source your data from. Click the "Sample-Superstore" dataset.

The next screen Tableau will give you is the Data Source tab:

![Figure 2](https://sofiadscribner.github.io/insights-unlocked-blog/assets/img/tab-2.png)

This tab gives you a chance to look over your data, and make sure it looks how you expected it to. 

Check to see if qualitative variables are in blue. Tableau calls these dimensions. Quantitative variables, or measures as Tableau refers to them, should be displayed in green.

You can also use this tab to make connections between multiple dataframes, which Tableau has automatically done for the three Superstore tables, People, Orders, and Returns.

Click the Sheet 1 tab.

#### Step 2: Create Visualizations

Now that we've got our data, we can start visualizing it. Each of our four graphs is going to have its own sheet in Tableau.

Here is what the sheet looks like:

![Figure 3](https://sofiadscribner.github.io/insights-unlocked-blog/assets/img/tab-3.png)

Let's say that the executives at the Superstore have asked us to create a sales KPI dashboard. 

##### Time Series

Let's start by making a line graph that will show the sales over time. On the left, we have all of our dimensions and measures. In the middle of the screen, we have the chart that we're creating.

Start by double-clicking Sales and Order Date. Order Date should automatically populate in the columns section at the top of the screen and Sales goes to the rows.

![Figure 4](https://sofiadscribner.github.io/insights-unlocked-blog/assets/img/tab-4.png)

Now we have a line graph of sales over time. Let's refine this a little bit. Say the executives are most interested in looking at the data from month to month for the year 2024.

To switch the x-axis to show months instead of years, right-click the date dimension and select Month on the dropdown.

![Figure 5](https://sofiadscribner.github.io/insights-unlocked-blog/assets/img/tab-5.png)

Now we're seeing the data over months instead of years! We just need to filter out everything but 2024.

In order to do this, go back to the variables on the left and drag Order Date to the Filters box. Tableau assumes you want to filter out a range of dates, which is correct, so hit next.

![Figure 6](https://sofiadscribner.github.io/insights-unlocked-blog/assets/img/tab-6.png)

Edit the starting date to be 1/1/2024 and hit OK. Now the line graph is showing the KPI we're looking for.

![Figure 7](https://sofiadscribner.github.io/insights-unlocked-blog/assets/img/tab-7.png)

Take some time to further refine the graph, adding labels, removing unneccessary text, and changing the color. Tableau's interface is fairly intuitive for this sort of thing.

![Figure 8](https://sofiadscribner.github.io/insights-unlocked-blog/assets/img/tab-8.png)

Our graph of sales over time is ready! 

##### Bar Chart

Another great KPI for Superstore sales data could be Top-Selling Categories. Let's make a bar chart to display these. Click the on the chart icon with a plus sign at the bottom of the screen to add another worksheet.

Go to the variables on the left side of the screen and click the dropdown next to Product. Drag Sub-Category to the Rows. Drag Sales to the Columns. You should get a bar chart like this:

![Figure 9](https://sofiadscribner.github.io/insights-unlocked-blog/assets/img/tab-9.png)

You can make the chart more readable by clicking the sort button at the top to put the bars in descending order.

Again, the stakeholders are mostly focused on sales during 2024, so create the same time filter by dragging Order Date to the Filters box and focusing in on dates in 2024.

The visualization would probably be more effective if we just limit it to the top 5 categories of merchandise. To do this, drag Sub-Category from the left onto the Filters box and select the Top tab at the top. Tell Tableau you want it to display the top 5 sub-categories by sum (or total) sales.

![Figure 10](https://sofiadscribner.github.io/insights-unlocked-blog/assets/img/tab-10.png)
