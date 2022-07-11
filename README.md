# LSE_Assignment_Covid_Data_Analytics
The UK government is boosting its efforts to increase vaccination rates through marketing campaigns to promote the COVID vaccine. In this assignment, you’ll use Python to analyse a data set in order to help inform the UK government about COVID-19 vaccinations.

The 2 main datasets provided, contain information for 12 States/Provinces. There are only 2 rows with missing data overall. 

Figure 1

Figure 2

The covid cases increases from the beginning (22/01/2020) all the way to the end (14/10/2021), however, it fluctuates and so it would be nice to be able to visualise this data with a line chart to see the changes over time. The recovered data stops from August 2021; is this an error? On their own, the descriptive statistics will not be very meaningful; what would help is to compare the results with other State’s in the DataFrames and see how they compare. 

The numerical data for Gibraltar seem to suggest the numbers are inflated. For example, the ‘Vaccinated’ sum is 5,606,041; Gibraltar’s population in 2020 was only 33,691, so how can the total vaccinated exceed this number? The sum for ‘Cases’, ‘Recovered’ and ‘Hospitalised’ also exceed the population of Gibraltar. Where is the data from and is it reliable? 

Figure 3
Figure 4

After merging the 2 datasets together, we are able to view all the vaccination and covid data all in one data frame. The State that has received the highest number of First Doses is Gibraltar, although the State that has the highest percentage who have received the first dose but not the second dose is, ‘Saint Helena, Ascension and Tristan da Cunha’ and so this could be a State for the government to target to boost fully vaccinated numbers.  

Figure 5
Figure 6

I grouped the date by month and aggregated the data to show the sum for each variable:

Figure 7

This shows us that the number of vaccinated individuals goes up from Jan 2021 to May 2021 but then we see a fall thereafter. With the first dose numbers, there are fluctuations throughout the entire timeframe but in general we see that there is a decline in the numbers being vaccinated towards the end of time. We can also note that, around April/May 2021 there are drops in the number of hospitalised in the corresponding months (April to June 2021); this could be due to the positive effects of the vaccine and so fewer people required hospitalisations. 

Using the Gibraltar subset, I used the melt() function to transform the data to be able to visualize the ‘Cases’, ‘Recovered’, ‘Hospitalised’ and ‘Deaths’ over time.

Figure 8

This clearly shows what was mentioned earlier about irregularities with the dataset; how can hospitalised cases be higher than the number of Covid cases at any given timepoint? There is a steep drop in the number of recovered cases at one point; shouldn’t the number of deaths increase at around the same time? 

Calculating the percentage of people who are partially and fully vaccinated showed the same trend; fully vaccinated is 95.49% for all States. This again makes me question the integrity of the data; if the percentage of fully vaccinated is so high, the Government would not be working to boost its efforts to increase vaccination rates through marketing.

Figure 9
Figure 10

Whilst initially visualising the line plot for deaths grouped by Province/State over time, the plot was not showing correctly:

Figure 11

Aggregating the deaths, I was able to identify the State that skewed the plot; ‘Others’. 

Figure 12

Once I removed this State, the plot was showing up as I would expect it to:

Figure 13

By converting the dates to months/year, I was able to further improve on this visualisation:

Figure 14

This line plot shows that the death rates are increasing for all States and it doesn’t seem to have reached the peak yet but starting to plateau. In addition, the deaths seem particularly low for some States; Falkland Islands has zero deaths, which doesn’t seem correct and may need to be investigated. The States with the highest deaths are Channel Islands and Gibraltar.

Figure 15
Figure 16

The Channel Islands had the highest number of recovered individuals over time, with Gibraltar briefly overtaking them from January 2021 to June 2021. Taking this information into consideration, the government could look to focus their vaccination drive at other regions where the recoveries is not so high (Figure 16). 
After importing the ‘Tweets’ data into Python, I was able to identify the hashtags that were mentioned the most and visualise these as a bar plot:

Figure 17

#COVID19, #CovidIsNotOver and #China were the most common hashtags. This shows us our serious of a concern Covid was. You can see in the visualisation that 2 countries are in the plot; China and Greece. This is likely due to people tweeting about high covid cases in those countries at the time although we should investigate if these tweets are actually referring to covid.

Figure 18

Despite the concerns relating to the reliability of the data, which should be investigated further, we were able to draw some interesting trends and insights from the data that we have to hand. I found that the number of vaccinations is going down, after an initial increase. We have identified the States that have the highest percentage in terms receiving the first dose but not the second dose; these States are an easy target for the government in the first instance to boost vaccination numbers.  

Lineplots helped to visualise the trends for all the States over time in terms of deaths and recoveries. I found that the deaths were increasing for all States and for some it looked as though the peak hadn’t been reached yet. With regards to recoveries, I found that this was also increasing over time and I was able to identify the States with the highest recoveries and so these States could be targeted at a later stage by the government when looking to boost vaccinations, focusing initially at the States with lower recovery numbers. A visualisation that will help in boosting the vaccination rates is a scatterplot to show the relationship between vaccination and hospitalisation; this shows that as the number of vaccinations increases, the hospitalised numbers fall (figure 19). This is important as it helps to portray the positive effect of vaccines and in turn it will help reduce the burden on the NHS; this’ll be a big plus point for the government. 

To further the analysis, it would be useful to have population data available for all States. This would help us to interpret which State’s actually had the best/worst vaccination uptake rates and also how serious the covid rates (deaths, hospitalisations, recovered) were. 

Figure 19















