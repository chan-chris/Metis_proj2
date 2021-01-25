**Readme.txt**

**Project 2 metis:**

**Date:** 
01/24/2021

**Project Title:** 
Predicting Vintage Vinyl Resale Prices

**Description:**
The purpose of the project is to help buyers and sellers estimate prices for vintage jazz vinyl records. 

**Features and Target Variables:**
The target variable is sales price of an album on Discogs.com. Features used as predictors are : release date, 
Record label, haves, wants, album ratings, album votes, media condition, sleeve condition, notes, etc.

**Data Used:** 
I scraped data from Discogs.com 

**Tools Used:** 
I started with beautiful soup to scrape data initially, but ended up using selenium. I used seaborn and/or marplot lib for some of the visuals. ScikitLearn 
Was also used for some of the models.

**Possible Impacts of your project:** 
Having completed web scraping and data cleaning, I ran a simple linear regression to find coefficients that were impactful
to resale price of an album. Some p-vals of coefficients pointed out collinearity with the outcome or simply noise in the data. Once these were taken
out we reran a linear regression and got an R^2 score of roughly 0.23.

Improvement came in later iterations having used interaction terms, polynomial terms (2nd degree) and standardization. Comparing results for LR, Lasso and 
Ridge, they all came up with similar R^2 scores and MAE scores of roughly 0.46 and $50 respectively. In the end I chose the Ridge model on the test
Data which resulted in an R^2 of 0.37.

Upon a closer look at the final outcome, strong relationships appeared between features such as: Media condition (Mint/near mint) + Record Label (blue note specifically) 
Or people that owned the album + media condition.
Further work can be done to perhaps rank albums in the lists by how frequent an album shows up in the list which points to a potentially higher values. 
Further exploration of blue note records only can be another interesting topic given it’s seeming relationship to resale price.
Extracting more keywords from the notes section could also help explain some of the variation in album prices. 



```python

```
