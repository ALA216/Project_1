## Project 1: Effects of Mask & Vaccine on Infection Rate
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
  Y = m1*X1 + m2*X2 + m3*X1*X2
In this regression analysis, we will see the test statistics and p-values to see the significance of the parameters; m1, m2, and m3.
## Summary of Finding:
We have found that infection rate of COVID were higher when population were wearing masks. We have also found that the vaccination helped decreasing the infection rate. However, when we did regression, the interaction value of both masks and vaccines is small, which means that there is no interaction.
Mask Mandates: Mean cases value reported in case of no mask is less as compared to that wearing mask. The t-value from calculation and built-in function was found to be -5.568. Also, p << 0.05 so there is sufficient evidence to reject null hypothesis. So, we can say that both data set are not from same and there is difference between mask and no mask data set cases behavior. There was significant evidence to reject null hypothesis. 
![image](https://user-images.githubusercontent.com/112144648/197838355-a1aa4291-832e-4801-a1d7-4040bc3f2306.png)
![image](https://user-images.githubusercontent.com/112144648/197838454-0b01309d-5bbf-4d75-aa5a-f7b0aebf3b00.png)
![image](https://user-images.githubusercontent.com/112144648/197838181-2ca45778-088a-4df9-bb15-0a0d540aaabd.png)

Vaccination: We selected specific dates where percentage of population vaccinated is zero and saved them as non-vaccinated group. Similarly, again, selected specific dates where the percentage of population vaccinated > 0.7 and saved them as vaccinated group. We have found that before vaccination, mean value of population infected is a lot higher than after vaccination. A clear decrease in rise in cases observed and density plot can be seen narrower as compared to the time when there was no vaccine.
![image](https://user-images.githubusercontent.com/112144648/197839059-1f122235-81bb-4d5b-a24a-b4d6d97c80f6.png)
![image](https://user-images.githubusercontent.com/112144648/197839100-78caf5a3-71f9-4e91-bae9-054ad800f043.png)
![image](https://user-images.githubusercontent.com/112144648/197839161-755fad90-e7eb-4092-8d08-e38fc6023831.png)
Mask and Vaccination (Interaction Effect): For the regression analysis, data was obtained for a specified time range for each of state. With interaction term least square regression was performed. This includes population from 2019 estimate. To check whether this parameter in model is significant or not we will see its p-value. The data point was chosen in a way where we have maximum number of valid data points without NaN value. From this, we can see that intercept has p < 0.05 so it is insignificant in this mode. Also, interaction term p-value is way less than 0.05 and its coefficient is very small we can ignore this too and say that there is no interaction. Also, we could see here that the effect of mask is greater than vaccine.
![image](https://user-images.githubusercontent.com/112144648/197839314-cf41dbe4-287d-45bb-b07a-d0a6c3d68b3d.png)

## Recommendations:
1) Doses of Vaccination: We have to see if 1 dose, 2 doses, or with booster would give us different outcomes.
2) Vaccine Type: What type of vaccine are in data.
3) Effect of other mask wearing behavior: effect of other mask wearing status, or change my assumptions to consider more than 1 status, which was just “ALWAYS” for wearing mask.
4) Assumptions Change: Consider changing the assumption of the vaccinated group to be higher than 0.5 instead of 0.7.
