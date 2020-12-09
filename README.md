ANALYZING COVID-19 DATA
Team Members:
<<<<<<< HEAD
	1. Habibou Dan Aouta
	2. Matthew O'Neill
	3. Sindhura Chaganti��

Project Description:
As we saw on the news, the first outbreak of covid-19 started last year in early December 2019 and has had devastating effects all over the world, infecting at least 55 million people and killing at least 1.3 million. Over the last few months a copious amount of symptoms, signs and methods have been discovered to have some effectiveness on this historic disease.� However, despite these grim statistics, the effect of the disease has been very disproportionate in different nations.� Nations such as New Zealand, Singapore, and South Korea have more or less gotten the pandemic under control, while Europe, the US, and Brazil seem incapable of meaningful pandemic response.� In this project, we plan on analyzing a dataset of national data to see if we can find any predictors that help us inform the Covid transmission and death rates.� We will look at things such as population structure (age), diabetes prevalence, cardiovascular disease rates, population density, and other factors in our analysis.

=======
Habibou Dan Aouta
Matthew O'Neill
Sindhura Chaganti  
Project Description:
As we saw on the news, the first outbreak of covid-19 started last year in early December 2019 and has had devastating effects all over the world, infecting at least 55 million people and killing at least 1.3 million. Over the last few months a copious amount of symptoms, signs and methods have been discovered to have some effectiveness on this historic disease.  However, despite these grim statistics, the effect of the disease has been very disproportionate in different nations.  Nations such as New Zealand, Singapore, and South Korea have more or less gotten the pandemic under control, while Europe, the US, and Brazil seem incapable of meaningful pandemic response.  In this project, we plan on analyzing a dataset of national data to see if we can find any predictors that help us inform the Covid transmission and death rates.  We will look at things such as population structure (age), diabetes prevalence, cardiovascular disease rates, population density, and other factors in our analysis.
>>>>>>> 24f3aab2f13f7380a5540a0284a91ae11ebe5688
CRISP-DM Process:
·         Research phase
·         Data understanding and EDA phase
·         Data preparation phase
Research phase
a. How Covid-19 impacted people's lifestyle, mental and fitness activities ?
b. How do various national measures affect Covid-19 transmission and death rates?  For example, how do the age structure, cardiovascular disease rates, diabetes prevalence, etc. affect Covid rates.
Data understanding and EDA
The dataset used in the project 'owid-covid-data.csv' has about 50 columns and 59759 rows. It  contains information about the region, spread of covid cases, number of deaths, number of smokers, number of cardiovascular deaths, number of diabetics etc. 
Exploratory data analysis phase is performed on the above data to:
get a deep understanding of data 
find missing values and replace them with appropriate data
find the relationship between the variables
The number of covid-cases observed across different parts of the world:
When EDA is performed on the data, the relationship between the variables ‘total_deaths’ and ‘total_smokers’ present in a particular region. And between the ‘total_deaths’ and the ‘cardiovascular_deaths’. And finally with the ‘total_deaths’ and the ‘diabetics’. It is observed that the increase in the ‘total_deaths’ do not change with the cardiovascular_deaths.

Data Preparation
In the data preparation phase, a subset of data containing the columns ['iso_code', 'continent', 'location','date', 'total_cases', 'total_deaths', 'cardiovasc_death_rate', 'female_smokers', 'male_smokers', 'diabetes_prevalence'] are taken.
The data with ‘continent’, ‘iso_code’ which are having the Nan are removed.
Replaced the columns ‘total_cases’, ‘total_deaths’, ‘cardiovasc_death_rate’ having  nan values to zero.
Replaced the columns ‘female_smokers’, ‘male_smokers, ‘diabetes_prevalence’ having nan to its mean values.

b. Machine Learning (if applicable - supervised, unsupervised):
1. In this research, if all exploratory analysis goes well and time permits, we will build various predictive machine learning models that use the national data to predict Covid death and new case rates.
c. Evaluation:
  	We will compare our analysis with other analysis that have been conducted in the academic community on the same or similar subjects
Known Issues
        	One major issue in this analysis is figuring out how to standardize the data we are working with.  It is true that different nations have different testing and hospitalization capacities.  The simple fact that nation x has a higher transmission rate than nation y does not necessarily inform you that that is the result of some of the national data predictors that we have access to.  It may be that because of testing capacity, that smaller, more urban, and richer nations catch many more of the true Covid cases than poorer, more rural nations.  It also may be true that some nations may underreport their Covid rates for political reasons.  I am suspicious of Russian and Hungarian Covid rates for this reason.  To try to account for this, we plan on looking at excess mortality rates in these nations to determine if the Covid rates are sufficiently in line with their overall death rates.
Relevant Domain Information
https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7458584/
https://www.mdpi.com/2227-9067/7/9/138/html
https://doi.org/10.1016/j.jad.2020.09.014
https://doi.org/10.1016/j.dib.2020.106239
https://www.medrxiv.org/content/10.1101/2020.05.15.20101097v1
https://www.frontiersin.org/articles/10.3389/fpubh.2020.00347/full?report=reader
https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7521067/
Data Sources
https://ourworldindata.org/covid-deaths
https://ourworldindata.org/covid-cases
https://ourworldindata.org/coronavirus-testing
https://ourworldindata.org/excess-mortality-covid
https://ourworldindata.org/covid-hospitalizations
Conclusion
        	Because of the severity of the Covid outbreak, as well as the highly unequal distribution of mortality and morbidity between different nations, it is important to try to understand what factors influence a nation’s susceptibility to a pandemic, as well as the factors that go into protecting nations from the worst parts of a pandemic.  In this analysis, we hope to shed some light onto some of those factors.
Github Link
https://github.com/schagan2/Project_Group_5-Covid-19
