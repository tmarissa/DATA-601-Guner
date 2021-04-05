# Population-Explosion-or-Decline-
This is study of a subset from 1987 National Indonesia Contraceptive Prevalence Survey.

# Overview

This dataset uses a subset of 1987 National Indonesia Conctraceptive Prevalence Survey which is a very extensive study of contraception in 20 provinces in Indonesia. The goal of this study is to help policy makers make decisions on fertility and family planning. 

In this project, given a women's many different attributes, can we predict if the population will increase or not increase?

# Goals

This project's goal is to train a classification algorithm that performs better than 55.94% for the population will increase.

# Data
This dataset was found in __[MLdata.io](https://www.mldata.io/dataset-details/contraceptive_method/)__, but the original source was found UCI ML Repo. The resource cited in UCI ML Repo was from Tjen-sien Lim. However, the title cited only skimmed about this dataset in the Lim's research. Lim only acknowledged that this dataset was from J.W. Molyneaux.This dataset is a subset of a bigger research done in 1987 National Indonesia Contraceptive Prevalence Survey. Here is the __[link]( https://dhsprogram.com/pubs/pdf/FR19/FR19.pdf)__. 

The original 1987 National Indonesia Contraceptive Prevalence Survey was very extensive. It studied 11,884 ever-married women with ages 11-49 from 20 provinces in Indonesia. The data was gathered to help policy makers make planned decision about fertily and family planning. However, this subset only provided 1,473 entries and 10 attributes which is approximately 12% of the original study. There are only 10 attributes in this study, but the original study has 802 different questions. 

# Table of Content
- Data are from contraceptive_method_dataset.csv
- Notebooks:
	- [CM_Getting Data](https://github.com/tmarissa/DATA-601/blob/main/Final%20Project/CM_Getting%20Data.ipynb)
		- This is getting data from the __[online source](https://www.mldata.io/dataset-details/contraceptive_method/)__
		- The data is called contraceptive_data which is named after the the title, "Contraceptive Method" - CM.

	- [CM_Exploration Data Analysis 1](https://github.com/tmarissa/DATA-601/blob/main/Final%20Project/CM_Exploration%20Data%20Analysis%201.ipynb)
		- Using describe, different statistical details  are provided such as mean, standard deviation, minimum, maximum, 25%, 50%, and 75%
		- Using box plot, visualization of the data while the outliers were cleaned.
		- Using histogram, further exploration of the data by visualization.

	- [CM_Exploration Data Analysis 2](https://github.com/tmarissa/DATA-601/blob/main/Final%20Project/CM_Exploration%20Data%20Analysis%202.ipynb)
		- The dataset is being assigned to X and y variable. X are all attributes besides children while the y is assigned for the attribute children. The y is split into a binary variable. 
 		- Logistic Regression is performed using Statsmodel. Logit function is used in this process. A model is made and is fitted.
	 	- Odd Ratios is needed to interpret logistic model. First, the results have to exponentiated. The values are interpreted as odds ratios. Its analogy is closes to "how many times likely" the outcome will be.

	 - [CM_Data Preparation](https://github.com/tmarissa/DATA-601/blob/main/Final%20Project/CM_Data%20Preparation.ipynb)
	 	- The dataset is Train Test Split
	 	- Standard Scaling is applied
	 	- Plotting the Logistic Regreesion Chart using PCA

	- [CM_CM_Logistic Regression Unregularized and Regularized.ipynb](https://github.com/tmarissa/DATA-601/blob/main/Final%20Project/CM_Logistic%20Regression%20Unregularized%20and%20Regularized.ipynb)
		- Logistic Regression Modeling was applied. 
		- Without Regularization
		- With Regularization with Ridge
		- With Regularization with Lasso
				 
	- [CM_Decision Tree.ipynb](https://github.com/tmarissa/DATA-601/blob/main/Final%20Project/CM_Decision%20Tree.ipynb)
		- Decision Tree
			- Preliminary Classification 
			- Plotting of the Confusion Matrix
			- Cross Validation Score Plot
			- Cross Validation in 5 Split

	- [CM_K-Means, LogReg, Lasso and Ridge Charts](https://github.com/tmarissa/DATA-601/blob/main/Final%20Project/CM_K-Means%2C%20LogReg%2C%20Lasso%20and%20Ridge%20Charts.ipynb)
		- K-Means
			- Calinski Harbasz Method
			- Silhouette Method
		- Ridge, Lasso and Logistic Regression Test Model
	
# Packages and Software
This project uses Pandas, Numpy, Sklearn, Yellowbrick, Matplotlib, Mlxtend, Itertools, Operation, OS, and Statsmodels. 

