# IPL Report Power BI Project

This project presents a comprehensive analysis of the Indian Premier League (IPL) seasons from 2008 to 2024. The report was developed using **Power BI** and showcases key insights and statistics about teams, players, and matches over the years. The dataset was sourced from KAGGLE and includes detailed information on each season, match statistics, and player performances.

## Links
- **Dataset**: https://www.kaggle.com/datasets/rajsengo/indian-premier-league-ipl-all-seasons
- **Live Dashboard**: https://app.powerbi.com/view?r=eyJrIjoiOTBlMjU3ZTctYjRjYi00NTllLWI4ZDQtMWMwYjY1NWRkZDU1IiwidCI6ImVhYTYyODJiLWQ3NDktNDFmZi1iMjU1LTlkZTAzYmRjNzM5MSJ9&pageName=e71a431924c80936e332
  
## Table of Contents
- [Overview](#overview)
- [Data Cleaning](#data-cleaning)
- [Data Modeling](#data-modeling)
- [Building Visuals](#building-visuals)
- [10 Key Insights](#10-key-insights)
- [How to Use](#how-to-use)
- [Conclusion](#conclusion)

## Overview
This Power BI report is divided into four main pages:
1. **HOME**: Introduction to IPL with navigators to other pages.
2. **IPL OVERVIEW**: Summary of IPL seasons, top stadiums, umpires, and season-wise analysis.
3. **TEAM PROFILE**: Performance analysis of teams across seasons and venues.
4. **PLAYER PROFILE**: Analysis of top performers, including top six and four hitters, and bowler-batter face-offs.

## Data Cleaning
The dataset consisted of several CSV files, organized into folders for the 2022, 2023, and 2024 seasons. In this phase:
- Data from the 2022 and 2023 folders were removed.
- Data from the 2024 season was appended to the historical data (2008-2023) using the **APPEND QUERY** function in Power Query.
- Additional cleaning operations included:
  - **Removing errors**
  - **Fixing data types**
  - **Imputing null values using statistical methods**
  - **Creating custom and conditional columns**
- A new table, **TEAM PROFILE**, was created from the "all season details" table to achieve the required data granularity.

## Data Modeling
The **Star Schema** was leveraged in data modeling, with the "all season details" table at the center. Relationships between different tables were established using matching columns, enabling effective filtering in visuals.

## Building Visuals
The report is designed to be visually engaging and informative:
- **HOME Page**: Includes a brief description of IPL, navigators to other pages, and an IPL logo linking to the official IPL page.
- **IPL OVERVIEW Page**:
  - **Cards**: Display total seasons, total teams participated, and total matches played.
  - **Bar Charts**: Show top 10 stadiums and 10 most used TV umpires.
  - **Line Charts**: Illustrate average runs per season, total no-balls, and the percentage of wide balls per season.
  - **Table**: Lists the top four ranked teams of all seasons.
  - **Hover Feature**: On the average runs per season line chart, hovering displays total boundaries and count of runs.
- **TEAM PROFILE Page**:
  - **Tables**: Show team performance in each season and venue.
  - **Column Charts**: Depict top 5 run scorers and top 5 wicket-takers for each team in each season.
  - **Parameterized Chart**: Displays average runs, total boundaries, and total wickets for each team in each over in each season.
  - **Clear Slicers Button**: Allows users to clear all slicers for easier data exploration.
- **PLAYER PROFILE Page**:
  - **Bar Charts**: Show top 5 six hitters and top 5 four hitters in each season.
  - **Visual**: Displays face-off between each bowler and batter in each season.
  - **Clear Slicers Button**: Similar to the TEAM PROFILE page.

### Key Features Utilized:
- **Parameterized Charts**
- **Edit Interaction**
- **Custom and Conditional Columns**
- **Custom Tooltip**: Created two separate visuals as a tooltip for average runs per season line chart.
- **DAX Measures**: A total of 35 DAX measures, ranging from simple to complex, were created to generate insights.
- **Dynamic Title**: Leveraged DAX to create dynamic titles which changes upon selection of slicers.

## 10 Key Insights
1. **16 teams** have participated across **17 seasons**, with a total of **1106 matches** played.
2. **Wankhede Stadium** in Mumbai is the most used stadium, hosting **118 matches**.
3. **Anil Chowdhury** is the most popular TV umpire.
4. **Average Runs** per season have increased since 2020.
5. The **least number of boundaries** (1827) was hit in 2009.
6. **CSK** is the most consistent team, with the most playoff qualifications despite a 2-year ban.
7. **Virat Kohli** is the top run scorer with **7897 runs**, and **Yuzvendra Chahal** is the leading wicket-taker with **201 wickets**.
8. **2016** was Virat Kohli's most successful year, with **973 runs**.
9. **Chris Gayle** is the highest six-hitter, with **357 sixes**.
10. **Shikhar Dhawan** is the most prolific boundary hitter, with **768 fours**.


## How to Use
To explore the report:
1. Use the **Page Navigators** on the HOME page to access detailed analysis on IPL Overview, Team Profile, and Player Profile.
2. Interact with the **visuals** by hovering, filtering, and using slicers to dive deep into specific details.
3. Use the **Clear Slicers Button** to reset filters on the TEAM PROFILE and PLAYER PROFILE pages.

## Conclusion
This project showcases the powerful capabilities of Power BI in handling complex datasets and generating actionable insights. The IPL Report not only serves as a comprehensive analysis tool but also demonstrates advanced data modeling, DAX calculations, and visual storytelling techniques.
