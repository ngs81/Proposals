# Proposals
Proposals for capstone

proposal 1:
Housing prices in Australia:
- The Dataset from kaggle has 7 categorical vars, 3 location vars, 1 id, 2 natural language columns, and one numerical target variable. 
- Amount of data: Total dataset has 105k (105120) rows, only 15 NA’s in the target variable. Unfortunately, upon further inspection - it looks like there are a ton of duplicate rows (all the columns are exactly the same for those duplicates), leaving only 1000 unique rows to analyze. So the small size of the data will be a challenge. 
- The target variable is the price
- We have features like date sold (could separate this feature into year and month features to see if there is some element of seasonality), longitude/latitude which could be used to create  features like “distance to nearest beach”, “distance to nearest park”, and an interesting natural language one is the title which mentions aspects of being close to the beach, good views etc. Upon simple linear regressing, the numerical columns seem to be able to explain 75% of the variance in the data with a decent p-value.

proposal 2:
CryptoCurrnecy prices:
- The dataset will consist of 6 years of daily historical prices (~ 1600 dates) from crypto and other assets from yahoo finance https://finance.yahoo.com/quote/ETH-USD/history?p=ETH-USD, elon musks tweets from kaggle (https://www.kaggle.com/ayhmrba/elon-musk-tweets-2010-2021?select=2021.csv until 202103. how do they get these? ) 
- Target variable: I will rotate around a few cryptos like eth, dog, btc for the target, to see which has most predictive power, given the set of input features, and use that for the target. 
- Features: I will be using similar data for different assets like other cryptos, gold futures, S&P and some other global stock market prices like nikkei -> about 20-30 feature variables. I will merge all these by date, and try to find predictive relations between them. 
 
- Other features: Based on date, I will also try to add some other categorical variables like whether elon musks tweets about crypto that day positively or negativel, whether it is a weekend or not a weekend, day of week. 

proposal 3: is it good from my learning perspective and also to give as a sample to potential employers? I would like to include some aspect of natural language processing in it though not sure yet.

Studying the impact of weather and people's mobility on covid case counts.  
Data set consists of several columns of mobility data, region and datetime (mobility to groceries, pharmacies, parks, transit, workplaces) from beginning of 2020 till date (https://www.google.com/covid19/mobility/) and covid case counts from other sources which will be merged using the datatime column. Weather data will be gotten from weather underground using its api (https://stackabuse.com/using-machine-learning-to-predict-the-weather-part-1)
- the size of the data can get quite big if we consider region+date as another datapoint. It is also very clean with almost no missing values.
- the target variable we are predicting is covid case counts based on the weather and mobility for that region (for the days leading up to it). Another interesting target variable is gas prices (since they seem to be fairly affected by covid, mobility etc.)
- Features:  1 datatime variable, 1 location var (region which will give us some additional categorical features like was the area under lockdown, developing country or not, etc), categorical variables, numerical variables (change in mobility from baseline, temperature, humidity)
- Challenges: it would be nice to somehow include vaccine counts as that probably affects the covid case counts, especially in recent months. I also wanted to include covid tweet data as a natural language feature, but that has been harder to access.



