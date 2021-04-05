# Overview

The objective of this study is to be able to measure with the different attributes if there will be increase or no increase in population.  This is very important for a country because it not just about increase or decrease of human resources but also about the survival of the next generation and caring of the aging generations. There are many factors that influences the number of children that a couple decides to have. Who and what gets to decide the number of children a couple has?

For many years, China had a one child policy. Around late 2015, this policy has been relaxed to a limit of two children with many incentives for more children. However, the receptivity to a change of policy has been taking time to take its roots. On the other hand, Germany experienced low fertility among educated women in around 2008, but this observation was no longer true in 2011 when highly educated East Germany's women have higher fertility than the rest of its population. Does religious belief have influences on the number of children born? Christian country such as Philippines has a median age of 26 which is not very young compared to African countries with median age in the teens and is not as mature compare with Japanese median age of 48. Yet, Philippines also has seen slow yearly decrease of population. What influences the increase or not increase in population? Are they their government's policies, education, religion and/or etc?

The interest in the population explosion or extinction is a concern to many, from businesses, societal groups, environmental groups, and etc... which is why policymakers are very involved in this topic because it affects life itself. All cities becomes extinct when aging citizens dies, and life in the locality will not rejuvenate. On the other hand, population explosion becomes a burden to the many resources such as welfare, food, housing and etc... For these reasons, studies on these topics have been continuously conducted in different parts of the world and at different points in time. One of such study is from Indonesia called 1987 National Indonesia Contraceptive Prevalence Survey. This study is about contraception. Its goal is to help policy makers to make decisions on fertility and family. My project is a subset from this study. The goal of my project is to train a classification algorithm that performs better than 55.94% from the population to increase. Being able to train an better classification algorithm would help understand better what attributes influences the increases in populations and help policy makers formulate plans for the survival of the community. 


