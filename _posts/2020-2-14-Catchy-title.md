---
layout: post
title: Catchy title
---

What matters most in the fight against American child obesity?

![_config.yml]({{ site.baseurl }}/images/posts/youth-obesity/AppleScale.jpg)

Obesity is a condition defined by the [World Health Organization](https://www.who.int/topics/obesity/en/) as a *"major risk factor for a number of chronic diseases, including diabetes, cardiovascular diseases and cancer"* and a leading preventable cause of death in the United States and worldwide.
It is also a condition that is seen increasingly in children.
The [Youth Risk Behavior Surveillance System (YRBSS)](https://www.cdc.gov/healthyyouth/data/yrbs/overview.htm) was developed in 1990 by the Centers for Disease Control and Prevention (CDC) to study obesity and other health outcomes and associated risk factors among youth in the United States.
The motivation for this project is to understand the rates of youth obesity over time and across locations and populations within the United States, and how they are correlated with certain nutritional, behavioral, institutional, and environmental risk factors.
Two datasets from the CDC are considered: [Nutrition, Physical Activity, and Obesity - Youth Risk Behavior Surveillance System](https://chronicdata.cdc.gov/Nutrition-Physical-Activity-and-Obesity/Nutrition-Physical-Activity-and-Obesity-Youth-Risk/vba9-s8jp) contains information on the prevalence of youth obesity and associated risk factors gathered from the YRBSS, and [Nutrition, Physical Activity, and Obesity - Policy and Environmental Data](https://data.cdc.gov/Nutrition-Physical-Activity-and-Obesity/Nutrition-Physical-Activity-and-Obesity-Policy-and/k8w5-7ju6) focuses on state policy and environmental factors.

![_config.yml]({{ site.baseurl }}/images/posts/youth-obesity/Choices.jpg)

{% include image.html url="/images/posts/youth-obesity/Choices.jpg" description="Choices..." %}

When we're trying to take control of our health, it can be hard to know what really works.
That was my goal with this project, to clear some of the fog surrounding healthy choices.

# Question 1: How do rates of high-BMI categories vary over time and by population?

![_config.yml]({{ site.baseurl }}/images/posts/youth-obesity/Q1_obesity.png)

While the percentages of obese and overweight or obese students has declined at some points, overall they have increased with time.
Will this be true also when we consider specific populations?
It won't make much sense to compare obesity rates for population subgroups of different types, e.g. 12th graders and males.
So let's do a comparison for each type of grouping: grade, gender, and race/ethnicity.

![_config.yml]({{ site.baseurl }}/images/posts/youth-obesity/Q1_obesity_by_grade.png)

There isn't much that we can say about the grade subgroups.
They all basically follow the overall trend, with some switching of places throughout the years.

![_config.yml]({{ site.baseurl }}/images/posts/youth-obesity/Q1_obesity_by_gender.png)

The breakdown by gender is much more stark: males have significantly higher percentages than females for all years.
However, the female rates of high-BMI categories are catching up to the male rates.
In fact, the increase in the percent of male students that are overweight or obese from 2001 to 2017 is negligible; the overall increase is almost entirely due to the female population.

![_config.yml]({{ site.baseurl }}/images/posts/youth-obesity/Q1_obesity_by_race_ethnicity.png)

Looking at the race/ethnicity breakdown, some populations' rates are significantly variable over time.
The rates of high-BMI categories among the American Indian/Alaska Native population are the highest in 2001 but the second-lowest in 2017; meanwhile, those of the Hawaiian/Pacific Islander population are second-lowest in 2001 but highest in 2017.
The order of the rates of the other five population groups are more stable.
In most years, the Non-Hispanic Black and Hispanic populations have the highest rates out of these five groups, followed by 2 or more races, Non-Hispanic White, and Asian.
The rates of both of the high-BMI categories for the Asian population are the lowest every year.

One thing you might notice is that the overall obesity rate peaks in 2013, yet in the race/ethnicity breakdown several populations are at or near their lowest points in that year.
This is because there are simply so many more students in certain populations than others, specifically Non-Hispanic White, whose obesity rate peaked in 2013.
This is why we plotted the data such that larger points correspond to larger populations.

# Question 2: How do rates of high-BMI categories vary over time and by location?

![_config.yml]({{ site.baseurl }}/images/posts/youth-obesity/Q2_obesity_by_location.png)

The five locations with below-average rates of high-BMI categories were Colorado, Idaho, Montana, Utah, and Wyoming, all located in the Rocky Mountains.
The five with above-average rates were Guam, Kentucky, Mississippi, Tennessee, and either Arkansas (obesity) or Louisiana (overweightness or obesity).
Besides Guam, these are all located along the Mississippi River.
There is a fair amount of switching places between the locations in each group, but no switching between the groups.
In fact, with the exception of 2013, none of these states ever cross the U.S. average.
It appears that geographic location may be strongly correlated with youth obesity.

# Question 3: What nutritional, behavioral, institutional, and environmental factors are associated with rates of high-BMI categories?

![_config.yml]({{ site.baseurl }}/images/posts/youth-obesity/Q3_factor_bar_chart.png)

Low-BMI locations have percentages lower than the national average of high-school students that *"watch 3 or more hours of television each school day"*, *"consume vegetables less than 1 time daily"*, and *"drink regular soda/pop at least one time per day"*.
Meanwhile, high-BMI locations have percentages higher than the national average for these same categories, as well as for students *"consuming fruit less than 1 time daily"*.

Low-BMI locations also have more farmers markets per capita and more people living within half a mile of a park than the national average, while high-BMI locations have fewer of these than the national average.
Interestingly, none of the low-BMI locations during any of the years in this data have *"state child care regulations that align with national standards for serving fruits"* or likewise for vegetables.
High-BMI locations have these regulations for serving vegetables at rates higher than average, but not for fruits.
Perhaps the high-BMI locations have attempted to address their rates of high-BMI categories among students through regulations, while the low-BMI locations have not seen the need.

Comparing these factors among three groups of locations is not the only way to consider their correlation with the prevalence of high-BMI categories.
We can calculate the Pearson correlation coefficient between all columns in our data, and visualize the correlations between the high-BMI metrics and associated factors.

Certain trends emerge as significant: TV, vegetables, soda, farmers markets, and living near a park.
For these factors, the low-BMI states are on one side of the national average, and the high-BMI states and territories are on the other.

![_config.yml]({{ site.baseurl }}/images/posts/youth-obesity/Q3_factor_heatmap.png)

The relative importance of factors mostly matches what we saw in the bar chart.
Watching TV, drinking soda, eating fruits less often, and especially eating vegetables less often are positively correlated with higher rates of high-BMI across the statewide data, grade-grouped data, gender-grouped data, and race/ethnicity-grouped data.
Living near a park is negatively correlated with higher rates of high-BMI across these data groups.
However, the numbers of farmers markets per capita and the prevalence of vegetable regulations do not appear significant from this analysis, in contrast to the bar chart.

Also, it is important to remember that for the policy/environmental factors, we do not have population-specific data.
In the correlation across location and race/ethnicity for example, we are looking at the correlation between obesity rates in different racial/ethnic groups across many locations versus the percent of all students in that location, regardless of racial/ethnic group, living within half a mile of a park.
With more detailed data we would be able to further refine this analysis and consider more specific questions.

# Question 4: Can we predict rates of high-BMI categories?

The correlation calculation we performed quantifies the degree to which there is a linear relationship between one of our high-BMI metrics of interest and another factor in the data.
However, it does not take into account the other factors.
To do that we can train a linear regression model on the data and see what factors are most important for model performance.
Let's start with the data across all locations and drop the columns we don't want to be in the model.

![_config.yml]({{ site.baseurl }}/images/posts/youth-obesity/Q4_lm_coef.png)

Negative values indicate that the model predicts lower obesity when the factor value is high, while for positive coefficients it predicts higher rates.
The absolute value of the coefficient represents the degree of influence of that factor on model predictions.
Currently **VeggieReg** and **CompleteStreets** are being considered most heavily by the model.
From the bar chart we saw that these factors, especially **VeggieReg**, seemed to be correlated with geographic location.

This function perfoms the steps of data preparation, model building, training, prediction, and scoring for five different choices of algorithm: linear regression, ridge regression, support vector regression (SVR), bagging, random forest, and AdaBoost.
Ridge regression is a regularization technique that performs linear regression but with a penalties imposed on coefficients being too high.
SVR is a regression extension of support vector machines, originally used in classification problems.
Bagging, random forest, and AdaBoost are all ensemble techniques, in which multiple models are constructed and their predictions are integrated by some means into a single prediction.
Let's build another function to plot the accuracy of these models on various subsets of the data.

![_config.yml]({{ site.baseurl }}/images/posts/youth-obesity/Q4_alg_performance.png)

For both the percent of students obese and those overweight or obese, SVR, bagging, and random forest outperform the other algorithms.
We can also see that predictive performance is better across all algorithms for the overall data by location.
This may be because there are simply more data samples, which allow for more training, more learning, and thus higher accuracy when generalizing to the test samples.

# Summary

In examining this data we have seen that the percents of high-school students in the United States that are obese and those that are overweight or obese have increased from 2001 to 2017, are higher in certain racial/ethnic groups, and are higher in males than females, although females are catching up.
We have also learned that five states in the Rocky Mountains have the lowest rates of these high-BMI categories, and in those states students tend to watch less TV, eat more vegetables, and drink less soda than the national average.
Those states also have more farmers markets per capita and more people living within half a mile of a park than the national average.
Five states along the Mississippi River and Guam have the highest rates of these high-BMI categories, and students in those locations tend to watch more TV, eat fewer fruits and vegetables, and drink more soda than the national average.
Those locations also have fewer farmers markets per capita and fewer people living within half a mile of a park than the national average.
Similar results are seen in the single-factor correlation coefficients.
We have also shown that by providing some level of information on geographic location, the test set accuracy of a model can be improved.

One important caveat is that BMI is not the same as body fat percentage, nor is it perfectly correlated.
The metric has been criticized for its bias across height ranges (being underpredicted for shorter individuals and overpredicted for taller) and failure to account for body composition properties, such as a person's degree of musculature.

Another is that much of the data considered here are from self-report surveys, including a student's height and weight, which are used to calculate BMI.
The [YRBSS methodology documentation](https://www.cdc.gov/mmwr/pdf/rr/rr6201.pdf) mentions a CDC study on the reliability of these two question in particular, in which students' heights and weights were measured after having taken the questionnaire:

> *"Self-reported height, weight, and BMI calculated from these values were substantially reliable, but on average, students in the study overreported their height by 2.7 inches and underreported their weight by 3.5 pounds, which indicates that YRBSS probably underestimates the prevalence of overweight and obesity in adolescent populations."*

In addition, the policy data comes from aggregating various state and local level reports under a common standard, for example that the *"state has adopted some form of a Complete Streets policy"*.

Finally, the factors considered here are far from the only ones that could be used to understand and predict rates of youth obesity.
The CDC decided that

> *"the system should focus almost exclusively on health-risk behaviors rather than on the determinants of these behaviors (e.g., knowledge, attitudes, beliefs, and skills), because there is a more direct connection between specific health-risk behaviors and specific health outcomes than between determinants of behaviors and health outcomes."*

However, research and analysis of the determining factors of risk behaviors is undoubtedly important in the effort to address this issue.
