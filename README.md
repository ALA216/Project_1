## Project_1
This project will discuss COVID-19 related questions.

As COVID-19 brokeout, the government decided to implement lockdown for an immediate outbreak of the high COVID-19 infection. However, this policy cannot be implemented for a long time. So, the government decided to advise the public to wear mask while outside and get vaccinated.
In this project, we will focus on the study effect of wearing masks and getting vaccinated, and study the behavior change in infection spread by analyzing factual data obtained.
For this purpose, the following two factors are assumed to influence infection.
  - Y = # of infections percentage in a state
  - X1 = Wear Mask or Not (A discrete variable)
  - X2 = Vaccinated or Not (A discrete variable)

So, there are the following three questions we pose before we start our statistical study:
  - Q1: How mask mandates affected COVID cases?
  - Q2: How vaccination affected COVID cases?
  - Q3: How both masks and vaccines affected COVID cases?

We have US counties data available year wise from 2020-2022. We can look into each county by its identification number and its infection status, number of casualities. We get a number of infections and normalize it by county population. Also, we have data about wearing masks in each county according to percentage of population and then quoted as percent of population.
There is more than one class and to track mask wearing behavior in a county, we will set a threshold value after checking the distribution of the mask wearing percentage throughout the counties. Based on that threshold, we will create a factored variable about the status of mask wearing. After this, data will be partitioned into two groups. A group who wear masks and a group who do not.
Using two sample or t-test, we will test our hypothesis.
  - H0: Both data sets come from same population, there is no difference means.
  - H1: Both data come from different population but means are not equal.

Data from mid 2020 to mid 2021 will be included.
There are 2 approaches to answer Q2, data will be split into 2 phases, before vaccination period and after vaccination period, or check vaccination status of a a county and then sort into one of the two data sets for vaccinated and non-vaccinated, and then distribution of infection per population will be analyzed by two sample t-test.
For Q3, we will take regression analysis technique into action and make a model below:
  Y = m1*X1 + m2*X2 + m3*X1*X
In this regression analysis, we will see the test statistics and p-values to see the significance of the parameters; m1, m2, and m3.