# Get the data

 - ###  [CM_Getting Data](https://github.com/tmarissa/DATA-601/blob/main/Final%20Project/CM_Getting%20Data.ipynb)
 	- The original 1987 National Indonesia Contraceptive Prevalence Survey is very extensive. Here is the __[link]( https://dhsprogram.com/pubs/pdf/FR19/FR19.pdf)__ It studied 11,884 ever-married women with ages 11-49 from 20 provinces in Indonesia. However, this project is a subset that only provided 1,473 entries and 10 attributes which is approximately 12% of the original study. Although there are only 10 attributes in this study, the original study has 802 different questions. The 10 attributes are wife_age, wife_education, husband_education, children, wife_religion, wife_working, husband_occupation, standard_of_living_index, media_exposure, contraceptive_method_used. 
	- This project's dataset is found in __[MLdata.io](https://www.mldata.io/dataset-details/contraceptive_method/)__, but the original source is found UCI ML Repo and published in 1997. The resource cited in UCI ML Repo is from Tjen-sien Lim. However, the resource cited only skimmed about this dataset in the Lim's research. Lim acknowledge that this dataset is from J.W. Molyneaux. 
	- My data is called contraceptive_data which is named after the title, "Contraceptive Method" and is gathered in structured csv format. The data does not have empty, null, or na entries, so data is not required to be cleaned by filling with mean, removing with deletion, or whatever is a suitable method. In this notebook, the data has been checked for the ranges of its entries before further exploration. The number of children is used as the dependent variable to measure the increase or no increase in population while the remaining 9 attributes are important as the independent variable that influences the increase or no increase in population.

# Explore the Data 
 
 - ### [CM_Exploration Data Analysis 1](https://github.com/tmarissa/DATA-601/blob/main/Final%20Project/CM_Exploration%20Data%20Analysis%201.ipynb)
 	- To see the head and shape of the data. Click on [CM_Exploration Data Analysis 1](https://github.com/tmarissa/DATA-601/blob/main/Final%20Project/CM_Exploration%20Data%20Analysis%201.ipynb).
	- Various features were used to explore the data like describe, box plot, histogram, and statsmodel which help understand the attributes.
 	- The describe feature presents who took the survey. The survey was conducted with women who were around 16 to 49 years old. The average woman attained a level of education which is lower than the average husband. An average woman would have a minimum of 3 children. She is most likely not working and believe in Islam. Her husband's occupation is around 3. She is not exposed to media and has a standard of living index of 3. The use of contraception is hard to gauze because it is from 0 (no contraception), 2 (long term), 3 (short term). Since long term and short term periods were not defined with specific time frame.
 	- The box plot is used to look into the datasets. If there are some outliers, it is removed to see the box plots clearer. The women's age is symmetrical and has no outlier to clean. The wife's education is around level 3 while the husband is close to 4. Majority of the women are not working, doesn't have much media exposure, doesn't practice contraception, has a level 3 standard of living index.
 	- The histogram gave a clearest assessment of the people survey. There is no cap on the maximum of this bar chart. The most amount of women surveyed are 25 years old which belong the populus range of the women in the survey which is 23 to 36. For this reason average woman's age is around 32 years old. Most women has 1 to 3 children. Having 4 and more children is more than having no children which is why the average is 3 children. Most women practice no contraception. Their husband's education is equally as high as the women, but overall the husband have better education than the woman across all levels. 

 - ### [CM_Exploration Data Analysis 2](https://github.com/tmarissa/DATA-601/blob/main/Final%20Project/CM_Exploration%20Data%20Analysis%202.ipynb)
 	- The dataset is assigned to X and y variable. X are all attributes besides children while the y is assigned for the attribute children. The y is split into a binary variable.
 	- Splitting the children into binary variable. A woman having 0 to 2 children has index 0 while a woman having more than 2 children has index 1. The reason is a woman having 2 or less children will have negative or destabilizing effect on the population while a woman with more than 2 children will have a positive effect on the population because a couple will replace themselves with two offspring.
 	- In this survey, there are 824 people who has more than 2 children which is 55.94% of the population which is the target variable that needed to be increased in this project. There are 649 who has 2 children or less which is 44.059%. The y variable is balance because the difference is not 90% to 10%.
 	- Logistic Regression is performed using Statsmodel. Logit function is used in this process. A model is made and is fitted. This summary was included in this project because it will give us an idea on the statistical significance of these attributes.
 	- Based on this summary, the p-value for intercept, wife's age, wife religion, wife working, and contraceptive method used are statistically significant because the p-value should be lesser than .05. It is interpreted that the intercept is -6.4243. For one unit increase in wife age, the odds increases by a multiplicative factor of 0.1661. For one unit increase in wife religion, the odds increases by a multiplicative factor of 0.3840. For one unit increase in wife working, the odds increases by a multiplicative factor of 0.4585. For one unit increase in contraceptive method used, the odds increase by a multiplicative facor of 0.7788. The p-value for wife's education, husband's education, husband's occupation, and standard of living index are statistically insignificant because the p-value is bigger than 0.5 which makes it statistically insignificant or not sure. Its effect is not by random chance.
	- Odd Ratios is needed to interpret logistic model. First, the results have to exponentiated. The values are interpreted as odds ratios. Its analogy is closes to "how many times likely" the outcome will be. For every one unit increase in wife working, the odds of having more than 2 children increased by 1.58 times. While the every one unit increase in wife's education, the odds of having more than 2 children will decrease by .86 times being greater than 2 

# Prepare the Data 

 - ### [CM_Data Preparation](https://github.com/tmarissa/DATA-601/blob/main/Final%20Project/CM_Data%20Preparation.ipynb)
	- The dataset is Train Test Split by 70%. The total instances for this data is 1,473. Therefore, the X has a training data of 1031 and testing data of 442 while y has the training data split into 454 and 577. The ratio of y train and y test for 0 (equal or less than 2 children) are 44% which is very close.
	- Logistic-regression classifiers decision boundaries on the first two dimensions of the contraceptive dataset - The datapoints are colored according to their labels. The blue labels for 0 represents number of children equal or less than two while the biege labels for 1 represents number of children greater than two. The background is only biege and has no partition from the other label.

# Explore the Models

 - ### [CM_Logistic Regression Unregularized and Regularized](https://github.com/tmarissa/Population-Explosion-or-Decline-/blob/main/CM_Logistic%20Regression%20Unregularized%20and%20Regularized.ipynb)
 	- Logistic Regression was choosen because this has categorical data whose variables are not continuous.
	- For this Logistic Regression Model without Regularization. The Accuracy of the Test score is 0.7769 ~ 0.7769156159068865 while the Accuracy of the Train Score is  0.7534 ~ 0.753393665158371. Here is the Test Score is higher than the Train Score. The Accuracy Score of this plot confusion matrix is approximately 0.7769 ~ 0.77691561590.
	- The plot confusion matrix for the Logisic Regression is interpreted as of the No Population Increase (index 0) 454 which is 324 + 130, 324 (71.36%) is correctly classified. On the other hand the Population Increase (index 1) 577 which is 477 + 100, 477 (82.66897%) is correctly classified. 
	
 - ### [CM_Decision Tree](https://github.com/tmarissa/DATA-601/blob/main/Final%20Project/CM_Decision%20Tree.ipynb)
 	- Decision Tree is included in this modeling because it uses observations about an item (represented in the branches) to conclusions about the item's target value (represented in the leaves).
	- The Decision Tree train score (98.15%) is higher than its test score (65.61%).
	- The plot confusion matrix for the Decision Tree is interpreted as of the No Population Increase (index 0) 195 which is 128 + 67, 128 (65.65%) is correctly classified while for the Population Increase (Index 1) 247 (74 + 173), 173 (70.04%) is correctly classified.
	
 - ### [CM_K-Means, LogReg, Lasso and Ridge Charts](https://github.com/tmarissa/DATA-601/blob/main/Final%20Project/CM_K-Means%2C%20LogReg%2C%20Lasso%20and%20Ridge%20Charts.ipynb) 
	- Two methods of Kmeans was used in this project which are the Calinski Harbabasz and the Silhouette. The Calinski Harbabasz's elbow is more pronounce which can be found in 3 and the score of 3428.76. On the other hand, Silhouette elbow can not be detected in this chart.
	- Based on the chart, the Lasso is flatter than Logistic Regression and Ridge, but Lasso is closer in (variance) distance from Ridge than logistic regression. However, logistic regression have a very similar dip and peaks with ridge. As mentioned earlier, lasso shrinks variables that it deems useless.
	- As we see from above, Lasso uses 0 coefficient which allows more predictability, and there are many useless variables in the data which is why it shrinks to 0. 
    
# Fine Tune the Models

 - As presented in Explore the Models of this Jupyter "Report", Cross Validation was applied to fit models which is to pick optimal parameters for regularization. Cross validation of 5 split was applied to regularization of the Decision Tree, Ridge, and Lasso which is to prevent overfitting of data.
 - Regularization is needed to reduce complexity and helps increase model's interpretability. Two regularization techniques was chosen. Ridge prevents overfitting while Lasso provides sparse solutions. 
 - Refer to [CM_Logistic Regression Unregularized and Regularized](https://github.com/tmarissa/Population-Explosion-or-Decline-/blob/main/CM_Logistic%20Regression%20Unregularized%20and%20Regularized.ipynb)
	- The Vanilla Log Regression (Accuracy) without regularization is 0.772 +/- 0.027.
	- Regularized Log Regression (Ridge) 5 fold cv results (Accuracy) 0.775 +/- 0.025.
	- Regularized Log Regression (Lasso) 5-fold cv results (Accuracy) 0.770 +/- 0.024.
- Refer to [CM_Decision Tree](https://github.com/tmarissa/DATA-601/blob/main/Final%20Project/CM_Decision%20Tree.ipynb)
	- Decision Tree Log Regression 5-fold cv results (Accuracy)  0.734 +/- 0.015.
	- Before the Cross Validation, of the No Population Increase 195 which is 128 + 67, 128 (65.65%) was correctly classified. While for the Population Increase 247 (74 + 173), 173 (70.04%) was correctly classified.
	- After the Cross Validation, of the No Population Increase 195 which is 114 + 81, 114 (58.46%) was correctly classified. While for the Population Increase 247 (38 + 209), 209 (84.61%) was correctly classified.

# Present Your Solution

 - This project's goal is to train a classification algorithm that performs better than 55.94% for the population will increase. Please refer [CM_Exploration Data Analysis 2](https://github.com/tmarissa/DATA-601/blob/main/Final%20Project/CM_Exploration%20Data%20Analysis%202.ipynb).

 - Here are the following selections: The Vanilla Log Regression (Accuracy) without regularization is .772 +/- 0.027. Regularized Log Regression (Ridge) 5 fold cv results (Accuracy) 0.775 +/- 0.025. Regularized Log Regression (Lasso) 5-fold cv results (Accuracy) 0.770 +/- 0.024. Decision Tree Log Regression 5-fold cv results (Accuracy)  0.734 +/- 0.015. It is best to choose the Regularized Log Regression (Ridge) 5 fold cv results (Accuracy) 0.775 +/- 0.025 which ranges between 0.75 to 0.80. The Regularized Log Regression (Ridge) 5 fold cv results is the best accuracy among the models.

 - The reason that the Ridge Regression has higher accuracy is it has more useful variables and has shrunk the slope asympthotically close to O. There is no certainity with any results. However, this results provides the highest predictability with these data. This dataset provides a good preliminary study as observed on the [CM_Exploration Data Analysis 1](https://github.com/tmarissa/DATA-601/blob/main/Final%20Project/CM_Exploration%20Data%20Analysis%201.ipynb) because the data has good distributions. As stated in the limitations and later work selection, more data are needed which also needs more clarifications to be able to analyze effectively.  

# Limitations and Later Work

 - In this survey, the wife’s and husband’s education, husband’s occupation, standard of living index, and contraceptive method are nominal numbers. It is unclear what the placeholders represents. The numbers are represented in ascending order from low 1 to high 4.  For education, does 1 represent primary education, 2 to 3 represents junior to senior high, and 4 represent university education? For husband’s occupation, what does 1 to 4 represents? For standard of living index, what does 1 to 4 represents? For contraceptive method, there are three placeholders. While 1 placeholder represents people not using contraception, 2 representing long term and 3 representing short term seem to be unclear. What is the length of the long term is it months or years of usage? What is the length of short term? 

 - In the original study, more details have been provided. It is hard to incorporate the classification of the original study to this subset since they use different classification. Example, education was classified as 0 - none, 1 - some primary, 2 - completed primary, 3 - junior high, 4 - senior high, 5 - academy, 5 - DK. Another example, religion was classified 1 - Muslim, 2 - Protestant/Christian, 3 - Catholic, 4 - Hindu, 5 - Buddhist, 6 - others. 

# References and Contributions

Contraceptive Method. Chart. MLData. By Tjen-Sien Lim. 1997. 27 Nov. 2020. https://www.mldata.io/dataset-details/contraceptive_method/

Countries in the World By Population (2020). __Worldometer__. 15 Nov. 2020. https://www.worldometers.info/world-population/population-by-country/

“Demographics of Germany”. __Wikipedia__. The Free Encyclopedia. Wikipedia. Free Encyclopedia. Web 15 Nov. 2020. https://en.wikipedia.org/wiki/Demographics_of_Germany

Indonesia. __Central Bureau of Statistics, National Family Planning Coordinating Board and Institute of Resource Development/Westinghouse__. National Indonesia Contraceptive Prevalence Survey 1987. Jakarta: Central Bureau of Statistics, 1987. https://dhsprogram.com/pubs/pdf/FR19/FR19.pdf

Lim, Tjen-Sien, Loh, Wei-Yin, and Shih, Yu-Shan. "A Comparison of Prediction Accuracy, Complexity and Training Time of Thirty-Three Old and New Classification Algorithms." __Machine Learning__ 40 (2000): 203-229. http://pages.stat.wisc.edu/~loh/treeprogs/guide/mach1317.pdf

