# SEMESTER PROJECT

### CS 625 Spring 2024

### Sujitha Cherukuthota

### April 9

# SHOOTING INCIDENTS IN SCHOOLS 

## DATASET

Data Source URL : [Link](https://www.chds.us/sssc/data-map/)

#### ABOUT DATASET 

Certainly, let's start by providing an overview of the dataset and then move on to describe the sheets and the columns within the 'Incidents' sheet.

---

**Dataset Overview**

This dataset provides a comprehensive view of school shooting incidents in the United States. It is intended to give educators, policymakers, and academics with thorough information for analyzing the trends, circumstances, and results of these unfortunate incidents.


**Sheets in the Dataset**

The dataset is organized into multiple sheets, each containing specific aspects of school shooting data:
- Incidents    : Detailed records of each shooting incident.
- Victim       : Information about individuals affected by the shootings.
- Shooter      : Data related to the individuals who carried out the shootings.
- Weapons      : Details about the firearms used in the incidents.

**Columns in the 'Incidents' Sheet**

- incident_id     : A unique identifier for each incident.
  
- sources         : References to data sources where information about the incident was obtained.
- number_news     : The count of news reports covering the incident.
- media_attention : Qualitative assessment of the media coverage intensity.
- reliability     : A rating of the information reliability for the incident details.
- date            : The date when the incident occurred.
- quarter         : The fiscal quarter within which the incident took place.
- school          : The name of the school where the incident occurred.
- city            : The city in which the school is located.
- state           : The state in which the school is located.
- school_level    : The education level of the school (e.g., Elementary, Middle, High).
- location        : Specific location at the school where the incident took place.
- location_type   : Classification of the location (e.g., classroom, cafeteria).
- during_school   : Indicates whether the incident happened during school hours.
- time_period     : The time period during the day when the incident occurred.
- first_shot      : Location where the first shot was fired.
- summary         : A brief account of the incident.
- narrative       : A detailed narrative description of the incident.
- situation       : The situation or context in which the shooting occurred.
- targets         : Individuals or groups targeted in the incident.
- accomplice      : Information on whether the shooter had accomplices.
- hostages        : Indicates whether hostages were taken during the incident.
- barricade       : Specifies if a barricade situation occurred.
- officer_involved: Involvement of law enforcement officers in the incident.
- bullied         : Information regarding whether bullying was a factor in the incident.
- domestic_violence: Indicates a domestic violence connection to the incident.
- gang_related    : Signifies whether the incident was related to gang activity.
- preplanned      : Denotes if the incident was premeditated.
- shots_fire      : The estimated number of shots fired during the incident.
- active_shooter_fbi : Classification of the incident as an active shooter situation by the FBI.

#### WHY THIS DATASET?

I selected this dataset because it offers a valuable collection of information that is essential to comprehending school shootings in the US. In order to contribute to prevention efforts, my goal is to thoroughly examine patterns, contributing factors, and the aftermath of such situations. This data offers the breadth and depth required for a meaningful analysis, as it spans a long time span in addition to being rich in detail.


## STAKE HOLDER
Policymakers are the dataset's primary stakeholders.  They can use the analysis to better understand the prevalence, causes, and consequences of school shootings. This understanding is critical for developing legislation, allocating money for mental health care, improving school security protocols, and implementing educational programs that foster a culture of nonviolence. The ultimate goal for these stakeholders is to use data to protect students and educators while also ensuring that schools are safe places to learn and thrive.

For policymakers, the conclusions of this dataset have far-reaching consequences. The effectiveness of laws and regulations can be tested against data, ensuring that activities are both reactive and preventive. This can have a significant real-world impact, potentially saving lives and producing more secure future for the coming generations.


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


<img src="https://github.com/sujithacherukuthota/FINAL-PROJECT/blob/main/F11.png" width="700" height="500">

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

### What underlying factors are most prevalent in school shooting incidents, and how do these contributing elements vary in their impact on the occurrence of such tragic events?"


<img src="https://github.com/sujithacherukuthota/FINAL-PROJECT/blob/main/F22.png" width="700" height="500">


X-Axis (Horizontal):

Label: “% of All School Shootings”
Scale: Appears to be linear, representing the percentage distribution of incidents across different factors.
Data: Reflects the proportion of school shootings associated with each listed factor.

Y-Axis (Vertical):

Label: There is no explicit label, but it lists factors that led to shootings.
Categories: Different factors such as "Escalation of Dispute," "Drive-by Shooting," "Illegal Activity," etc.
Data: Categorical data indicating the nature of each incident.

Each bar represents the percentage of school shootings attributable to the factor listed on the y-axis.
The length of the bar corresponds to the frequency percentage.

The color scheme differentiates between factors with a higher impact (red) and factors with a lesser impact (green), offering visual guidance on their relative significance.

Tooltip: When hovering over a bar, a tooltip appears showing specific data, like incident_id=19 and situation=Accidental, suggesting an interactive element that provides more detail on demand.

#### INSIGHTS 

The chart  "Primary Factors that Led to the Shooting" is  a compelling visualization of the triggers behind school shootings. The stark contrast in colors between high-impact and low-impact factors draws immediate attention to "Escalation of Dispute," the predominant cause. This insight alone is a clarion call for conflict resolution programs within schools. Interventions that focus on de-escalation could be instrumental in curbing the incidence of violence.

Drive-by shootings, usually associated with gang violence or external disputes spilling onto school grounds, stand out as the second most common factor. This suggests that some school shootings are a reflection of broader societal issues rather than isolated school-based problems. It raises important questions about community safety and the need for comprehensive strategies that extend beyond school premises.

Illegal activities, which are just as prominent as accidental shootings, underscore the intertwining of schools with the legal challenges facing the community. These activities might range from drug-related issues to possession of firearms, indicating a potential for preventive measures through law enforcement and education.

The lower end of the scale, marked in green, covers factors such as bullying, officer-involved shootings, and mental health crises (indicated by 'Psychosis'). While these factors account for a smaller percentage of incidents, they are no less critical. Each incident represents a failure to protect students and staff, highlighting gaps in mental health support, bullying prevention, and the role of law enforcement in educational settings.

Moreover, the interactive aspect of the graph, revealing details upon hover, not only personalizes the data but also reminds us that behind every statistic is a story, a community impacted, and lives changed.

This chart doesn't just paint a picture of past tragedies; it offers a blueprint for prevention. Stakeholders could use these insights to prioritize funding, target interventions, and craft policies that tackle the most prevalent factors, perhaps mitigating future incidents before they occur. It's a data-driven starting point for crucial conversations about safety, mental health, and the well-being of young learners in our nation's schools.

#### VISUALIZATION IDIOM

| Data: Attribute             | Data: Attribute Type | Encode: Channel           |
|-----------------------------|----------------------|---------------------------|
| Primary Factors             | Categorical         | Y-axis (vertical position)|
| Percentage of Incidents     | Quantitative        | X-axis (length of bar)    |


## FURTHER ANALYSIS 

### States Under the Microscope: A Comparative Analysis of School Shooting Incidents


<img src="https://github.com/sujithacherukuthota/FINAL-PROJECT/blob/main/top%2010%20states.png" width="700" height="500">


The bar chart highlights the disparity in school shooting incidents across the U.S., with California, Texas, and Florida reporting the highest numbers. This visualization underscores the national scope of the issue, with the top ten states showcasing significant counts, necessitating proactive measures and policy reforms to enhance school safety. It's a nationwide call to action for stakeholders to delve into causative factors and strengthen preventive strategies.


### States with Minimal School Shooting Occurrences

<img src="https://github.com/sujithacherukuthota/FINAL-PROJECT/blob/main/least%2010.png" width="700" height="500">

orizontal Axis (X-Axis): Displays the states, categorized by their geographical designation.
Vertical Axis (Y-Axis): Represents the number of school shooting incidents recorded.

The graph provides a revealing perspective on the states with the fewest school shootings, a significant contrast to the more prevalent instances in other states. It may point towards effective preventive measures, stringent gun laws, or lower risk factors in these regions. This analysis can serve as a reference for stakeholders aiming to understand the effectiveness of various strategies in minimizing such incidents. The visualization invites a deeper analysis into the socio-economic and legal frameworks of these states that could be contributing to these lower numbers.
Stakeholders like policymakers and educational authorities can use this data to identify and emulate effective safety strategies in states with higher incident rates.


### Evolving Risk Patterns: A Decadal Snapshot of School Shooting Frequencies by Educational Tier"

<img src="https://github.com/sujithacherukuthota/FINAL-PROJECT/blob/main/school%20level%20vs%20year.png" width="700" height="500">

The data visualization offers a longitudinal analysis of school shooting occurrences broken down by educational tiers, revealing significant patterns over the years. The graph's timeline underscores decades of relative consistency, with incidents occurring sporadically across various school levels, but a striking and disturbing surge in incidents at high schools in recent years stands out. This sudden rise poses critical questions about the underlying causes, ranging from socio-economic stressors to changes in school environment dynamics or societal issues impacting youth. The marked increase necessitates a deep dive into high school environments to understand and address the drivers of such trends.

The graph also accentuates the contrast between high school incidents and those at other educational levels, such as elementary, middle, junior high, and combined-grade schools like K-8 and K-12. Although there is a visible uptick across the board, the frequency and intensity of events in high schools demand urgent attention.


### Dissecting the Gender Disparity: Victim Profile Analysis in School Shooting

<img src="https://github.com/sujithacherukuthota/FINAL-PROJECT/blob/main/male%20vs%20female.png" width="700" height="500">

The x-axis represents the primary factors leading to school shooting incidents, offering a categorical breakdown of the events.
The y-axis quantifies the number of victims, providing a comparison between male and female individuals affected by these tragedies.

This graph starkly illustrates the gender disparity among victims of school shootings, segmented by the precipitating factors of each event. The peak in male victims during drive-by shootings and indiscriminate shootings suggests a potential gender bias in targeting or perhaps a higher likelihood of males being present or involved in such situations.

However, the disparity is not consistent across all categories. In some instances, such as domestic situations with a targeted victim, the number of male and female victims is closer. This could imply that domestic circumstances that escalate to violence at schools affect genders more equally.

The overall trend implies a multifaceted issue where gender dynamics intersect with the motives and contexts of school shootings. Such insights are essential for stakeholders developing gender-sensitive preventative measures, support systems, and post-incident protocols.


### Decoding the Calendar: Seasonal and Annual Rhythms in School Shootings 

<img src="https://github.com/sujithacherukuthota/FINAL-PROJECT/blob/main/dashboard%20111.png" width="700" height="500">

The x-axis on the top graph represents the progression of years, providing a timeline for the incidents' occurrence.

The y-axis on the top graph indicates the number of incidents, offering insight into the frequency of occurrences over time.

The x-axis on the bottom graph displays the months of the year, hinting at potential seasonal patterns in the incidents.

The y-axis on the bottom graph shows the number of incidents, similarly offering insight into the frequency of occurrences but on a monthly basis.

This dual graph offers a compelling visualization of school shootings across different time scales. The top graph's sharp upward trend in recent years raises alarm, indicating a surge in such tragic events. It serves as a stark reminder of the escalating nature of the issue at hand.

The bottom graph sheds light on the monthly distribution, suggesting a seasonal pattern to these occurrences. There are noticeable spikes in certain months, which may correlate with the academic calendar and associated stressors, times of celebration, or specific societal events.

These patterns  provide valuable information for stakeholders like educational institutions, law enforcement, and mental health professionals, as they seek to bolster preventive measures during higher-risk periods.

For example, law enforcement could increase surveillance and presence during peak months, while schools might focus on conflict resolution programs or mental health support. Mental health professionals could advocate for more resources or campaigns during these times.

The slider at the bottom suggests the capability to drill down into specific months, offering even finer granularity that could lead to more targeted interventions and policies.


### Distribution of Shooting Incidents Across Different School Areas

<img src="https://github.com/sujithacherukuthota/FINAL-PROJECT/blob/main/location.png" width="700" height="500">


X-axis: "Location Type"
Y-axis: "Number of Incidents"


The majority of incidents occur within school buildings, indicating that schools are primary targets.
Incidents on school property but outside buildings are less frequent, suggesting that indoor areas are more at risk.

Incidents involving both inside and outside locations, as well as on school buses, are relatively rare, possibly due to the transient nature and better supervision in these areas.
Understanding the location distribution of these incidents can help stakeholders, such as school administrators and policymakers, to improve safety protocols where they are needed most and allocate resources more effectively to prevent such tragedies.


### Variability and Distribution of News Reports on School Shootings by Educational Stage

<img src="https://github.com/sujithacherukuthota/FINAL-PROJECT/blob/main/voilin%20plot'.png" width="700" height="500">

X-Axis: "School Level"
Y-Axis: "Number of News Reports"


The chart provides a visualization of how media coverage varies by school level.
High schools and elementary schools have a broader distribution and a higher number of reports, indicating more media focus, possibly due to the severity or the impact of incidents at these levels.

Other school levels like middle, junior high, and K-8 exhibit a narrower spread and fewer reports, suggesting less frequent or less covered incidents.
The length and width of each ‘violin’ indicate the range and the frequency of reports, with wider sections representing a higher occurrence of a specific number of reports.

### Interplay of Time and Place in School Shooting Episodes

<img src="https://github.com/sujithacherukuthota/FINAL-PROJECT/blob/main/stacked%20bar.png" width="700" height="500">

X-Axis: "Location Type" - categorizes the places where incidents occurred, such as inside school buildings or on school property.
Y-Axis: "Number of Incidents" - quantifies the count of incidents.


The stacked layers of the bars illustrate the prevalence of incidents at different times of the day for each location type.
For example, the highest stack, presumably for "Outside on School Property", suggests a significant portion of incidents occur during dismissal, followed by events and other labeled timeframes.

The chart indicates that certain times of day, like "Evening" or "Lunch", are more prone to incidents in specific locations.
This information can be pivotal for school administrators and security personnel in planning and prioritizing safety measures and resource allocation during vulnerable periods.

For policymakers, the data could underscore the need for tailored strategies for incident prevention that take into account the dynamics of time and place in school environments


### Impact Severity: Average Victims in School Shooting Scenarios

<img src="https://github.com/sujithacherukuthota/FINAL-PROJECT/blob/main/number%20of%20victims.png" width="700" height="500">

X-Axis: "Situation" - categorizes the context or situation during which the shooting took place, such as "Indiscriminate Shooting" or "Hostage/Standoff."

Y-Axis: "Average Number of Victims" - represents the mean count of victims involved in the shootings within each categorized situation.

The line chart illustrates that indiscriminate shootings tend to have the highest average number of victims, highlighting their particularly devastating impact.
Situations labeled as "Hostage/Standoff" and racially motivated shootings, while less frequent, also show a higher average victim count, indicating these situations are significantly severe when they do occur.

Other contexts, such as bullying or drive-by shootings, present lower average victim numbers but are still critical areas for intervention.

Understanding these patterns is essential for law enforcement, educators, and policymakers to develop focused preventative measures and crisis response plans.
The data informs stakeholders about the critical need for interventions tailored to the nature of the incident to mitigate impact effectively.

### ADDITIIONAL RESEARCH 

#### Comparative Analysis of School Shooting Incidences: A Global Perspective

<img src="https://github.com/sujithacherukuthota/FINAL-PROJECT/blob/main/pie%20chart.png" width="700" height="500">


In our research, we sought to compare the incidence of school shootings across different countries to glean insights into the relative frequency of such events on an international scale. The data utilized for this comparison was drawn from multiple sources that track incidents of gun violence, specifically within educational institutions. Our methodology involved compiling reported instances of school shootings and normalizing these numbers by country to understand their distribution.

The pie chart illustrates the stark disparity between the United States and other nations regarding school shootings. The U.S. accounts for a substantial majority, indicated by the overwhelming blue segment at 91.4%, highlighting the disproportionate frequency of such tragic events in comparison to the rest of the world. Mexico, South Africa, Pakistan, Nigeria, and a collective of other countries make up the remainder, each represented by smaller slices of the chart.

<img src="https://github.com/sujithacherukuthota/FINAL-PROJECT/blob/main/countries.png" width="700" height="500">

#### International Firearm Homicide Rates: Unpacking the Numbers

This bar chart presents a comparative analysis of firearm homicide rates per 100,000 population across a range of countries. The data underscores a significant disparity, with the United States showing a notably higher rate of 4.52 deaths per 100,000 population, which is markedly above other countries listed. Saudi Arabia and Chile follow, yet with considerably lower figures at 1.46 and 1.2, respectively. The trend continues to taper off as we move down the list towards countries like Germany, Poland, Taiwan, and ultimately Japan, which reports a rate of zero.

The graph provides an incisive look into how gun-related homicides are not merely a matter of gun prevalence but are influenced by a matrix of factors including gun control policies, enforcement rigor, social welfare, cultural attitudes towards conflict resolution, and the overall socio-political climate. 

Countries with lower rates, such as Japan and the United Kingdom, often have stringent gun control laws coupled with strong societal norms against gun ownership. Conversely, the United States' high rate can be partially attributed to its unique constitutional rights, cultural factors, and the varying strictness of gun laws across states.

The insight drawn from this graph could be crucial for policymakers and researchers aiming to understand the impact of firearm regulation and societal factors on gun violence. It highlights a potential correlation between gun control measures and reduced firearm-related homicides, suggesting that policies and cultural attitudes towards firearms have a tangible effect on reducing such incidents.





## MY RECOMMENDATIONS FOR STAKE HOLDER 

Reflecting on our extensive analysis of school shooting incidents, we distill our findings into specific actionable insights for our chosen stakeholders, the policymakers:

**Final Thoughts for Policymakers:**

- **Proactive Educational Policies:** The data underscore the necessity for integrating behavioral and mental health education within school curricula, particularly in high-risk states. Policies encouraging early intervention could be vital in preempting potential incidents.
  
- **Safety Protocols and Drills:** There's a clear pattern to the timing of school shootings, which often coincide with the start or end of the school day. Policymakers should advocate for mandatory safety drills that reflect these patterns, ensuring that both students and staff are prepared for such eventualities.

- **Resource Allocation:** The varying frequency of incidents across states suggests the need for a nuanced approach to resource allocation. States with higher incidences may require more funding for school safety measures and mental health resources.

- **Community Engagement:** Policymakers can use these insights to foster community engagement programs, ensuring that the nuances of each incident type—whether bullying, disputes, or other factors—are addressed within local contexts.

- **Legislative Action:** There's an opportunity to draft legislation that supports mental health initiatives and conflict resolution programs in schools, with the potential to deter the pathways leading to school shootings.

**Implications and Implementations:**

Policymakers have the advantage of accessing a consolidated body of data that reveals patterns and risk factors associated with school shootings. By leveraging this data, they can:

- Draft targeted policies that address the specific needs and trends observed, such as the most affected school levels and the times when incidents are most likely to occur.
- Collaborate with educational bodies to ensure the development of a supportive and responsive school culture that can prevent the circumstances leading to shootings.
- Use the insights as a foundation for building consensus around legislation that aims to enhance the safety and well-being of students.
-  Fund programs for early detection and intervention of at-risk youth.
- Ensure consistent nationwide practices for safety drills and emergency response.
- Allocate resources for states identified as high-risk to reinforce their educational and security infrastructure.



## FINAL THOUGHTS

**Through various visualizations, we have observed a disturbing increase in the number of incidents over recent years, with a marked rise in the last decade, signaling an urgent need for intervention and policy response.**

**The data has also revealed that certain states, such as California, Texas, and Florida, have experienced a higher frequency of these tragic events. This geographic concentration might suggest the influence of regional factors and calls for tailored preventative strategies.**

**When dissecting the incidents by school level, it becomes apparent that high schools have been disproportionately affected, which could reflect the social dynamics and developmental challenges specific to that age group. However, the presence of such incidents across all educational levels, from elementary to junior high, is a stark reminder that no segment of the school population is immune.**

**Another poignant insight comes from the gender distribution of victims where, in many types of incidents, male victims outnumber female victims. It's a reflection that could spur discussions around gender-related social issues and security measures in educational environments.**

**The analysis of incident causes paints a complex picture of the motivations behind these shootings, ranging from personal disputes to bullying. Each cause, no less tragic than the others, prompts us to consider the underlying societal and psychological factors at play.**

**The interactive maps and the granular data on the time and location of incidents highlight potential patterns in when and where school shootings are more likely to occur, offering a pathway for focused security enhancements.**

 
### REFERENCES 

[REFERENCE 1](https://www.healthdata.org/news-events/insights-blog/acting-data/gun-violence-united-states-outlier)

[REFERENCE 2](https://k12ssdb.org/data-visualizations)

[REFERENCE 3](https://visme.co/blog/best-data-visualizations)

[REFERENCE 4](https://hex.tech/blog/how-to-build-a-dashboard-in-python//)
