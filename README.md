# Project-1

This project is for the EdEx Data Visualization Bootcamp affiliated with Case Western Reserve University. There were three group members working on this project: Ian Denker, Jonathan Bateson, and Maddie Haughton. The purpose of the project was to analyze a real world data set and visualize trends. 

Our group chose to consider trends in the telemedicine usage in the United States since the onset of the COVID-19 pandemic in March of 2020. We analyzed Medicare Telehealth Trends from the Centers for Medicare & Medicaid Services. This data is found in the csv file "Medicare_Telehealth_Trends_Q1_2023.csv" in the Data folder in this repository. We downloaded this file from https://data.cms.gov/summary-statistics-on-use-and-payments/medicare-service-type-reports/medicare-telehealth-trends.

We worked collectively to clean the original dataset by reading the csv file, creating a dataframe, removing rows of empty data, and separating the data into datasets based on if it was aggregated at the national level or by individual state. Each group member then visualized the data to answer different analysis questions that we came up together at the start of our project. This analysis and visualization was done in the three separate ipynb files named "Medicare_Analysis_MH.ipynb", "Medicare_Analysis_States&Locality.ipynb", and Medicare_analysis_demo.ipynb". These notebooks are all saved in the folder called "Analysis Notebooks" in this repository. Any visualizations that we created in our notebooks are saved in the folder called "Graphs" in this repository.

Our final presentation describing the project can be found in the file "Group 1 - Telehealth Presentation.pdf".

# Question 1: 
## What effect did the onset of the 2020 pandemic have on the usage of telemedicine, and if there was an effect, have trends been sustained?

In the file "Medicare_Analysis_MH.ipynb" there are visualizations and data analysis to answer the question of if there was a change in telemedicine usage after the onset of the COVID-19 pandemic in March of 2020 and if that effect has continued. This notebook focused on the part of the dataset that was aggregated at the national level. The two populations that were visualized are "Total Telehealth-Eligible Users" and "Telehealth Users". "Total Telehealth-Eligible Users" refers to the number of Medicare beneficiaries who accessed services that are eligible for telemedicine. However, this eligibilty was determined from a list of covered services finalized in July of 2022. So, it is unclear what the trend in that population was exactly, since the services users accessed before the eligibilty list was confirmed may not have been eligible for telemedicine. "Telehealth Users" refers to Medicare beneficiaries who had telehealth vists during the year and/or quarter (including audio only and audio-video visits).

![Alt text](https://github.com/ID216135/Project-1/blob/main/Graphs/usersLine.png)

Looking at the number of medicare beneficiaries who have used telemedicine services, there was an increase in usage of telemedicine services in the second quarter of 2020 (correlating with the onset of the pandemic). Since then, the general trend has been a decrease in telemedicine users. However, the number of Medicare beneficiaries who use telemedicine services remains higher in 2023 than before the onset of the COVID-19 pandemic.

![Alt text](https://github.com/ID216135/Project-1/blob/main/Graphs/usersBar.png)

When looking at the data by year alone, rather than by year and by quarter, one can see a decreasing trend in number of telehealth users and number of telehealth-eligible users. There is a trend of a decreasing number of telehealth-eligible users as well, however it has not been as significant of a decrease as in the number of telehealth users. Again, the trend in telehealth-eligible users may not be an accurate representation of services which were eligible for telemedicine since the list of covered telehealth services was effective as of July 2022.

# Question 2:

## What was the breakdown in telemedicine usage by demographic factors?

Looking at the demographic data, we can draw a few conclusions. It is clear the eligible users under 64 used telemedicine the most since 2020. As for sex, females used telemedicine more than males by 6%. Finally, when it comes to race, Hispanic people had the highest percentage of usage among eligible users.

There was also a clear difference in usage by a recipient's locality, i.e. whether they lived in a rural or urban area. 58% of the total telehealth users were residing in urban areas, which does not, by itself, show a difference, as there may be more urban users overall.



However, when looking at each population as a subset, rural recipients were far less likely to make use of telemedicine services, with a lower usage rate within their group at every timepoint. The gap was closest prior to the pandemic, with only a 1.7% difference in usage. however, after the pandemic hit in Q2 2020, the gap was consistently at least 4.4%, with a peak difference of 11.2%. The difference in usage has been shrinking since the onset of the pandemic, but remains at least several percentage points tall.

![Alt text](https://github.com/ID216135/Project-1/blob/main/Graphs/Urban_v_Rural_Line.png)
![image](https://github.com/ID216135/Project-1/assets/143837858/1966fd25-1783-4b1c-990f-24c2efe723d4)
![image](https://github.com/ID216135/Project-1/assets/143837858/5d4fddbc-9826-4bef-acd6-1732104cacc8)
![image](https://github.com/ID216135/Project-1/assets/143837858/5e4bde5f-9479-4963-a9d2-b1aee4ca7f4f)
![image](https://github.com/ID216135/Project-1/assets/143837858/692765b5-433c-4fb8-8168-1ae32de9b229)


# Question 3: 
## Does Telemedicine Usage Vary Significantly by State?

In the file "Medicare_Analysis_States&Locality.ipynb", we analyzed the data based on state and locality. There was a clear difference in telemedicine usage by state. States like California and Massachussetts have a much greater proportion of their population use telemedicine than states like Nebraska and North Dakota, on average.

![Alt text](https://github.com/ID216135/Project-1/blob/main/Graphs/Mean%20Telehealth%20Usage%20by%20State.png)

Additionally, the change in telemedicine usage from Q1 to Q2 2020 was also highly variable by state, with some states like Monatana only increasing by 22 percentage points, while others, like Massachussetts, increased by 60 percentage points. 

![Alt text](https://github.com/ID216135/Project-1/blob/main/Graphs/Change%20in%20Peak%20Telehealth%20Usage%20by%20State.png)

There was a very tight correlation between a state's usage prior to the pandemic and their usage after the pandemic's onset, with an r-value of 0.898.

![Alt text](https://github.com/ID216135/Project-1/blob/main/Graphs/Scatter_Plot.png)

Additionally, a state's usage prior to the pandemic was very highly correlated with their average usage from 2020 to 2023, with an r-value of 0.843.

![Alt text](https://github.com/ID216135/Project-1/blob/main/Graphs/Scatter_Plot_2.png)
