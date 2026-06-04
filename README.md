## Executive Summary

This project analyzes over 120 years of Olympic athlete participation and performance data to uncover trends in country success, athlete achievements, medal distribution, participation patterns, and gender representation.

Using Excel, Power Query, and Power BI, the dataset was cleaned, validated, transformed, and modeled to support interactive reporting and analysis. The project resulted in three Power BI dashboards focused on Country Performance, Athlete Performance, and Olympic Participation & Demographics.

The analysis identified key trends in Olympic participation, highlighted dominant countries and athletes, and provided insights into the evolution of gender representation throughout Olympic history.

## Project Overview

The Olympic Games represent one of the world's largest international sporting competitions, bringing together athletes from diverse countries and sporting disciplines.

This project was conducted to evaluate historical Olympic performance and participation data while demonstrating the end-to-end analytics process, including:

- Data quality assessment and cleaning
- Exploratory Data Analysis (EDA)
- Data modeling
- Dashboard development
- Insight generation and recommendations

The final deliverable consists of three interactive Power BI dashboards designed to support the analysis of country performance, athlete achievements, and participation trends.

## Data Source

The analysis was performed using an altered version of the 120 Years of Olympic History: Athletes and Results dataset.

### Dataset Summary

| Metric |	Value   |
|--------|----------|
| Initial Records |	271,117 |
| Final Records |	269,731 |
| Coverage Period |	1896–2022 |
| Data Granularity |	Athlete-Event Level |

The dataset contains athlete-level information including:

- Athlete Name
- Sex
- Age
- Height
- Weight
- Team
- NOC
- Games
- Year
- Season
- City
- Sport
- Event
- Medal

An additional NOC Regions lookup table was used to support country-level analysis.

## Problem Statement

The objective of this project was to transform a large historical Olympic dataset into a reliable analytical solution capable of answering key business questions:

### Country Performance
- Which countries have achieved the greatest Olympic success?
- How have medal counts evolved over time?
- Which countries consistently dominate Olympic competition?

### Athlete Performance
- Who are the most successful athletes in Olympic history?
- Which sports produce the highest-performing athletes?
- How does athlete participation relate to medal success?
  
### Participation & Demographics
- How has Olympic participation changed over time?
- How has female participation evolved throughout Olympic history?
- What demographic patterns exist among Olympic athletes?
  
## Tools and Methodology
### Tools Used
| Tool | Purpose |
|------|---------|
| Excel |	Exploratory Data Analysis (EDA), Pivot Tables, Summary Statistics |
| Power Query |	Data Cleaning and Transformation |
| Power BI |	Data Modeling, DAX Calculations, Dashboard Development|

### Data Cleaning & Preparation

The following data quality checks and transformations were performed:

- Converted Age, Height, and Weight columns to numeric data types.
- Removed 1,385 duplicate records.
- Corrected an invalid year value (2202 → 2022).
- Standardized Singapore's NOC code (SIN → SGP).
- Assessed missing values across key fields.
- Applied median imputation grouped by Sport and Sex for Age, Height, and Weight.
- Investigated extreme values to distinguish valid records from data anomalies.

### Missing Values Identified
| Column |	Missing Values |
|--------|-----------------|
|Age |	9,315 |
|Height |	58,814 |
| Weight |	61,527 |
| Medal	229,896


## Data Modeling

A star-schema model was implemented in Power BI.




### Fact Table
- Olympic Athlete Events

### Dimension Tables
- Dim Country
- Dim Sport
- Dim Event
- Dim Games
- NOC Regions

**Dimension tables were created from referenced copies of the fact table in Power Query by extracting distinct values and removing duplicates.**

## Exploratory Data Analysis
### Athlete Demographics
The average Olympic athlete was approximately 25 years old. Basketball recorded the highest average athlete height at approximately 191.5 cm. Tug-of-War recorded the highest average athlete weight at approximately 95.2 kg.
Extreme values identified during analysis were validated and confirmed as legitimate historical records.

