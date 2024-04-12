# SEMESTER PROJECT

### CS 625

### Sujitha Cherukuthota

### April 9

# SHOOTING INCIDENTS IN SCHOOLS 

## DATASET

Data Source URL : [Link](https://www.chds.us/sssc/data-map/)

#### ABOUT DATASET 

Certainly, let's start by providing an overview of the dataset and then move on to describe the sheets and the columns within the 'Incidents' sheet.

---

**Dataset Overview**

This dataset offers a comprehensive look at school shooting incidents in the United States. It is designed to provide educators, policymakers, and researchers with detailed information to analyze the trends, circumstances, and outcomes of these tragic events.

**Sheets in the Dataset**

The dataset is organized into multiple sheets, each containing specific aspects of school shooting data:
- `Incidents`: Detailed records of each shooting incident.
- `Victim`: Information about individuals affected by the shootings.
- `Shooter`: Data related to the individuals who carried out the shootings.
- `Weapons`: Details about the firearms used in the incidents.

**Columns in the 'Incidents' Sheet**

- `incident_id`: A unique identifier for each incident.
- `sources`: References to data sources where information about the incident was obtained.
- `number_news`: The count of news reports covering the incident.
- `media_attention`: Qualitative assessment of the media coverage intensity.
- `reliability`: A rating of the information reliability for the incident details.
- `date`: The date when the incident occurred.
- `quarter`: The fiscal quarter within which the incident took place.
- `school`: The name of the school where the incident occurred.
- `city`: The city in which the school is located.
- `state`: The state in which the school is located.
- `school_level`: The education level of the school (e.g., Elementary, Middle, High).
- `location`: Specific location at the school where the incident took place.
- `location_type`: Classification of the location (e.g., classroom, cafeteria).
- `during_school`: Indicates whether the incident happened during school hours.
- `time_period`: The time period during the day when the incident occurred.
- `first_shot`: Location where the first shot was fired.
- `summary`: A brief account of the incident.
- `narrative`: A detailed narrative description of the incident.
- `situation`: The situation or context in which the shooting occurred.
- `targets`: Individuals or groups targeted in the incident.
- `accomplice`: Information on whether the shooter had accomplices.
- `hostages`: Indicates whether hostages were taken during the incident.
- `barricade`: Specifies if a barricade situation occurred.
- `officer_involved`: Involvement of law enforcement officers in the incident.
- `bullied`: Information regarding whether bullying was a factor in the incident.
- `domestic_violence`: Indicates a domestic violence connection to the incident.
- `gang_related`: Signifies whether the incident was related to gang activity.
- `preplanned`: Denotes if the incident was premeditated.
- `shots_fired`: The estimated number of shots fired during the incident.
- `active_shooter_fbi`: Classification of the incident as an active shooter situation by the FBI.

#### WHY THIS DATASET?

I chose this dataset because it provides an invaluable compilation of data that's crucial for understanding school shootings in the United States. My objective is to delve deeply into patterns, causative factors, and the aftermath of such incidents with the hope of contributing to preventative strategies. This data is not only rich in detail but also spans a comprehensive time frame, offering the depth and breadth necessary for a meaningful analysis.

## STAKE HOLDER

Policymakers are the primary stakeholders of this dataset. They can utilize the analysis to understand the prevalence, causes, and aftermath of school shootings. This understanding is pivotal for crafting legislation, allocating resources for mental health services, enhancing school security protocols, and implementing educational programs that promote a culture of non-violence. The ultimate goal for these stakeholders is to leverage the data to protect students and educators and to ensure that schools are safe havens for learning and growth.

For policymakers, the findings from this dataset have far-reaching implications. The effectiveness of laws and policies can be measured against the data, ensuring that actions taken are not only reactive but also preventive. This can lead to a substantial real-world impact, potentially saving lives and creating a more secure future for the coming generations.


## EXPLORATORY DATA ANALYSIS

#### Data Cleaning

- `Handling Missing Values`:  Recognizing the importance of complete records, I addressed the missing values in 'number_news' by filling them with the column's mean, ensuring numerical consistency. I chose to remove any entries lacking essential data in the 'date' or 'state' columns, as these are vital for my temporal and geographical analyses.
  
- `Data Type Correction`: I converted the 'date' column to the datetime type to facilitate time-based analysis. Additionally, I transformed other columns that were incorrectly categorized as strings into numeric data types, setting non-convertible values as NaNs to maintain data integrity.


- `Duplicate Removal`: In my pursuit of data accuracy, I removed any rows that were exact duplicates, thereby preventing data redundancy from skewing the results of the analysis.

- `Irrelevant or Incorrect Data Handling`: I eliminated entries with future dates and those with illogical negative values in 'number_news'. Such entries are likely to be data entry errors and could distort the findings of my study.

#### STATICTICAL SUMMARY

<img src="https://github.com/sujithacherukuthota/FINAL-PROJECT/blob/main/STAT%20SUMMARY%201.png" width="300" height="300">

High schools experienced the most incidents, with 1,302 cases, which is significantly higher than other levels.
Elementary schools reported 358 incidents, and middle schools had 205 incidents.

This indicates that higher educational levels (like high schools) might be more prone to such incidents, possibly due to older student populations and associated factors like behavioral issues or accessibility to weapons.

Reliability: This column might measure the confidence or credibility of the incident report on a scale from 1 to 5. The average reliability score is 2.77, with a standard deviation of 0.996. This suggests that most reports are moderately reliable, with a fair number being rated as highly reliable (max = 5).

Year: The data spans from 1970 to 2022, with an average incident year around 2005.71. The spread of incidents over the years, from the minimum in 1970 to the maximum in 2022, helps to understand how incidents have been reported over time. The mean near 2006 suggests a possibly higher concentration of reported incidents around the mid-2000s.

### CORRELATION MATRIX

<img src="https://github.com/sujithacherukuthota/FINAL-PROJECT/blob/main/corr%20matrix.png" width="500" height="500">

A correlation matrix is a table showing correlation coefficients between variables. Each cell in the table shows the correlation between two variables. The value is in the range of -1 to 1. If two variables have high correlation, it means the when one variable changes, the other is likely to make a similar change if the correlation is positive, or an opposite change if the correlation is negative.

number_news has a correlation coefficient of 1 with itself, which is always the case for any variable (perfect positive correlation).

reliability and shots_fired both have coefficients of 1 with themselves, also indicating perfect positive correlation.

The correlation between number_news and reliability is 0.09, suggesting a very weak positive correlation. This implies that there is no strong relationship between the number of news reports and the reliability rating of the incidents.

The correlation between number_news and shots_fired is 0.23, which is a weak positive correlation. This indicates that there's a slightly positive relationship between the number of news reports and the number of shots fired.

Lastly, reliability and shots_fired have a correlation of 0.03, which is negligible, suggesting no meaningful relationship between these two variables.

## FINAL QUESTIONS

### QUESTION 1 

### "What has been the trend of school shooting incidents in the United States over the past decades, and what does the latest data suggest about the changing frequency of these occurrences?"


<img src="https://github.com/sujithacherukuthota/FINAL-PROJECT/blob/main/F%20CHART%201.png" width="800" height="600">

X-axis (Time Scale): The horizontal axis represents time, plotted in years. It extends from the early 1980s through to 2021, providing a long-term view of the data.

Y-axis (Incident Count): The vertical axis indicates the number of school shootings reported each year. The numbers on this axis range from 0 upwards, with specific increments not fully visible but likely at regular intervals based on the chart's grid.

Line Graph: The red line graphically represents the number of shootings per year, where each point on the line corresponds to the number of incidents reported in that year. This provides a visual representation of trends over time.

Data Points: Specific data points are called out on the graph, such as the one for 2021, which indicates 93 incidents. These points likely represent notable years or points of interest.

#### INSIGHTS 

**Long-term Trend**: For much of the 1980s and 1990s, the number of school shootings per year remained relatively low and consistent.

Recent Years: There is a visible and significant increase in incidents in the most recent years. Notably, the years leading up to 2021 show a sharp rise, with 93 incidents in 2021, suggesting a concerning trend in the frequency of these events.

**Inflection Points**: The graph shows some years where there are peaks or troughs, indicating years where the number of incidents notably increased or decreased compared to surrounding years. The most striking is the sharp increase at the end of the timeline.

**Interpretation**: This chart serves as a stark visual reminder of the increasing prevalence of school shootings in recent years. While the underlying causes of this increase are likely complex and multifaceted, the chart underscores the importance of addressing this issue with urgency.

**Stakeholder Impact**: The insights from this chart are invaluable for policymakers, educators, law enforcement, and communities as they seek to understand the scale of the problem and work towards comprehensive strategies to prevent school shootings.

Imagine each year as a step on a long, winding path. For years, the path was relatively level, with only a few stones to trip over—these were the school shootings of the 80s and 90s, regrettable but rare. Suddenly, in the most recent decade, the path steepens dramatically; the stones become boulders, symbolizing an alarming increase in the frequency of these tragic events. This graph is a call to action, visually representing an escalation that cannot be ignored, urging immediate and effective measures to flatten this steep climb and ensure the safety of students across the nation.

#### VISUALIZATION IDIOM

By combining bars and lines, I can display multiple variables at once

| Data: Attribute | Data: Attribute Type | Encode: Channel |
|-----------------|----------------------|-----------------|
| YEAR            | key, temporal        | horizontal position on a common scale (x-axis) |
| NUMBER OF INCIDENTS | value, quantitative | vertical position on a common scale (y-axis) |


### QUESTION 2

### 

