# Proposals
Proposals for capstone

proposal 1:
Housing prices in Australia:
The Dataset from kaggle has 7 categorical vars, 3 location vars, 1 id, 2 natural language columns, and one numerical target variable. Total dataset has 105k (105120) rows, only 15 NA’s in the target variable. Unfortunately, upon further inspection - it looks like there are a ton of duplicate rows (all the columns are exactly the same for those duplicates), leaving only 1000 unique rows to analyze. So the small size of the data will be a challenge. 
The target variable is the price, and we have features like date sold (could separate this feature into year and month features to see if there is some element of seasonality), longitude/latitude which could be used to create  features like “distance to nearest beach”, “distance to nearest park”, and an interesting natural language one is the title which mentions aspects of being close to the beach, good views etc. Upon regressing, the numerical columns seem to be able to explain 75% of the variance in the data with a decent p-value.




proposal 3:
CryptoCurrnecy prices:
The dataset consists of daily historical prices from crypto and other assets from yahoo finance https://finance.yahoo.com/quote/ETH-USD/history?p=ETH-USD, elon musks tweets from kaggle (https://www.kaggle.com/kulgen/elon-musks-tweets from 2017 onwards) 
I will be using similar data for different assets like other cryptos, gold futures, S&P and some other global stock market prices like nikkei. I will merge all these by date, and try to find predictive relations between them (will rotate around a few cryptos like eth, dog, btc for the target, to see which has most predictive power, given the set of input features). Based on date, I will also try to add some other categorical variables like whether elon musks tweets about crypto that day positively or negatively (Is twitter data something I can get data easily). For the target variable, in addition to daily prices, I will also see if some variant of like returns between two days of the week surrounding the weekend has predictive power, which would tell us maybe its a good idea to always buy before the weekend and sell after the weekend). 
