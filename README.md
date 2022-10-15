# Predicting NBA Salaries Using Regression
The goal of this project was to build procure data by webscraping, then using the data to build a predictive regression model that helps to predict the salary of an NBA player based on their age and game stats.

## Data
Data was webscraped off of the NBA official website and includes all regular season stats from 1996-97 to 2021-22 (current). There were over 12K+ data points with over 20+ features in the raw dataset.  Each row represented a player during a given season/year and their associated game stats, such as: age, games played, wins, losses, minutes played, total points, etc.
Data on salary was webscraped off of HoopsHype (www.hoopshype.com).  Each row of data represented a player during a given season/year and their associated salary for that year.
Data was cleaned and the two tables were joined together to produce a dataframe with 11,000 rows of data.

## Tools
Selenium and BeautifulSoup were used to webscrap data from the websites.  All analysis was done in Jupyter Notebook with Python and Python libraries: Matplotlib, Seaborn, Pandas, Numpy, Sklearn, adn Statsmodels.

## Algorithms
I started with a simple linear base model with 27 features and a target "salary".  Initial R^2 values were noted for later comparisons.  
Regularization, scaler standardization were then applied to run a Ridge Regression and Lasso Regression, the latter to help simplify the model by eliminating some features.
Polynomial transformation of the features was applied to see if metrics would improve.
Log transformation of the target was applied to fix normality issues that appeared in teh residual plots.  Unfortunately, the log transformation produced a lower R^2 value.

# Final Model
The best performative model was a LASSO Regression with Polynomial Transformation of the features.
