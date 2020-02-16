---
layout: post
title: Childhood obesity risk factors
subtitle: What matters most in the fight against American child obesity?
---

{% include image.html url="/images/posts/youth-obesity/AppleScale.jpg" description=" " %}

Obesity is a condition defined by the [World Health Organization](https://www.who.int/topics/obesity/en/) as a *"major risk factor for a number of chronic diseases, including diabetes, cardiovascular diseases and cancer"* and a leading preventable cause of death in the United States and worldwide.
It is also a condition that is seen increasingly in children.
The [Youth Risk Behavior Surveillance System (YRBSS)](https://www.cdc.gov/healthyyouth/data/yrbs/overview.htm) was developed in 1990 by the Centers for Disease Control and Prevention (CDC) to study obesity and other health outcomes and associated risk factors among youth in the United States.
The motivation for this project is to understand the rates of youth obesity over time and across locations and populations within the United States, and how they are correlated with certain nutritional, behavioral, institutional, and environmental risk factors.
Two datasets from the CDC are considered: [Nutrition, Physical Activity, and Obesity - Youth Risk Behavior Surveillance System](https://chronicdata.cdc.gov/Nutrition-Physical-Activity-and-Obesity/Nutrition-Physical-Activity-and-Obesity-Youth-Risk/vba9-s8jp) contains information on the prevalence of youth obesity and associated risk factors gathered from the YRBSS, and [Nutrition, Physical Activity, and Obesity - Policy and Environmental Data](https://data.cdc.gov/Nutrition-Physical-Activity-and-Obesity/Nutrition-Physical-Activity-and-Obesity-Policy-and/k8w5-7ju6) focuses on state policy and environmental factors.

{% include image.html url="/images/posts/youth-obesity/Choices.jpg" description="Choices..." %}

When we're trying to take control of our health, either as an individual or as a society, it can be hard to know what really works.
That was my goal with this project, to clear some of the fog surrounding healthy choices.

# Question 1: How do obesity rates vary over time and by population?

The first question I thought to explore was simply what the rates of American childhood obesity were, and how they had changed over time.
The data from the CDC includes what percent of students are obese as well as what percent are overweight, as determined from BMI.
For adults these definitions are based on absolute thresholds, but for children they depend on age and gender.
Obese is defined as being at or above 95th percentile for BMI relative to age and gender, while overweight is defined as at or above 85th percentile, but below 95th percentile.

I wasn't satisfied with this definition of overweight as a health outcome.
If something were correlated with a decrease in overweightness, I wouldn't know if kids had fallen below 85th percentile for BMI, or had instead risen above the 95th percentile.
Therefore I defined a new category: overweight or obese, including all students at or above the 85th percentile.
With that out of the way, we can look at the rates over time.

![_config.yml]({{ site.baseurl }}/images/posts/youth-obesity/Q1_obesity.png)

With some exceptions, the percentages of obese students across the U.S. increases every time the data is collected, which is every two years.
Overall it's risen from 10.5% in 2001 to 14.8% in 2017.
The same is true for the percent that are overweight or obese, rising from 24.1% to 30.4%.

In addition to the overall statistics, we can also see the rates by grade in school, gender, and race/ethnicity.

![_config.yml]({{ site.baseurl }}/images/posts/youth-obesity/Q1_obesity_by_grade.png)

There isn't much notable about the data by grade; some of the trendlines cross and switch places throughout the years, but all basically follow the same trend as the overall data.

![_config.yml]({{ site.baseurl }}/images/posts/youth-obesity/Q1_obesity_by_gender.png)

The breakdown by gender is much more stark: male students have significantly higher percentages for being obese and for being overweight or obese than female students, across all years.
However, the female percentages are catching up.
In fact, the male overweight or obese rate has been virtually flat from 2001 to 2017, meaning that girls are accounting for practically the entire overall increase.

![_config.yml]({{ site.baseurl }}/images/posts/youth-obesity/Q1_obesity_by_race_ethnicity.png)

The obesity rates for some races/ethnicities are much more variable.
Here the size of the points is proportional to the number of students in each population.
For example, the American Indian/Alaska Native rates are the highest in 2001 but the second-lowest in 2017.
Meanwhile, the Hawaiian/Pacific Islander rates are the reverse, going from second-lowest in 2001 to highest in 2017.
Apart from these two groups, the Non-Hispanic Black and Hispanic students generally have the highest obesity rates, followed by 2 or more races, Non-Hispanic White, and Asian.
The rates of both of the high-BMI categories for the Asian population are the lowest every year.

# Question 2: How do obesity rates vary over time and by location?

Part of the function of the CDC's Youth Risk Behavior Surveillance System is to integrate state and local surveys in one place under a common standard.
Thus, we can look at obesity rates over time as a function of location.
There are 51 locations (47 states, 3 territories, and DC) for which we have data in addition to the national average.
Rather than trying to plot all at once, here are the rates for the top and bottom 5 locations.

![_config.yml]({{ site.baseurl }}/images/posts/youth-obesity/Q2_obesity_by_location.png)

The same five states were lowest in terms of percent of students obese and those overweight or obese, and they're all clustered together in the Rocky Mountains.
The locations with the most obese and the most overweight or obese students are almost the same: Guam tops both lists, and Kentucky, Mississippi, Tennessee, and either Arkansas (obesity) or Louisiana (overweightness or obesity) round out the top five.
Besides Guam, these are all located along the Mississippi River.

While I was not surprised to see the least obese states in the West and the most obese in the South, I did not expect the geographic clustering to be this strong.
Also, these groups' separation from the national average and each other is consistent.
With the exception of 2013 none of these eleven locations' obesity rates ever cross the U.S. average.

# Question 3: What nutritional, behavioral, institutional, and environmental factors are associated with obesity rates?

The goal of this project is not just to see how obesity rates have changed, but what risk factors are associated with those changes.
The YRBSS dataset includes a variety of other self-survey responses, including the percent of students:
* watching 3 or more hours of television each school day
* achieving 1 hour or more of moderate-and/or vigorous-intensity physical activity daily
* participating in daily physical education
* consuming fruit less than 1 time daily
* consuming vegetables less than 1 time daily
* drinking regular soda/pop at least one time per day ("regular" meaning not diet soda)

I also made use of another CDC dataset on state policy and environmental factors over time, from which I identified the following potentially relevant factors:
* Number of farmers markets per 100,000 residents
* Number of food hubs in each state
* Percent of U.S. population living within half mile of a park
* Percent of farmers markets that accept WIC Farmers Market Nutrition Program coupons
* State child care regulations align with national standards for serving fruits (Yes or No)
* State child care regulations align with national standards for serving vegetables (Yes or No)
* State has adopted some form of a Complete Streets policy (Yes or No)

For each of these factors I compared the average of the least obese locations and of the most obese locations to the national average.

![_config.yml]({{ site.baseurl }}/images/posts/youth-obesity/Q3_factor_bar_chart.png)

Certain trends emerge as significant, where the low-BMI states are on one side of the national average and the high-BMI on the other: TV watching, vegetable consumption, soda consumption, farmers markets, living near a park, and regulations on serving vegetables.
Fruit consumption almost falls under this designation too.

All but one of these trends are in the direction that we might expect, e.g. the high-BMI locations watch more TV than the national average while the low-BMI locations watch less.
The exception is the vegetable regulations, where the group more likely to have them in place (and aligned with national standards) is the one with higher obesity rates.
We certainly can't infer causality from this analysis, but we might speculate that the policy effort has come in response to increased obesity rates rather than the other way around.
Likewise, we don't know if a prevalence of farmers markets and parks has any effect on lowering child obesity or is simply a feature of the cultural and economic environment in certain areas of the country.

To validate these findings we can use a more quantitative measure: the correlation coefficient between each factor and the obesity rates.
Here are the coefficients color coded by value, where 1 represents the greatest possible *positive* correlation (increased prevalence of the factor correlates with *increased* obesity), -1 the greatest possible *negative* correlation (increased prevalence of the factor correlates with *decreased* obesity), and 0 signifies no correlation.
The correlations are computed on the overall data as well as by grade, gender, and race/ethnicity.

![_config.yml]({{ site.baseurl }}/images/posts/youth-obesity/Q3_factor_heatmap.png)

The relative importance of factors mostly matches what we see in the bar chart.
Watching TV, drinking soda, eating fruits less often, and especially eating vegetables less often correlate with higher obesity rates, while a high proportion of residents living near a park correlates with lower rates.
However, the number of farmers markets and the prevalence of vegetable regulations don't appear significant from this analysis.

# Question 4: Can we predict obesity rates?

Finally, we can try to predict obesity rates based on the factors we believe to be relevant.
Since what we want to predict is a number (percent students obese), the type of algorithm we need is regression.
For the overall data and the subpopulations, I constructed a variety of regression models, used a portion of the data to train them to predict obesity rates, and tested their accuracy on the remaining data.
From left to right the algorithms increase in complexity, roughly speaking.
Linear regression is similar to the correlation analysis above, except for multiple factors at once.
Ridge regression is linear regression plus a penalty imposed on large coefficients.
Support vector regression (SVR) allows for non-linear relationships, and the final three algorithms are ensemble methods, where multiple models' predictions are combined into one (hopefully) better prediction.

![_config.yml]({{ site.baseurl }}/images/posts/youth-obesity/Q4_alg_performance.png)

Some of the more complex algorithms outperform the simpler ones, but this is not a consistent trend.
We can also see that predictive performance is better across all algorithms for the overall data than for the subgroups.
This may be because there are simply more data samples, which allow for more training, more learning, and thus higher accuracy when generalizing to the test samples.

These models were not allowed to predict based on year, state, grade, gender, or race/ethnicity, but 61% and 63% accuracy are still not really what we want for a useful predictive model.
We could increase model accuracy by training on this data, but instead let's supply more general information: the geographic region of the country.
We can use the four regions of the country defined by the [U.S. Census Bureau](https://www2.census.gov/geo/pdfs/maps-data/maps/reference/us_regdiv.pdf): Northeast, Midwest, South, and West.
Territories are not classified in a region, so we will group them in a separate class.

![_config.yml]({{ site.baseurl }}/images/posts/youth-obesity/Q4_alg_performance_region.png)

Accuracy has improved with this additional information, but not much.
Recalling which states had the highest and lowest obesity rates, they weren't spread all across the South and West respectively, but rather specific parts of those regions.
Let's get a bit more precise with the geography by training on the region subdivisions used by the Census Bureau:
* NewEngland
* MidAtlantic
* EastNorthCentral
* WestNorthCentral
* SouthAtlantic
* EastSouthCentral
* WestSouthCentral
* Mountain
* Pacific

![_config.yml]({{ site.baseurl }}/images/posts/youth-obesity/Q4_alg_performance_division.png)

Now we're getting close to 70% accuracy in predicting our two health outcomes.
We could tune these algorithms' parameters to try to improve performance further, or even explore more complex algorithms, but we may run into model overtraining or simply diminishing returns of our effort.
It's important to remember that the quality of the data is more important than the choice of algorithm.
It seems that while the associated risk factors we identified are somewhat correlated with obesity rates, they alone aren't sufficient for predicting them with high accuracy.

# Summary
Just by considering the associated risk factors (not the year, state, grade, gender, or race/ethnicity), we can achieve a little above 60% accuracy.
By supplying the geographic region (but still not the exact state) we get close to 70%.

In data science it's important to remember that the quality of the data is more important than the choice of algorithm.
Linear regression is often a good place to start beacuse it lets us know if a more complex model is even necessary.

In examining this data we have seen that the percents of high-school students in the United States that are obese and those that are overweight or obese have increased from 2001 to 2017, are higher in certain racial/ethnic groups, and are higher in males than females, although females are catching up.
We have also learned that geography is correlated with  obesity rates, with five states in the Rocky Mountains having the lowest rates, while Guam and five states along the Mississippi have the highest.
Students in the least obese states watch less TV, eat more vegetables, and drink less soda, while those in the most obese states do the opposite.
We have also built models to predict obesity rates, with accuracy as high as 70% when geographic information is provided.

This analysis has uncovered some interesting relationships, but there are some caveats that we should keep in mind.
First, correlation is not causation.
We cannot say that eating more vegetables, drinking less soda, or anything else will lower the obesity rates in a state, territory, or country, at least not from this data.
Second, these obesity rates are statewide; we can't show correlation, yet alone causation, between an individual's behaviors and environment and their BMI.

Third, BMI is not a perfect measure of obesity.
The metric has been criticized for its bias across height ranges (taller people have higher BMIs relative to body fat percentage) and failure to account for body composition properties, such as a person's degree of musculature.
For an example of both of these limitations, this man is 6' 5" and weighs 260 pounds, giving him a BMI of 30.8 and making him "obese":

{% include image.html url="/images/posts/youth-obesity/DwayneJohnson.jpg" description='Dwayne "The Rock" Johnson' %}

Another is that much of the data considered here are from self-report surveys, including a student's height and weight, which are used to calculate BMI.
The [YRBSS methodology documentation](https://www.cdc.gov/mmwr/pdf/rr/rr6201.pdf) mentions a CDC study on the reliability of these two question in particular, in which students' heights and weights were measured after having taken the questionnaire:

> *"Self-reported height, weight, and BMI calculated from these values were substantially reliable, but on average, students in the study overreported their height by 2.7 inches and underreported their weight by 3.5 pounds, which indicates that YRBSS probably underestimates the prevalence of overweight and obesity in adolescent populations."*

In addition, the policy data comes from aggregating various state and local level reports under a common standard, for example that the *"state has adopted some form of a Complete Streets policy"*.

Finally, the factors considered here are far from the only ones that could be used to understand and predict rates of youth obesity.
The CDC decided that

> *"the system should focus almost exclusively on health-risk behaviors rather than on the determinants of these behaviors (e.g., knowledge, attitudes, beliefs, and skills), because there is a more direct connection between specific health-risk behaviors and specific health outcomes than between determinants of behaviors and health outcomes."*

However, research and analysis of the determining factors of risk behaviors is undoubtedly important in the effort to address this issue.
