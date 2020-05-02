# Flu Shot Learning
Repository for "Flu Shot Learning" Competition, DrivenData

2 May 2020:

Today, I'll read up on background information about the topic, figure out what the topics are like, and do some exploratory data analysis (EDA). 

Interesting questions that I could explore:
	- Are people with children more likely to get flu shots? 
		- What if the child is <6months (this is a binary column in the data)
	- How do their opinions on flu shots affect likelihood of getting shots?
		- This, I'd assume, is the strongest predictor?
	- How do vaccination rates differ by race, location?
		- Seems like there is a difference in vaccination rates by race and by state (see this source: https://www.healthline.com/health-news/why-so-many-adults-children-dont-get-flu-shots-021116#4)
		
	- How do vaccination rates differ by whether their doctor recommended it or not?
	- How do vaccination rates vary by age? Maybe young adults, thinking that they're invincible, 
	are less likely to get flu vaccines? Or maybe elderly people (65+) are disproportionately more likely to get a flu shot?
		- If the rates are skewed by age group, then this means that you can't, for example, build a linear regression, because the coefficient for age would not capture the extreme spikes in vaccination rates for young (which could be low) or elderly (which could be high) people. 
			- An approach could be to keep the age as a category?
			- According to this resource (https://www.npr.org/sections/health-shots/2015/11/27/456202280/many-americans-believe-they-dont-need-the-flu-vaccine), in 2015,
			 people 65+ yrs. old got the flu vaccine at a 71\% rate, while those aged 50-64 got
			 it at a 48\% rate and those 18-49 got it at a 33\% rate.
	
	- Is it possible that the data (which was gathered from calling people) could be
	biased in some systematic way?
	
	- how effective would it be to use ensemble models?
		- e.g., create a separate model for young vs. old adults (because if the rates of vaccinations
		are so disproportionately different across these two age groups, it could be worth either
		creating an indicator variable for age group or just creating a new model for each altogether)
		
	