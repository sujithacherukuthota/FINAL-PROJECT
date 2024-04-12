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

-'Handling Missing Values': Recognizing the importance of complete records, I addressed the missing values in 'number_news' by filling them with the column's mean, ensuring numerical consistency. I chose to remove any entries lacking essential data in the 'date' or 'state' columns, as these are vital for my temporal and geographical analyses.
Data Type Correction: I converted the 'date' column to the datetime type to facilitate time-based analysis. Additionally, I transformed other columns that were incorrectly categorized as strings into numeric data types, setting non-convertible values as NaNs to maintain data integrity.
Text Standardization: To avoid case sensitivity issues, especially with string data, I standardized the 'state' column by converting all entries to uppercase. This ensures uniformity and prevents misclassification due to text format discrepancies.
Duplicate Removal: In my pursuit of data accuracy, I removed any rows that were exact duplicates, thereby preventing data redundancy from skewing the results of the analysis.
Irrelevant or Incorrect Data Handling: I eliminated entries with future dates and those with illogical negative values in 'number_news'. Such entries are likely to be data entry errors and could distort the findings of my study.

