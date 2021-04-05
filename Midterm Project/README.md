# Meal-Planning
Predicting whether tourists will join meals when participating in certain activities

Table of Content
I.  Overview
II. Goals
III.Motivation and Background
IV. Data
V.  Packages and Software

I.	Overview
Crowd source reviews are popular source of gathering information about certain products or services that consumers want to purchase. Using the same medium, companies could gather information on how to better or expand their services or products. 
In this study, the dataset from trip advisor was used.  Consumers’ reviews were gathered from its site. It contains user’s average feedback/rating information on 10 categories of attractions in East Asia.

II.	Goals
This dataset was gathered from a crowd source reviews.  The goal of this study is to be able predict patronization of restaurants using other travel activities such as museums, resorts, picnic, religious institutions, art galleries, beaches, juice bars, and dance clubs. 

III.	MOTIVATION AND BACKGROUND
The background to do this study is because the common denominator for everybody is the need for food or sustenance. However, the emphasis of food is different for many people, some people prioritize activities more than food. This study would like to know what activities have correlation to food. The reviews of restaurants and its correlation to the reviews of the different activities could give a general idea of what people like. Does the activities that people like have correlation to the restaurants?  A review rating of .58 and higher meant that the tourist appreciate food that is served. 
The motivation to do this study is this study could influence the decision making for companies such as travel tour, cruise liner, or restaurant owners. To a travel tour companies, this study would answer what activities are more important than going to a restaurant?  The tour companies could rearrange the schedules of the tours, so the tourist can have a more enjoyable experience. To a cruise ship, this study would answer what certain activities would mean the tourist will not return to the cruise ship for a meal. This will mean reduction of food inventories until the next port. To a restaurant owner, this study would help where to locate the next restaurant if the restaurant targets tourist as their main customers. Using attributes, the study will try to predict if there is a correlation with the dependent variable restaurant with the 9 other attributes. Knowing the correlation of restaurant and the nine other attributes will allow companies to formulate plans for tour activities, for inventories, and for restaurant expansion. 

IV.	DATA
This dataset was populated by crawling from tripadvisor.com. It contains user’s average feedback/rating information on 10 categories of attractions in East Asia. The dataset contains 980 instances with 10 attributes gathered from many destinations. The 10 activities attributes plus 1 User Id attribute which are as follows: Unique user id, feedback on art galleries, dance clubs, juice bars, restaurants, museums, resorts, parks & picnic spots, beaches, theaters, and religious institutions. The ratings are Excellent (4), Very Good (3), Average (2), Poor (1) and Terrible (0).
The study will use logistic regression if the restaurant reviews are equal or higher than .58, there is a correlation with the activity. Otherwise, if it lower than .58, there is no correlation between the dependent variable and the independent variables. The basis of .58 was it was the 75% of the quartile results.

V.	Packages and Software
Jyputer Notebook, Pandas,  Matplotlib, OS, Numpy, Seaborn, Sklearn, Statsmodel, and Mlxtend were used in this study.
