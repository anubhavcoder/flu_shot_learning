# Flu Shot Learning
Repository for "Flu Shot Learning" Competition, DrivenData

### 2 May 2020:

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
		
	- What does the scientific literature say?
		- From Aguero et al. (2011), it seems like the following factors relate to people following
		H1N1 intervention measures (social distancing, hand-washing, etc.) prior to the vaccine 
		being widely available.
			- Gender: women more likely
			- Education level: higher educated people more likely
			- People who have higher concerns about the virus are more likely
			- People who perceive the government as a useful source of information are more likely
			- People who perceive the risk factors of a vaccine to be lower are more likely
			
		- From Betsch and Wicker (2012), the following factors influence whether a person intends
		to get a vaccination (for flu)
			- (strongest effect) own perceived risk of contracting flu
			- Recommendation to get vaccine (significant, but weaker effect)
			- Belief in vaccine side effects (stronger the belief in side effects, the less likely they were 
			to get vaccinated)
			
		- From Ramsey and Marczinski (2011), the following factors influence whether or not a
		person (in this case, a college student) gets a flu vaccination:
			- For the people who were willing to get the H1N1 flu vaccine, these were the reasons 
			(in descending order of prevalence, as a \% of the people surveyed):
				- They didn't think it would work
				- Worried about side effects
				- Believe vaccine to not be safe
				- Believing that they are not at risk
			- For the people who were not willing to get a flu vaccine, these were the reasons
			(in descending order of prevalence, as a \% of the people surveyed):
				- To avoid flu/illness
				- Belief that H1N1 is deadlier than seasonal flu
				- Living with people who are high risk
				- Being a high-risk person
				
		- From Velan et al. (2011), the following factors pushed people to not get the H1N1 vaccine:
				- Gender: females less likely than males to get H1N1 vaccine
				- Income: lower income people less likely to get H1N1 vaccine
				- Belief that they didn't need the vaccine
				- Belief that vaccine is unsafe
				- Mistrust in the vaccine
				- Don't believe in vaccines in general
				- Belief that the virus posed a low-risk threat
				- Passiveness (e.g., "I never got around to doing it")
				
### 3 May 2020:
	- Today, I will create a few visualizations to better understand the dataset and what values can predict flu vaccination rates, using the knowledge gathered yesterday.
				
	
	