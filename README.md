# Kickstarting with Excel

## Overview of Project

### Background
Louise's play came within a small amount of its fundraising goal in a short amount of time. She requested information
about how other plays fared based on their launch dates and their fundraising goals.

### Purpose
This project analyzes the number of plays that were successful, failed, or canceled based on the month a play
was launched in. This analysis includes the ability to filter the plays by the year they were launched in. The total number of 
successful, failed, or canceled plays were charted by month.

A seperate analysis was done comparing the number of plays that were successful, failed, or canceled based on their
fundraising goals. A percentage of each category based on the total plays in a fundraising goal range were charted.

All sheets referenced are located in https://github.com/skgolden13/kickstarter-analysis/blob/main/Kickstarter_Challenge.xlsx .

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
A new column in the "Kickstarter" sheet titled "Year" was created using the formula =YEAR(S2). Column S contains the date a project was created.
This formula was copied down for the entire set of data. A pivot table and pivot chart was created using this data and is located in the sheet "Theater Outcomes by Launch Date." This pivot filters by parent category and year. The parent category filter is set to "theater" while the year filter is set to all years. The columns in the pivot are the total number of successful, failed, and canceled theater projects along with a grand total. The rows are the twelve months of the year.

### Analysis of Outcomes Based on Goals
A new sheet titled "Outcomes Based on Goals" was created to analyze the outcome of plays based on their fundraising goals. The COUNTIFS function was used to determine the total number of successful, failed, and canceled plays within a specific fundraising goal range. These values were then used to calculate a percentage of successful, failed, or canceled plays and charted on a line chart. 
An example of the COUNTIF function and SUM function for the percentage calculation can be found at 

### Challenges and Difficulties Encountered
Potential challenges that could be encountered include use of the COUNTIFS function. Understanding the syntax for the conditions in terms of requiring quotes and the logic statements may not be intuitive. These errors may also be difficult to find when troubleshooting the formula. Generating a pivot table and chart that displays the correct information and the appropriate filters may also be difficult to organize.

## Results

### Results of Outcomes Based on Launch Date
Theater projects launched between May and August produce the greatest number of successful projects. This value peaks in May and decays linearly through August and September. The early spring, fall, and winter months still produce more successful theater projects than not, but at significantly reduced rates compared to May, June, July, and August. These trends can be seen in https://github.com/skgolden13/kickstarter-analysis/blob/main/Theater_Outcomes_vs_Launch.png .

### Results of Outcomes Based on Goals
Plays with fundraising goals below $15,000 have greater success rates. After the $15,000 mark, plays become successful less than 50% of the time. This changes again at the $35,000 mark before going below 50% again at the $45,000 mark. No plays were canceled at any fundraising goal. These trends can be seen in https://github.com/skgolden13/kickstarter-analysis/blob/main/Outcomes_vs_Goals.png .

### Limitations of the Dataset and Additional Recommendations
This dataset includes theater projects and plays launched across the world between the years 2009 and 2017. It is recommended to include a filter for projects launched in the region of the world that _Fever_ is being launched in. The outcomes based in launch date analysis would be better served by looking at the percentages of successful, failed, or canceled plays. Similar to how the outcomes based in goals analysis is performed. It may also be beneficial to analyze results from the past 5 years to get a more accurate picture of the current results of similar projects.

