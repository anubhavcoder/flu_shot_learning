This repo details my progress in DrivenData's "Flu Shot Learning: Predict H1N1 and seasonal flu vaccines" challenge. 

The 'data_exploration.ipynb' Jupyter notebook details my EDA process. 

The 'data_imputation.ipynb' Jupyter notebook details how I went about with imputing missing data. I considered the pros and cons of various approaches before settling on an imputation method. 

The 'models.ipynb' Jupyter notebook details my model-building attempts.

The link for the challenge is: https://www.drivendata.org/competitions/66/flu-shot-learning/

My approach takes the following steps:

\textbf{NOTE TO SELF: SAVE MODEL WEIGHTS}
	- Do background research, learn more about the problem at hand.
	- Think of hypotheses to test from the data
	- Perform exploratory data analysis (EDA) to learn more about the data
	- Create visualizations
	- Perform preprocessing on the data and figure out an appropriate way to impute missing data
	- Design, implement, and evaluate ML models
		- Logistic regression (as baseline)
		- Random forest
		- Feedforward neural network	
	- (possible) - subset the data, run different ML models on different subsets of the data. 
	If this gives promising results (e.g., one model architecture does better on a certain subset of 
	the data than the other models), then we can use an ensemble of various models.
	
	- Work with test set
		- Compare training and test set, check for things such as consistency in class balance, 
		similar proportions of certain values, etc.
		- Run model on test set
		- Get predictions, submit predictions
		
		
Then, based off my findings, I'll provide a few actionable takeaways that could be implemented to promote vaccinations, and see if there's evidence in the literature to support the recommendations.

Tracking performance of models on test set (with AUC metric):
hisq
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