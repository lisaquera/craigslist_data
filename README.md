# README

## Associated blogpost

http://lquera.com/Quera_DSND_project1.html

## Motivation

Sometimes we begin with a business question and then attempt to find the data to answer it. In this instance, I found a technically interesting dataset, Craigslist postings for used vehicles, and then explored what business questions might be answered by it. This is representative of genuine business situations where a domain expert or data steward might approach you to work with them on understanding the data they have available.

Why did I find this dataset appealing? It had lots of categorical variables, lots of missing data, and several different datatypes in the columns.  This diversity would guarantee both technical challenges - eg. how to extract good variables from raw timestamps, and analytical challenges - eg. how to decide what is truly informative or predictive. At first, the dataset ended up meeting my expectations for fun technical challenges (please see notebook for technical discussion) but disappointing on the business analysis because it was missing key data on desired outcomes. That is, it had the posting data but not the sale data, so for example, we know the price that was asked but not the price that was received and we know when the vehicle was posted but not when it was actually sold.

However, when I changed perspective from the seller to the buyer, I was able to find more useful information.  In the asymmetrical information relationship between buyer and seller, the buyer only has the posting information to work with. So the dataset is well suited to answer the buyer's business questions.


## Results
* Is there a best day to run a search to get a competitive advantage over other buyers? Yes, Wednesday will have the most fresh postings.
* Is there any correlation between paint color and price? Yes, avoid the most common colors to get the best prices.
* Are there significant regional differences that might make traveling worthwhile? Definitely, there are big average price differences at the state and larger regional levels.
* Is there any correlation with length of description (possible proxy for time invested by seller) and price? No, there are no patterns correlated with description length.
* Can prices be predicted? It depends on the model but the errors are too large to provide good price predictions. The RandomForestRegressor output might be useful to give a buyer a negotiation range.




## Libraries and files
Libraries required: Numpy, Pandas, Matplotlib, Scikit-learn

Files:
* vehicles.csv contains the dataset of Craigslist used vehicles for Nov & Dec 2019
* Quera_Craiglist_Vehicle_Analysis.ipynb provides the analytical code and technical discussion
* Quera_3_Things.pdf provides a static rendering of the blogpost


## Models tested
LinearRegression
DecisionTreeRegressor
RandomForestRegressor
On three datasets of varying specificity: National, Western regional, Single vehicle model.


## Acknowledgements
The dataset was helpfully scraped from Craiglist in January 2020 by Austin Reese and posted to kaggle here: https://www.kaggle.com/austinreese/craigslist-carstrucks-data
