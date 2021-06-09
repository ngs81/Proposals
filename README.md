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
- Target variable: I will rotate around a few cryptos like eth, dog, btc for the target, to see which has most predictive power, given the set of input features, and use
- Features: I will be using similar data for different assets like other cryptos, gold futures, S&P and some other global stock market prices like nikkei -> about 20-30 feature variables. I will merge all these by date, and try to find predictive relations between them. 
 that for the target. 
- Other features: Based on date, I will also try to add some other categorical variables like whether elon musks tweets about crypto that day positively or negativel, whether it is a weekend or not a weekend, day of week. 

proposal 3:

Human activity recognition using smartphones data set, from UCI:
https://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones#
The target variable is one of 6 types of activity (walking, walking upstairs, walking downstairs etc), and there are about 500 feature variables are signals from the smartphone. 

Quoting them:
The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. 

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain. See 'features_info.txt' for more details. 
For each record they have provided: 
- Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration.
- Triaxial Angular velocity from the gyroscope. 
- A 561-feature vector with time and frequency domain variables. 
- Its activity label. 
- An identifier of the subject who carried out the experiment.



