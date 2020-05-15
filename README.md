This repo details my progress in DrivenData's "Flu Shot Learning: Predict H1N1 and seasonal flu vaccines" challenge. 

The 'data_exploration.ipynb' Jupyter notebook details my EDA process. 

The 'data_imputation.ipynb' Jupyter notebook details how I went about with imputing missing data. I considered the pros and cons of various approaches before settling on an imputation method. 

The 'models.ipynb' Jupyter notebook details my model-building attempts.

The link for the challenge is: https://www.drivendata.org/competitions/66/flu-shot-learning/

My approach takes the following steps:

	- Do background research, learn more about the problem at hand.
	- Think of hypotheses to test from the data
	- Perform exploratory data analysis (EDA) to learn more about the data
	- Create visualizations
	- Perform preprocessing on the data and figure out an appropriate way to impute missing data
	- Design, implement, and evaluate ML models
		- Logistic regression (as baseline)
		- Random forest
		- Feedforward neural network	
		- Ensemble models
	
	- Work with test set
		- Compare training and test set, check for things such as consistency in class balance, 
		similar proportions of certain values, etc.
		- Run model on test set
		- Get predictions, submit predictions
		
From my exploratory data analysis, it seems like I found the following results:

Some of the preliminary findings from the exploratory data analysis are: 

1. Whether or not a doctor recommended a person to get a vaccine was the strongest predictor of if a person got either the H1N1 or the seasonal flu vaccine. However, this may not necessarily be causal. For example, this might just indicate that people who go see the doctor are inclined to be more careful with their health - so, our observed effect might be due to a selection bias. 

2. People without health insurance are less likely to get the seasonal flu vaccine, though this just might be due to the fact that people without health insurance are less likely to see a doctor and therefore less likely to be advised that they need the flu vaccine. 

3. Healthcare workers are more likely to get the seasonal flu vaccine than non-healthcare workers, but it doesn't seem to be due to the fact that they think the seasonal flu is more dangerous than do their counterparts. 

4. Having children in the household somewhat predicts if a person is likely to get the H1N1 or seasonal flu vaccine - but this seems to only be the case if one has a very young child (e.g., 6 months old) who has yet to develop a strong immune system. This finding was unusual because past literature suggested that those with children would be more likely to get a vaccine for both themselves and their children (e.g., https://www.webmd.com/cold-and-flu/news/20181210/almost-half-of-us-adults-to-skip-flu-shot#1; https://www.sciencedirect.com/science/article/pii/S0264410X10017445?via%3Dihub)

5. Those with pre-existing conditions see themselves as more likely to get sick from either the H1N1 or the seasonal flu, and they're also more likely to get the associated vaccines (likely as a result of these beliefs).

From this, it seems like the two most relevant interventions for promoting vaccine adoption are:

1. Increase access to and spread of information regarding the flu - as people's awareness of either the H1N1 or the seasonal flu increases, they tend to be more likely to get the vaccine. 

2. Get people to see their doctors - whether or not a doctor told someone to get a vaccine was the strongest predictor of whether or not they got the vaccine. It is possible that people who see their doctor are more wary about their health in the first place, just as it is possible that poeple who weren't recommended by their doctor to get the vaccine just hadn't seen their doctor in the first place. However, it would logically make sense that seeing a doctor would nudge a person to get the vaccine if the doctor were to advise them to do so. 

Tracking performance of models on test set (with AUC metric):

1. Logistic regression, no hyperparameter tuning: 0.7984 
2. Random forest, no tuning; 0.7582
3. Random forest, randomized cross-validation grid search hyperparameter tuning: 0.8050
4. Logistic regression, no hyperparameter tuning, on standard-scaled data: 0.7984
5. Random forest, with grid search hyperparameter tuning: 0.8039
6. Ensemble of average of predictions from logistic regression, grid-search-hypertuned random forest: 0.8056
7. Ensemble of average of predictions from logistic regression, grid-searched hypertuned random forest, and vanilla feedforward neural network: 0.8054

For my next steps, I would like to try:
	- Examining which features to use (e.g., should I start with more features)
	- Use logistic regression (it seems like using more complicated architectures only marginally improved performance, which makes sense given the size of the dataset)