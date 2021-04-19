# An Analysis of Kickstarter Campaigns
## Overview
This analysis is a deep dive into the drivers of success and failure of Kickstarter campaigns. This analysis is intended to provide insight into key trends in how kickstarter campaigns perform across a few key metrics. This analysis evalutes the relationship outcomes based on campaign goals and outcomes based on launch date. While the overall data set includes multiple categories of categories of campaigns, this analysis focuses on the Theater and Play categories/subcategories.

## Analysis and Challenges
Our first goal was to assess how Theater outcomes are impacted by the launch date of the campaign. In the chart below, we have mapped the number of campaigns launched in a given month according to the outcome. This includes campaigns launched in multiple geographies and all Theater subcategories (musicals, plays, etc.) In the accompanying Excel File (Kickstarter_Challenge), this chart can be filtered by year to show trends between 2009 and 2017. The following chart aggregates outcomes over the entire eight year period for the initial data set. 

![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/81983110/115293130-f36f8a00-a124-11eb-952d-f1be6ad10115.png)

Our second goal was to drill down further into the Play subcategory to understand this subcategory in greater detail. In the chart below, we have mapped the percentage of a given outcome relative to campaign goal size. This chart describes how many campaigns had a particular outcome compared to the number of launched within that bucket. For this analysis, we have grouped campaigns in buckets between a range of $5000. This chart includes campaigns launched in multiple geogrpahies. Of note, the first bucket includes all campaigns with a goal less than $1,000 and the final bucket includes all campaigns with goals above $50,000.

![Outcomes_vs_Goals](https://user-images.githubusercontent.com/81983110/115293052-d63abb80-a124-11eb-9688-364c3c7f9b60.png)

### Challenges
A challenge in the creation of both charts was the existence of 'live' campaigns within the data set. As the goal of this analysis is to understand how campaigns perform overtime, these data points were appropriately eliminated. Another potential challenged faced in running the analysis for the outcomes vs goals was the potential to unintentially omit campaigns on the boundary. This challenge was overcome through the inclusion of ">=" and "<=" within the COUNTIFS functions. It proved helpful to double check the functions by creating a final column to count all successful, failed and canceled plays and comparing this to the sum of all functions within the category (ie. Kickstarter_Challenge!Outcomes Based on Goals E14 is equal to both SUM(E2:E13) and SUM(B14:D14).

