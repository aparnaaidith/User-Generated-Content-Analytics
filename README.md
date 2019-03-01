# User-Generated-Content-Analytics
This repository consists of the assignments done by me and my teammates as a part of my Master's coursework.

## What is web-scraping?
Web scraping is a technique for extracting information from the internet automatically using a software that simulates human web surfing.

Web scraping helps us extract large volumes of data about customers, products, people, stock markets, etc. It is usually difficult to get this kind of information on a large scale using traditional data collection methods. We can utilize the data collected from a website such as e-commerce portal, social media channels to understand customer behaviors and sentiments, buying patterns, and brand attribute associations which are critical insights for any business.

## Requirements :
* Python 3.0
* Selenium package
* Chrome driver

## Twitter Sentiment Analysis
This analysis involved scraping conversation messages(Tweets) among different users in Twitter and analyzing them to find four key issues mentioned by the public in the tweets and thereby to establish a relation and sentiment analysis on each candidate and the issue. And also candidates were analyzed with respect to large versus small cities/towns in Texas.

### Notes : The code has been written used Python3 using Jupyter notebook as interface The code needs to be executed in a sequential fashion as in certain case previously created tables are referred to later

### Approach : 
Conversation messages(Tweets) in Twitter were scraped using Tweepy streaming API. Basic text processing techniques such as word tokenization, stopword removal were applied to get relevant words. Using tokenized words data, lift ratio between candidates and issues was calculated which is the ratio of probability that the candidate and issue were mentioned in a particular post divided by the probability each of them were mentioned in the post individually. The dissimilarity values (1 / lift ratio) were then plotted on a Multidimensional scaling plot to see which candidate and issue are closely related with one another and mentioned frequently. To see which candidate are closely linked with issues such as tax, gun, healthcare and oil, lift ratio was calculated in a similar fashion described above to see how closely these candidates are associated with each of these variables and then we get the dissimilarity matrix. This analysis can be useful for the candidates during election time to figure out the core issue they are related with. The analysis can be further improved by calculating the lift ratio between candidates with respect to large versus small cities/towns in Texas.

## Crowdsourced Recommendation System
The objective of this group assignment was to create the building blocks of a crowdsourced recommendation system. This recommendation system should accept user inputs about desired attributes of a restaurant and come up with 3 recommendations.  We broke down this assignment into subtasks and achieved the final objective.

### Tasks Involved :

* **Task A** : After reading the scraped data of the restaurants, we cleaned the data by dropping the columns that are useless to us (retaining the three requested columns).
* **Task B** : We replaced the keywords in the comments to one of the four attributes they belonged to, so we can conduct sentiment analysis. For instance, we replaced “taste”, “smell”, and “vegan” to the attribute name “food”.
* **Task C** : We calculated the word frequency of words in the comments after replacing them to different attributes.
* **Task D (part one)** : In order to recommend similar restaurants to customers, we grouped the restaurants by their name and calculated the average rating of them. Then, we performed the cosine similarity analysis to the restaurants.
* **Task D (part two)** : To better recommend the restaurants to the customers, we conducted a sentiment analysis of the restaurants and sorted them by their score (high to low).
* **Task E** : We built and tested a recommendation function, so the system will recommend the top three restaurants to the customer given the index of a restaurant the customer has already been to (based on cosine similarity and sentiment analysis).
* **Task F** : We built another recommendation system which is simply based on the rating of the restaurants. Comparing to the recommendations generated from Task E, these restaurants have much lower cosine similarity score and sentiment analysis score. In conclusion, the recommendations generated simply from the ratings are not meeting the requirement of the customers.









