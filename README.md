
# Mathesis MOOCs - Data Science and Machine Learning in Python

## Questions



The results of the study are available at <https://www.cgdev.org/sites/default/files/patel-sandefur-human-capital-final-results.xlsx>. You will download the file and put the `Country Scores` worksheet into a `DataFrame` which we will call `country_scores`. Student performance across countries is assessed by the metrics `Median Math Score (TIMSS Scale, 4th Grade)`, math in 4th grade, and `Median Reading Score (PIRLS Scale, 4th Grade)`, reading in 4th grade.



### Q1: Correlation between Income and Test Results



You will explore the relationship between income in each country and TIMSS and PIRLS test scores, as in 4.1 and Figure 5 of the study. Specifically, you will explore through regression the relationship between the log of income and the TIMMS score, and the log of income and the PIRLS score. After building the relevant models and commenting on your results, you should produce data plots corresponding to the following.



To answer the question, you will also need the `WDI_data.csv` file, which contains income data by country from the World Bank.



### Q2: Correlation between Years of Training and Test Scores




You will investigate how much years in school affect test performance, taking into account per capita income, as in 4.1 and Figure 6 of the study. To do this, you will take the residuals of the models you created in Q1. The residuals contain what of the outcomes cannot be explained by income, so you will use them to see how years of education explains the part of the outcomes that is not explained by income.



So you already have the remainders from the models for TIMSS and PIRLS. Except that years of education may also depend on income in each country. You need to specify a model with log per capita income in 2015 as the independent variable and years of education as the dependent variable. Show the results of the model and obtain the residuals. These residuals represent the years of education that cannot be explained by income. 



Then run a regression between the TIMMS residuals and the years of education residuals and a regression between the PIRLS residuals and the years of education residuals. Show the results and make graphs like the ones below.



Why are we doing all this stuff with the residuals? Because it is likely that student performance and years in school are affected by per capita income. So we want to look at them without that influence.


To answer the question you will also need the file `BL2013_MF1599_v2.2.dta`, which contains the years of education data and comes from Barro, Robert J. and Jong-Wha Lee, A New Data Set of Educational Attainment in the World, 1950-2010, Journal of Development Economics, 2013, 104, 194-198. We will use the values for 2010. The file is in the format of the econometrics program Stata, and can be read with pandas using the `read_stata()` function.