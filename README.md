# Project_Group_5-Covid-19


# Association Learning for National Predictors of Covid Deaths<br>

## Team Members​:
1. Habibou Dan Aouta
2. Matthew O'Neill
3. Sindhura Chaganti<br/>
## Project Introduction:<br/>
Over the last year, the novel covid-19 virus has had devastating effects all over the world, infecting at least 55 million people and killing at least 1.3 million. However, despite these grim statistics, the effect of the disease has been very disproportionate in different nations. Nations such as New Zealand, Singapore, and South Korea have more or less gotten the pandemic under control, while Europe, the US, and Brazil seem incapable of meaningful pandemic response. In this project, we plan on analyzing a dataset of national data to see if we can find any predictors that help us inform the Covid transmission and death rates. We will look at things such as population structure (age), diabetes prevalence, cardiovascular disease rates, population density, and other factors in our analysis.  After this simple analysis, we will use Association Learning (a form of machine learning) techniques to see what combinations of factors most predict either high death rates, or low death rates.  We will confine our analysis to European nations of sufficient size (no Vatican City, Monaco, etc.) in order to minimize differences in COvid statistics gathering all over the world.<br/>
## Project Statement <br/>
What are the various national factors that most predict either high Covid deaths, or low Covid deaths.
## Data Source <br/>
Taken from ourworldindata.org.  We used the Covid Deaths Dataset, found under that name.  The most recent day of our analysis was November 14th.
## Data understanding and EDA<br/>
The dataset used in the project 'owid-covid-data.csv' has about 50 columns and 59759 rows. It contains information about the region, spread of covid cases, number of deaths, number of smokers, number of cardiovascular deaths, number of diabetics etc.<br/>
● get a deep understanding of data<br/>
● find missing values and replace them with appropriate data<br/>
● find the relationship between the variables<br/><br>
In the data preparation phase, a subset of data containing the columns ['iso_code', 'continent', 'location','date', 'total_cases', 'total_deaths', 'cardiovasc_death_rate', 'female_smokers', 'male_smokers', 'diabetes_prevalence'] are taken.<br/>
● The data with ‘continent’, ‘iso_code’ which are having the Nan are removed.<br/>
● Replaced the columns ‘total_cases’, ‘total_deaths’, ‘cardiovasc_death_rate’ having nan
values to zero.<br/>
● Replaced the columns ‘female_smokers’, ‘male_smokers, ‘diabetes_prevalence’ having
nan to its mean values.<br/>

The number of covid-cases observed across different parts of the world:

