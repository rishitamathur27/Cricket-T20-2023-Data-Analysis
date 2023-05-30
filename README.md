# Cricket-T20-2023-Data-Analysis
In this project, I'll cover web scraping (ESPN Cricinfo website), using python and Power BI to perform analysis part on T20 2023 world cup cricket data.


Following parameters help assess the performance of both batters and bowlers in cricket matches. By considering these criteria, we can gain insights into the consistency, efficiency, and involvement of players in the game.

![image](https://github.com/rishitamathur27/Cricket-T20-2023-Data-Analysis/assets/38039850/cb2eaf6c-7072-4acd-9baf-ab204de35a4c)


Performed the below steps in this project:

1. Data collection from the cricket data website.
2. Data preparation using pandas.
3. Built visuals in dashboard using Power BI.


Using the 'BrightData' to collect the data from the urls inspite of writing the scraping code. As, it uses proxy n/w for building web scrapers.


After importing the csv files to Power BI, we'll first need to transform the data. 

1. In file ("dim_match_summary"):
  * Remove redundant characters, duplicates from the table.
  * Create a conditional column "Stage", if date< 22 Oct 2022 "Qualifier" otherwise "Super 12" (here we can see Scotland v/s Zimbabwe       was the last qualifier match). Also, change this column to "text".

2. In file ("fact_bowling_summary"):
  * Rename some of the columns.
  * Create "balls" column using "overs" (overs1*6 + overs2) column using "Custom column" by first splitting this column into 2 and replace "null values" with 0.
  
3. In file ("fact_batting_summary"):
  * Rename some of the columns.
  * Change "out/not out" column to "out" and changes values into boolean ones.
  * Remove useless character in the column "batsmanName"



After this, link the tables (basically do data modelling) and then build DAX measures which would be useful to build actual visuals. For this, create a category/folder by clicking on "Enter Data" where we can keep all DAX measures. Further, right click on it and click on "New measure".

We'll need to create the some DAX measures based on the requirement.

Drag and drop the required columns to the dashboard and filter the valued based on the parameters mentioned in the starting.


Design the dashboard for the cleared and detail understanding of the data :)
