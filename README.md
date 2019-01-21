# Data-Science-Blog-Analysing-Airbnb-listing-data-for-Boston-and-Seattle

## Get some insights of Boston and Seattle Airbnb listing Data

![GitHub Logo](/images/logo.png)

### Introduction
Airbnb operates an online hospitality service which is accessible via its websites and mobile apps, Its quite popular platform for travellers, one can use the service to arrange or offer lodging, primarily home-stays, or tourism experiences.
Are you interested in knowing how Hosts set rent price? or does your order worth? are there better rental available around the location you are planning to stay? There are many interesting things we can explore using the data from Airbnb. Let's begin with it by asking three simple questions that we are interested in to get an answer for.

### Questions
- 1. What are observable or noticeable difference between Seattle and Boston hospitality services Airbnb?
- 2. What are the most important features which can help estimating Airbnb rentals?
- 3. What are the top most needed facilities ?

### Preparation
data is everything, lets prepare it better to get insights.
I have used Boston Airbnb listings and Seattle Airbnb listings data which can be downloaded from insideairbnb portal, I will follow CRISP-DM methodology get insights from the data.

The CRISP-DM Process (Cross Industry Process for Data Mining)
CRISP-DM stands for cross-industry process for data mining. The CRISP-DM methodology provides a structured approach to planning a data mining project. 

#### lets go through price distribution for Boston and Seattle.

from the data, Boston has almost 6036 listings with average cost $184/night where as Seattle has 8494 listings with an average cost of $152/night. if we dig more in details its clear that 75% of Boston listings lies below $219/night while 75% of Seattle listings lies below $189/night which indicates the rental price for Airbnb in Seattle is comparatively affordable than in Boston.

Most expensive, The most expensive listing in Boston is $3999/night while in Seattle the most expensive one is $5400/night, where least expencive data seems inacurate with value 0 for boston and seatele.

Airbnb hosts can list entire homes/apartments (red), private (green) or shared rooms (blue). 
Hosts listed their room type as 62.2%, 36.6% and 1.2% respectively for the above three room types in Boston, where as in Seattle the room type percentage range goes on 66.6%, 30.4% and 3.1% respectively.
Its time to take a deeper look at data and try to use them to estimate the rental price of Airbnb in Boston and Seattle.

### Model Preparation
Its time to build the model from the data
I dropped the rows above 500 to get a more stable prediction as 90% of them are seems non reverent, I had filled missing values by median value or in come cases most frequent value based on related features, GradientBoostingRegressor was used as classifier for data-sets and a five-fold GridSearchCV was applied to find the best Hyper-parameter for the classifier.
As a general practice splitted main data set to 4/5 and 1/5 for train and test respectively.

### Prediction
Lets get insights of predictions made by our model
Based on our production we would be able to find-out that Airbnb has more amenities listed in Seattle (168) than Boston (120).

### Important Felicities : Boston
Family/kid friendly, Pool, TV, Internet, Elevator, Lock-box, hangers, Laptop friendly work-space and Pets Allowed.
We can see if you have a pool in your property, you might have more confident to raise your rental price.

### Important Felicities : Seattle
First Aid Kit, Carbon monoxide detector, Private entrance, Air conditioning, Iron, Internet, Cable TV, 24 Hour Check-in, safety card.
We can see the importance of amenities are not as high as other features in the last section. As there are more than 100 amenities provided by the hosts and most of them are always provided as they are needed.

### Conclusion
lets recap what we did from the beginning
Gathered the Boston and Seattle Airbnb data
- https://www.kaggle.com/airbnb/seattle/data#listings.csv
- https://www.kaggle.com/airbnb/boston#listings.csv

#### recap : 
we did comparison of the two data sets Boston and Seattle then developed a machine learning model to predict the rental price for Boston and Seattle, after that we examined feature importance of the trained model and check for usability of them and Listed down important felicities to get a clear understanding how service provider can make more money by providing better felicities to customer by understanding the need.