### Correlation Analysis
| Variables |	Correlation |
|-----------|-------------|
| Height vs Weight |	0.80 |
| Age vs Height |	0.11 |
| Age vs Weight |	0.20 |

The analysis revealed a strong positive relationship between height and weight, while age showed only weak relationships with physical characteristics.

### Participation Trends
The 1992 Barcelona Olympic Games recorded the highest athlete participation. Participation declined after 1992 due to the scheduling separation of Summer and Winter Olympic Games. Female participation increased steadily across Olympic history.

### Medal Analysis
The 2008 Olympic Games recorded the highest medal distribution. Athletics recorded both the highest participation and highest medal count. The United States achieved the highest overall medal count across all medal categories.


## Key Insights
### Country Performance

<img width="6150" height="3525" alt="Olympic Project - Country Performance" src="https://github.com/user-attachments/assets/9a41c5ee-48f1-489b-81f8-ebd3639bf77d" />

- The **United States** recorded the highest athlete participation and overall medal count.
- **Germany** recorded the highest athlete participation among European countries.
- Medal success remained concentrated among a relatively small number of nations.
- **London** recorded the highest cumulative athlete participation across hosted Olympic editions.

### Athlete Performance
- **Michael Phelps** emerged as the most decorated Olympian with **28 Olympic medals**, including **23 Gold medals**.
- Athletics recorded approximately **38,624 athlete** entries and **3,969 medals** awarded.
- Approximately **21% of athletes** won at least one Olympic medal, highlighting the competitive nature of Olympic participation.

### Gender Participation
- **Female** participation increased significantly throughout Olympic history.
- The highest female participation was recorded during the **2016 Olympic Games**.
-** Athletics** remained the most participated sport among both male and female athletes.
- Participation levels varied significantly across countrie.


## Dashboard Preview
### Dashboard 1: Country Performance

**Purpose:** Analyze country-level Olympic performance across time.

### Key Metrics

- Total Medals
- Gold Medals
- Silver Medals
- Bronze Medals
- Athlete Participation
- Country Rankings




### Dashboard 2: Athlete Performance

**Purpose:** Evaluate athlete achievements across sports and Olympic Games.

### Key Metrics

- Total Medals
- Olympic Appearances
- Event Participation
- Athlete Rankings
- Gold Medal Count




### Dashboard 3: Gender Participation

**Purpose:** Analyze participation trends and athlete demographics.

### Key Metrics

- Athlete Participation
- Female Participation
- Gender Participation Across Years
- Participation by Sport



## Recommendations
#### 1. Expand Elite Athlete Development Programs

Medal success remains concentrated among a relatively small number of countries. Emerging Olympic nations should continue investing in athlete development pathways, talent identification, and high-performance training programs.

#### 2. Increase Female Participation Opportunities

Although female participation has increased significantly over time, participation levels remain lower than male participation in many countries. Continued investment in women's sports development initiatives can help close this gap.

### 3. Promote Underrepresented Sports

Sports such as Polo, Cricket, Lacrosse, Alpinism, and Motorboating recorded relatively low participation levels. Increased awareness and development programs may encourage broader participation.

### 4. Support Emerging Olympic Nations

Countries with historically low participation may benefit from international sporting partnerships, athlete exchange programs, and improved access to training infrastructure.

## Limitations

- Historical Olympic records contained substantial missing values, particularly in Age, Height, and Weight fields.
- Missing values required statistical imputation, which may not perfectly represent actual athlete characteristics.
- Athlete-event records may count the same athlete multiple times across different Olympic Games and events.
- Historical data collection standards varied across Olympic editions, potentially affecting data completeness and consistency.

## Conclusion

This project transformed a large and complex Olympic dataset into a structured analytical solution through data cleaning, exploratory analysis, data modeling, and dashboard development.

The analysis revealed meaningful insights into Olympic participation, athlete demographics, country performance, medal distribution, and gender representation. The resulting Power BI dashboards provide an interactive platform for exploring Olympic history and support data-driven understanding of long-term Olympic trends.
