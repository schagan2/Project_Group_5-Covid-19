ITCS 4142/ ITCS 6162 - Deliverable 1

1. Team Members:
a. Habibou Dan Aouta
b. Sindhura Chaganti
c. Matthew O’Neill
2. Project Introduction:
a. As we saw on the news, the first outbreak of covid-19 started last year in early December 2019. Over the last few months a copious amount of symptoms, signs and methods have been discovered to have some effectiveness on this historic disease. Due to this outbreak, millions of people have been at home working remotely or relieved from their daily activities such as jobs and self care activities. Therefore, using Kaggle 2 datasets have been found that represent 2 surveys regarding how people are staying fit and their lifestyle over the last few months.  
b. Over the last year, the novel covid-19 virus has had devastating effects all over the world, infecting at least 55 million people and killing at least 1.3 million.  However, despite these grim statistics, the effect of the disease has been very disproportionate in different nations.  Nations such as New Zealand, Singapore, and South Korea have more or less gotten the pandemic under control, while Europe, the US, and Brazil seem incapable of meaningful pandemic response.  In this project, we plan on analyzing a dataset of national data to see if we can find any predictors that help us inform the Covid transmission and death rates.  We will look at things such as population structure (age), diabetes prevalence, cardiovascular disease rates, population density, and other factors in our analysis.
3. Research Question:
a. How Covid-19 impacted people's lifestyle, mental and fitness activities ?
b. How do various national measures affect Covid-19 transmission and death rates?  For example, how do the age structure, cardiovascular disease rates, diabetes prevalence, etc. affect Covid rates.
4. Relevant Domain Information (links to three or more articles that relate to your research question):
a. https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7458584/
b. https://www.mdpi.com/2227-9067/7/9/138/html
c. https://doi.org/10.1016/j.jad.2020.09.014
d. https://doi.org/10.1016/j.dib.2020.106239
e. https://www.medrxiv.org/content/10.1101/2020.05.15.20101097v1
f. https://www.frontiersin.org/articles/10.3389/fpubh.2020.00347/full?report=reader
g. https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7521067/
5. Data Sources (this may be fluid)
a. https://www.kaggle.com/nithilaa/fitness-analysis/tasks
b. https://www.kaggle.com/ydalat/lifestyle-and-wellbeing-data/notebooks
c. https://ourworldindata.org/covid-deaths
d. https://ourworldindata.org/covid-cases
e. https://ourworldindata.org/coronavirus-testing
f. https://ourworldindata.org/excess-mortality-covid
g. https://ourworldindata.org/covid-hospitalizations
6. Approach (how you plan to address the research question):
a. Data understanding and EDA:
1. Exploratory data analysis will be performed by analyzing data, finding missing values and  discarding irrelevant data.  
2. Data Preparation: We will choose a subset of countries to work with.  We are tentatively considering working with European nations with sufficient data, as well as the U.S. and possibly other countries that have similarly reliable data.
b. Machine Learning (if applicable - supervised, unsupervised):
1. In this research, if all exploratory analysis goes well and time permits, we will build various predictive machine learning models that use the national data to predict Covid death and new case rates.
c. Evaluation:
      We will compare our analysis with other analysis that have been conducted in the academic community on the same or similar subjects
7. Known Issues (problems with predictors, reporting, bias, etc.) - this will develop over time
	One major issue in this analysis is figuring out how to standardize the data we are working with.  It is true that different nations have different testing and hospitalization capacities.  The simple fact that nation x has a higher transmission rate than nation y does not necessarily inform you that that is the result of some of the national data predictors that we have access to.  It may be that because of testing capacity, that smaller, more urban, and richer nations catch many more of the true Covid cases than poorer, more rural nations.  It also may be true that some nations may underreport their Covid rates for political reasons.  I am suspicious of Russian and Hungarian Covid rates for this reason.  To try to account for this, we plan on looking at excess mortality rates in these nations to determine if the Covid rates are sufficiently in line with their overall death rates.
8. Conclusion
	Because of the severity of the Covid outbreak, as well as the highly unequal distribution of mortality and morbidity between different nations, it is important to try to understand what factors influence a nation’s susceptibility to a pandemic, as well as the factors that go into protecting nations from the worst parts of a pandemic.  In this analysis, we hope to shed some light onto some of those factors.
9. Github Link:
https://github.com/schagan2/Project_Group_5-Covid-19


