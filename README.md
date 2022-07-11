# LSE_Assignment_Covid_Data_Analytics
The UK government is boosting its efforts to increase vaccination rates through marketing campaigns to promote the COVID vaccine. In this assignment, you’ll use Python to analyse a data set in order to help inform the UK government about COVID-19 vaccinations.

The 2 main datasets provided, contain information for 12 States/Provinces. There are only 2 rows with missing data overall. 

![alt text](https://github.com/haroonmiah/LSE_Assignment_Covid_Data_Analytics/blob/54efdb6dc7e7b3b37e565367a65633ea208029a0/Assignment%202%20figures/Fig_1.png)

Figure 1: Determining the Data types in the DataFrame and number of rows and columns

![alt text](https://github.com/haroonmiah/LSE_Assignment_Covid_Data_Analytics/blob/3474af80056781f4579d0967c71bd97c4e5e6b8a/Assignment%202%20figures/Fig_2.png)

Figure 2: Determining the number of missing values.

the numerical data seems to have issues. Really high numbers for everything

The numerical data for Gibraltar seem to suggest the numbers are inflated. For example, the ‘Vaccinated’ sum is 5,606,041; Gibraltar’s population in 2020 was only 33,691, so how can the total vaccinated exceed this number? The sum for ‘Cases’, ‘Recovered’ and ‘Hospitalised’ also exceed the population of Gibraltar. Where is the data from and is it reliable? 

![alt text](https://github.com/haroonmiah/LSE_Assignment_Covid_Data_Analytics/blob/5b574e80d9f52aec7058c6edad81f3bacd07e92f/Assignment%202%20figures/Fig_3.png)

Figure 3: Running the descriptive statistics and sum functions on Gibraltar_num DataFrame

![alt text](https://github.com/haroonmiah/LSE_Assignment_Covid_Data_Analytics/blob/f9c2252bec7a8dbd8724400450976d15a2740dd3/Assignment%202%20figures/Fig_4.png)
Figure 4: Running the descriptive statistics on Gibraltar_vac_num DataFrame

The State that has received the highest number of First Doses is Gibraltar, although the State that has the highest percentage who have received the first dose but not the second dose is, ‘Saint Helena, Ascension and Tristan da Cunha’.

![alt text](https://github.com/haroonmiah/LSE_Assignment_Covid_Data_Analytics/blob/f9c2252bec7a8dbd8724400450976d15a2740dd3/Assignment%202%20figures/Fig_5.png)
Figure 5: Grouped data by Province/State to show highest number of individuals with First Dose

![alt text](https://github.com/haroonmiah/LSE_Assignment_Covid_Data_Analytics/blob/f9c2252bec7a8dbd8724400450976d15a2740dd3/Assignment%202%20figures/Fig_6.png)
Figure 6: Grouped data by Province/State to show highest percentage to not receive Second Dose after receiving First Dose

I grouped the date by month and aggregated the data to show the sum for each variable:

![alt text](https://github.com/haroonmiah/LSE_Assignment_Covid_Data_Analytics/blob/f9c2252bec7a8dbd8724400450976d15a2740dd3/Assignment%202%20figures/Fig_7.png)

Figure 7: Table to show data grouped by month with sum for each variable.

vaccinated number goes up from Jan 2021 to May 2021 but then we see a fall thereafter. 

Using the Gibraltar subset, I used the melt() function to transform the data to be able to visualize the ‘Cases’, ‘Recovered’, ‘Hospitalised’ and ‘Deaths’ over time.

![alt text](https://github.com/haroonmiah/LSE_Assignment_Covid_Data_Analytics/blob/f9c2252bec7a8dbd8724400450976d15a2740dd3/Assignment%202%20figures/Fig_8.png)

Figure 8: Plot to show Cases, Recovered, Hospitalised and Deaths for Gibraltar over time

This clearly shows what was mentioned earlier about irregularities with the dataset

Calculating the percentage of people who are partially and fully vaccinated showed the same trend; fully vaccinated is 95.49% for all States. 

![alt text](https://github.com/haroonmiah/LSE_Assignment_Covid_Data_Analytics/blob/f9c2252bec7a8dbd8724400450976d15a2740dd3/Assignment%202%20figures/Fig_9.png)

Figure 9: Stacked Bar Plot to show percentage of vaccinated and partially vaccinated for each State.

![alt text](https://github.com/haroonmiah/LSE_Assignment_Covid_Data_Analytics/blob/f9c2252bec7a8dbd8724400450976d15a2740dd3/Assignment%202%20figures/Fig_10.png)

Figure 10: Bar Plot to show number of vaccinated and partially vaccinated cases for each State.

Whilst initially visualising the line plot for deaths grouped by Province/State over time, the plot was not showing correctly:

![alt text](https://github.com/haroonmiah/LSE_Assignment_Covid_Data_Analytics/blob/f9c2252bec7a8dbd8724400450976d15a2740dd3/Assignment%202%20figures/Fig_11.png)

Figure 11: Skewed Line Plot for deaths grouped by Province/State.

Aggregating the deaths, I was able to identify the State that skewed the plot; ‘Others’. 

![alt text](https://github.com/haroonmiah/LSE_Assignment_Covid_Data_Analytics/blob/f9c2252bec7a8dbd8724400450976d15a2740dd3/Assignment%202%20figures/Fig_12.png)

Figure 12: Skewed Line Plot identifying Province/State with skewed data for ‘Deaths’.

Once I removed this State, the plot was showing up as I would expect it to:

![alt text](https://github.com/haroonmiah/LSE_Assignment_Covid_Data_Analytics/blob/f9c2252bec7a8dbd8724400450976d15a2740dd3/Assignment%202%20figures/Fig_13.png)

Figure 13: Line Plot to show the Deaths over time grouped by Province/State.

By converting the dates to months/year, I was able to further improve on this visualisation:

![alt text](https://github.com/haroonmiah/LSE_Assignment_Covid_Data_Analytics/blob/f9c2252bec7a8dbd8724400450976d15a2740dd3/Assignment%202%20figures/Fig_14.png)

Figure 14: Line Plot to show the Deaths over time (month/year) grouped by Province/State.

The States with the highest deaths are Channel Islands and Gibraltar.

![alt text](https://github.com/haroonmiah/LSE_Assignment_Covid_Data_Analytics/blob/f9c2252bec7a8dbd8724400450976d15a2740dd3/Assignment%202%20figures/Fig_15.png)

Figure 15: Line Plot to show the Recovered cases over time (month/year) grouped by Province/State.

![alt text](https://github.com/haroonmiah/LSE_Assignment_Covid_Data_Analytics/blob/f9c2252bec7a8dbd8724400450976d15a2740dd3/Assignment%202%20figures/Fig_16.png)

Figure 16: Line Plot to show the States with the lowest Recovered cases over time (month/year)

The Channel Islands had the highest number of recovered individuals over time

After importing the ‘Tweets’ data into Python, I was able to identify the hashtags that were mentioned the most and visualise these as a bar plot:

![alt text](https://github.com/haroonmiah/LSE_Assignment_Covid_Data_Analytics/blob/f9c2252bec7a8dbd8724400450976d15a2740dd3/Assignment%202%20figures/Fig_17.png)
Figure 17: Bar Plot to show highest trending hashtags.

#COVID19, #CovidIsNotOver and #China were the most common hashtags. 

![alt text](https://github.com/haroonmiah/LSE_Assignment_Covid_Data_Analytics/blob/f9c2252bec7a8dbd8724400450976d15a2740dd3/Assignment%202%20figures/Fig_18.png)

Figure 18: Tweets with China mentioned in them.

![alt text](https://github.com/haroonmiah/LSE_Assignment_Covid_Data_Analytics/blob/f9c2252bec7a8dbd8724400450976d15a2740dd3/Assignment%202%20figures/Fig_19.png)

Figure 19: Scatterplot to show the relationship between Vaccinated and Hospitalised – Gibraltar data.