![alt text](https://github.com/schagan2/Project_Group_5-Covid-19/blob/main/Graph1.png?raw=true)

When EDA is performed on the data, the relationship between the variables ‘total_deaths’ and ‘total_smokers’ present in a particular region. And between the ‘total_deaths’ and the ‘cardiovascular_deaths’. And finally with the ‘total_deaths’ and the ‘diabetics’. It is observed that the increase in the ‘total_deaths’ do not change with the cardiovascular_deaths.

![alt text](https://github.com/schagan2/Project_Group_5-Covid-19/blob/main/Graph2.png?raw=true)  

## Data Preparation<br>
For the association learning data preparation, we must force these continuous variables into some sort of binary.  We have decided to code our analysis based on the median value for the European countries listed.  We will calculate the median of each category, such as Diabetes rates, and if you are at or above average, you receive a 1 for the category diabetes_high.  The column diabetes_low will then receive the opposite distribution of 1s and 0s.  This is done for each country until we have a dataset with one row for each country, and many columns of 1s and 0s.<br/>

We are limiting the scope of our analysis and omitting 3 categories, HDI, aged_65_and_older, and hospital_beds_per_thousand because the time needed to process the data.  Running the analysis with just one more of these factors took over 40 minutes before we gave up and limited our scope.<br/>

## Machine Learning<br/>
In the Machine Learning phase, the supervised learning algorithm The  Apriori Algorithm, is used to find all of the combinations of variables that best predict other variables.  We then limit our analysis to those combinations, called antecedents, that point to our Coronavirus death variables, in this case covid_deaths_high and covid_deaths_low.<br/>
## Evaluation<br/>
In the evluation phase, we observed the two main streams 'High Covid Death Rate Associations' and 'Low Death Rate Associations'.<br/>
### High Covid Death Rate Associations:<br/>
In the High Covid Death Rate Associations, it is difficult to find strong relationships between different combinations and high Covid death rates. However, some things pop out. Having low population density appeared in 33 of the 36 highest lift associations. Also, having a low stringency index and high cardiovascular death rates appeared in many of the associations. Despite these findings, there are many associations that do not conform to these three consistent factors.
### Low Covid Death Rate Associations:<br/>
In the Low Covid Death Rate Association, it is also difficult to find strong relationships for low Covid death rates. Having a high population density was found in many of the associations. Also, having a low median age and counterintuitively, a low stringency index were commonly found in the associations.<br/>
## Issues faced:<br/>
One major issue in this analysis is figuring out how to standardize the data we are working with. It is true that different nations have different testing and hospitalization capacities. The simple fact that nation x has a higher transmission rate than nation y does not necessarily inform you that that is the result of some of the national data predictors that we have access to. It may be that because of testing capacity, that smaller, more urban, and richer nations catch many more of the true Covid cases than poorer, more rural nations. It also may be true that some nations may underreport their Covid rates for political reasons. I am suspicious of Russian and Hungarian Covid rates for this reason. To try to account for this, we plan on looking at excess mortality rates in these nations to determine if the Covid rates are sufficiently in line with their overall death rates.<br/>
## Relevant Domain Information<br/>
In our reading of literature, we saw that there were many predictors of Covid deaths found in the scientific literature. These are commonly called comorbidities or pre-existing conditions. For a population from New York City, age was the biggest predictor of death[8]. In another paper, strong correlations between diabetes status and cardiovascular disease were found in a diverse population from 13 different countries[9]. Because of these findings, we hypothesize that we could use data from many European countries and see if we can also find correlations between these national measures and Covid death rate.<br/>
1. https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7458584/
2. https://www.mdpi.com/2227-9067/7/9/138/html
3. https://doi.org/10.1016/j.jad.2020.09.014
4. https://doi.org/10.1016/j.dib.2020.106239
5. https://www.medrxiv.org/content/10.1101/2020.05.15.20101097v1
6. https://www.frontiersin.org/articles/10.3389/fpubh.2020.00347/full?report=reader
7. https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7521067/
8. https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7273288/
9. https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0241742

## Data Sources<br>
1. https://ourworldindata.org/covid-deaths
2. https://ourworldindata.org/covid-cases
3. https://ourworldindata.org/coronavirus-testing
4. https://ourworldindata.org/excess-mortality-covid 
5. https://ourworldindata.org/covid-hospitalizations<br>

## Future Work<br>
For future work, this association analysis could be better done with more specific data.  We used zoomed out, national level data for our analysis, which did not capture much of the underlying complexity of the data.  We would like to do this analysis again, but with state or countl level data from the European countries studied.
## Instructions<br>
● This project is build on Python 3.7<br/>
● Requires Jupyter Notebook to run<br/>
● Requires modules: pandas, seaborn, matplotlib, numpy, mlxtend.frequent_patterns<br/>
To install mlxtend, the following line is executed in command prompt on anaconda:<br/>
> pip install mlxtend<br/>
## Conclusion<br>
While this analysis was interesting, we did not find strong associations for predicting Covid deaths. The highest lift for high death rates was 2.2, and 1.6 for low death rates. Also, there was not a huge amount of consistency in the antecedents that predicted covid death rates. While you would find something like cardiovascular_risk_high more of the time in the high death rate associations, you would still find it multiple times in the low death rate associations. The one exception to this is population density. Low population density consistently was associated with high death rate, while high population density was consistently associated with low death rate.<br/>
The main reason we failed to get many strong, consistent signals from our analysis has to do with the data itself. The data we worked with was national level data. We worked with things such as the average diabetes rate, or the average GDP. These types of national statistics lack any sort of precision and are in a sense "too zoomed out." The way Covid transmission works, is that much of the affects are localized to a certain area during an outbreak. Places like New York City and Lombardy, Italy had terrible outbreaks with factors such as the high population density playing a large part in the disease transmission. However, when you take the average population density of the entire country as your metric, you loose any of the specificity as to why that particular outbreak happened in that particular place. Our data was simply not specific enough, and our results reflected that.<br/>
To do a better analysis, it would be helpful to have not national data, but state level or county level data. If you could analyze Lombardy, Sicily, Bavaria, London, Madrid, and other lower level national divisions, you could potentially get a much better view of what is exactly going on with the disease's progression. Instead of viewing Europe through the window of the space station, you could, metaphorically, look at it while hovering in a low-flying hot air baloon.<br/>
## Github Link<br>
https://github.com/schagan2/Project_Group_5-Covid-19

Questions Answered:<br>
1. What was unique about the data?  Did you have to deal with imbalance? What data cleaning did you do? Outlier treatment?  Imputation?<br/>
This data was unique in that it contained data for each day for almost every country on the globe.  We only wanted to look at a subset of that data, so we grabbed only the European countries.  We also found many nonsensical valvues, such as negative numbers for Covid deaths on certain days, which had to be converted to positive values.  The outlier countries were mainly the microstates such as Vatican City or San Marino, which were lacking almost all data, and were therefore excluded from our analysis.<br/>
2. Did you create any new additional features / variables?<br>
Yes, for association learning, we had to convert all of the continuous variables into binary variables. We did this by a "divide in half" approach, where we divided each category based on the median value, basically seeing if you were in the top half of countries, or the bottom half, for each variable. <br/>
3. What was the process you used for evaluation?  What was the best result? <br>
We used lift as our main criteria for evaluation.  We did not find particularly strong relationships except for population_density, with low population density almost always appearing in high Covid associations, and high population density frequently appearing in low Covid death associations.<br/>
4. What were the problems you faced? How did you solve them?<br>
One major problem was the size of our analysis. When we ran 12 variables, and thus 24 binary categories, the analysis took so long that we had to limit our scope down to 9 variables just to get to run on our computers.<br/>
5. What future work would you like to do? <br/>
See Future Work and Conclusion ablove.<br>
6. Instructions for individuals that may want to use your work <br/>
See Instructions section


