# Notification-system-to-show-spam-free-ads-for-housing-rentals-on-Craigslist-
Notification system to show spam free ads for housing rentals on Craigslist 

In our modelling solution, we have 3 steps:
1.	Identification of Spam Ads
a.	In this first we scrape the data from craigslist. We create 2 files
i.	urls_city.csv - This file contain the url of the listings captured from the craigslist
ii.	city_data_complete.csv - This file contains the features extracted from all the listings as captured in the urls file.
b.	Then, we needed to create a training data-set containing the labels of whether the ad was SPAM or not. For that, we re-checked the captured urls (after 7 days, 14 & 30 days) to validate whether the listing has been marked as spam or not. Based on that we created a final file which contained the features of the listing and added a label of SPAM with values as True or False. 
c.	This data was used as a training dataset for training the various machine learning models.
2.	Getting Search Criteria Data
a.	In this we scraped the data from craigslist based on the keyword specified by the user.
b.	Then we passed the listings to our trained model which detects the spam-ads.
c.	Based on detection, it removes all the spam-ads and creates a list of spam-free ads.
3.	Notification System
a.	After identification of spam-free ads, we identify the most relevant ads from the legitimate listings data which has been curated. 
b.	We send a notification email to the user which contains the relevant spam-free ads.
c.	This process is automated and the user receives an e-mail on daily basis containing the new listings of relevant spam-free ads.

