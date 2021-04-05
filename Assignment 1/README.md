# DATA-601-Assignment1
The cleaning, narration, documentation of Ramen Rater

## Brief Explanation of the Project
This project is a review of ramen noodles. Ramen noodles is a Japanese invention which has evolved to not just with Japanese flavor but has crossed many culture like Korean's Kimchee flavors, Indonesia's Curry flavors, Philippines' Pancit flavors, and etc... 

This project captured my attention from the Kaggle posting by Aleksey Bilogur under www.kaggle.com/residentmario/ramen-ratings. What draws my attention was it only used 2580 reviews as opposed to 3400 original reviews given by The Rater.

There are many varieties of ramen noodles in this survey. It seems that the reviewers have been randomly choosen from the anywhere in the globe since there are many different kinds of ramen from all over the world. What is distinctive is the survey has low European ramen survey participation. We can also find noodle producers from India, Ghana, and Hungary. However, the dominant producers are from Asia such as Japan, Taiwan, Hong Kong, Philippines, and etc. United States also has a good selection of ramen noodles,too.

## Goals of the Project
The goal of the project is choosing which is the go to ramen by reviewers, what is the favorite flavor, how many different flavors are in the review, and which country produces most ramen.

## Methods
The database "The Big List" came in the excel format, so it was converted to csv. It is called Ramen Data in my Jupyter Notebook. There are 3400 reviews with 6 columns. The columns are Review #, Brand, Variety, Style, Country and Stars. To be able to get the favorite ramen, the stars have to be in integer or floating form. From csv, the object has to be converted to integers or floating number. However, the stars are not significant because it is the observation of a few reviewers since most reviewers don't taste a common ramen they are reviewing. 


## Questions attempted to solve
I attempted to solve what is the favorite ramen. Unfortunately, the reviewers are trying different flavors of ramen. A 3400 reviewer with 3140 variety of noodles means that there are only 260 common ramen in the pool.  

The top 3 brands out of 500 ramen producers that are commonly reviewed are: Nissin 460 reviewers, Maruchan 120 reviewers, and Nongshim 113 reviewers.

The top 3 countries that produces ramen are: Japan 606, United States 419, and South Korea 383.

The top 3 styles of packaging are: Pack 1948, Bowls 655, and Cup 593.

My top questions from the survey was will third world countries have the highest consumption of ramen noodles because is a cheap and convenient food. It is surprising that it is the highly industrial countries that consumed most ramen noodles. This questions reflects the possibility that the pace of life in this countries made the reviewers too busy to cook on a daily basis and resorted to quick cheap acessible food.


## Checking missing values, inconsistencies, outliers, sanity checks
In this data, there are at least 3140 varieties of ramen noodle from different producers. Scanning over the data, there are many varieties of noodle as much as reviewers. It seems that a reviewer's ramen needs only to be mentioned at least 3 to 5 times without consideration of the number of stars will be reviewed as a favorite ramen noodle. 

This data seems to have many reviewers giving one of a kind ramen noodle that they like. It is difficult to classify if the noodle the reviewers reviewed is the same noodle with a new caption "New and Improved Flavor". Looking over the data, the outliers will be the noodle that has been reviewed more than thrice.  

The inconsistencies were found in typos for the countries. United Kingdom has one count while UK, an abbreviated form of United Kingdom, has 69 more counts. The Philippines was spelled wrong, so the count was inaccurate. 

## License
Lienesch, Hans. "The Big List." The Ramen Rater. 20 Jan. 2020. 12 Sept. 2020. https://www.theramenrater.com/resources-2/the-list/
