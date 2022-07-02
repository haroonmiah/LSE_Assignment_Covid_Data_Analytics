# LSE_Assignment_Covid_Data_Analytics
The UK government is boosting its efforts to increase vaccination rates through marketing campaigns to promote the COVID vaccine. In this assignment, you’ll use Python to analyse a data set in order to help inform the UK government about COVID-19 vaccinations.

After loading the data into Python and creating the data frames (cov and vac), I found that the, ‘covid_19_uk_cases.csv’ file contained 7584 rows and 12 columns. Two rows had NA’s or missing data, both belonging to the ‘Province/State’ Bermuda. 

The ‘covid_19_uk_vaccinations.csv’ file contained 7584 rows and 11 columns. There were no NA’s. 

The 2 DataFrames do not have a default index. After sorting the cov DataFrame by ‘Date’ (cov.sort_values('Date')), I could see that the number of covid cases increases from the beginning (22/01/2020) all the way to the end (14/10/2021), however, it fluctuates and so it would be nice to be able to visualise this data with a line chart to see the changes over time. A similar observation can be made with the vaccination numbers.  The recovered data stops from August 2021; is this an error? On their own, the descriptive statistics will not be very meaningful; what would help is to compare the results with other State’s in the DataFrames and see how they compare. We can then try to interpret, based on the mean, for example, do states that have a higher mean vaccination lead to fewer hospitalisations or deaths?

The numerical data for Gibraltar seem to suggest the numbers are inflated. For example, the sum of the ‘Vaccinated’ is 5,606,041; Gibraltar’s population in 2020 was only 33,691, so how can the total vaccinated exceed this number? The sum for ‘Cases’ (1,413,853), ‘Recovered’ (956,103) and ‘Hospitalised’ (649,459) also exceed the population of Gibraltar. Where is the data from and is it reliable? 

The State that has received the highest number of First Dose is Gibraltar, although the State that has the highest percentage who have received the first dose but not the second dose is, ‘Saint Helena, Ascension and Tristan da Cunha’.  

The number of individuals who have received the vaccine has increased in time as we can see that the number vaccinated in 2020 was zero and the sum that received the First Dose in 2021 is 46,966,364.
 
We are now in a position to visualise the data using plots. Using the Gibraltar subset, I used the melt() function to transform the data to be able to visualize the ‘Cases’, ‘Recovered’, ‘Hospitalised’ and ‘Deaths’.

This clearly shows what was mentioned earlier about irregularities with the dataset; how can hospitalised cases be higher than the number of Covid cases at any given timepoint? There is a steep drop in the number of recovered cases at one point; shouldn’t the number of deaths increase at around the same time? 

Calculating the percentage of people who are partially and fully vaccinated showed the same trend for all State’s; fully vaccinated is 95.49% for all States. This again makes me question the integrity of the data as if the percentage of fully vaccinated is so high, the Government would not be so worried about boosting its efforts to increase vaccination rates through marketing campaigns to promote the COVID vaccine.

Whilst initially visualising the lineplot for deaths grouped by Province/State over time, the plot was not showing correctly:

By aggregating the deaths, I was able to identify the State that skewed the plot; ‘Others’. 

Once I removed this State, the plot was showing up as I would expect it to:
 
However, as the x-axis used the exact dates, the lines were not as smooth. By converting the dates to months/year, I was able to further improve on this visualisation:

This line plot shows that the death rates are increasing for all States and it doesn’t seem to have reached the peak yet. This is worrying if you consider that the fully vaccinated percentage is so high for all States. 

Recovered cases are increasing over time for all States but then all of a sudden there is an abrupt drop for all regions; is there data missing from July 2021 onwards?
 
In any case, the lineplot shows that the Channel Islands had the highest number of recovered over time, with Gibraltar briefly overtaking them from January 2021 to June 2021.

Whilst there are questions raised over the integrity and completeness of the dataset that we are using, there is no doubt that the visualisations created help to easily convey the trends of deaths, recoveries etc over time and these can be used by the government to create the stories to direct their campaigns. 

