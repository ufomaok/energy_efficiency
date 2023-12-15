# energy_efficiency

It is vital to understand how a building's features can increase or decrease its energy efficiency. Buildings are comprised of various features (e.g.: Height), which can play a role in determining how hot or cool the building is going to be. Our analysis aims at analyzing correlation/linear regression to observe howeight building features (Relative Compactness, Surface Area, Wall Area, Roof Area, Overall Height, Orientation, Glazing Area, and Glazing Distribution Area) determines a building's Heating Load (one aspect of energy efficiency).

## Data

Our dataset originated from UC Irvine's public data repository, and was created by Athanasios Tsanas and Angeliki Xifara. Our dataset is comprised of 768 instances (buildings)
UC Irvine Data: https://archive.ics.uci.edu/dataset/242/energy+efficiency

## Method

 We utilized a linear regression model, as it useful for predicting values on a continous scale (in this case Heating Load). It is important to note that some of our X variables were categorized as categorical data and were removed from modeling. However, the relationship between these X variables and Heating Load was analyzed through a correlation matrix. 

## Cleaning
Our goal was to clean our data (fortunately this dataset didn't contain any null values or outliers). However, we specified all of our column names, as our dataset only refered to our X and y variables using letters and numbers (e.g.: renaming X1 to Relative Compactness). Cooling Load was removed from table, since goal of this analysis solely focused on using Heating Load as target variable. 

## EDA

While exploring dataset, we observed that the average Heating Load across dataset fell at approximately 22.31. Additionally, the frequency of most of our sample distributions across X variables were relatively uniform in shape. Our kernel density plots revealed a potential positive correlation between Relative Compactness and Heating Load/Overall Height and Leading Load, as well as a negative correlation between Surface Area and Heating Load, as well as Roof Area and Heating Load. This correlation was confirmed by our correlation matrix. We observed a moderate positive correlation between Relative Compactness (0.62) and Heating Load, a positive correlation between Overall Height of building (0.89) and Heating Load, a moderate negative correlation between Surface Area (correlation -0.66) and Heating Load and strong negative correlation between Roof Area (correlation -0.86) and Heating Load. 

## Modeling

We utilized multiple packages (such as SciKitLearn) to perform machine learning modeling. We pre-processed our data by performing dummy encoding on our non-continuous X variables. We split our data into training/testing and used MinMaxScaler to scale all of our numerical variables. Additionally, we perfomed MSE (15.23) and R-squared (0.86) to determine the efficincy of our model predicting actual values. Our R-squared indicates that about 86% of variation in our output can be explained by our X variables. However, our model's performance yielded an MSE value of 15.23, indicating a moderate level of error in relation to our target variable. Based on our R-Squared value, MSE, and scatterplot, we can see that our model sometimes overestimates and underestimates our actual values, emphasizing the need for additional refinement in our model (or an entirely different model) to better understand and predict our target variable. 

## Further Research

It would be helpful to analyze where a building's city and occupancy size, as this might local building requirements and regulations may play a huge role in the energy efficiency of a building. It may also be wise to analyze the relationship building usage (e.g.: apartment versus working studio), building energy consumption, and Heating Load. These are a few of many examples that engineers, architects, and policymakers can further analyze to improve building and environmental sustainability.   
