![](https://i.imgur.com/AUeIH2y.png)

# Decade's End
An end-to-end data science project currently in development. My project aims to collect data, examine the data and then finally build and deploy a recommender system. 


## Contents
So far the project contains 3 Jupyter notebooks:
1. Data Collection 
  - **Data Scraping and cleaning** : Scraped the titles from 35 "best movies of the decade" websites using a variety of techniques. Cleaned 1500+ data points using python and excel functions.
2. Data Cleaning 
- **Fuzzy de-duplication** : Found movie titles which are almost the same and made them identical. Eg: "Mad Max: Fury Road" and "Mad Max - Fury Road" should have the same title. Features entity resolution and shingling to fix this. Eventually, I discovered even more titles that needed entity resoltion and so I leveraged a package dedupe to automate this process. Once I ran de-dupe the fuzzy de-duplication was completed!

3. Feature engineering
- **API Usage** : I used the IMDbPy package to gather meta-data about the collected movies including but not limited to the cast, directors, cinematographers, writers, genre of the movies. 
- **Custom features** : 

  1. I developed a scoring feature that would weight movies based on the length of the list that they are found in as well as the rank that they received in those lists! 
         
  2. I wrote a function that can pull data about actors, writers, cinemetographers, directors, editors, composers to get the top artists of the decade. I'm still working on finding the optimal formula for obtaining the most representative list!
  
  3. I wrote functions to do keyword detection using TF-IDF to find the most important words found in the plots of movies.

## Dependencies
1. jupyter
2. beatiful soup
3. pandas-dedupe
4. pickle
5. sklearn
6. imdbpy 

## Setup
1. Clone repository.

```
git clone https://github.com/jmuddappa/decades_end
```

2. Run the jupyter notebooks.


3. WIP - add steps for deployment of web-app

## Future Work Possibilities

1. Automating the web scraping or creating more robust functions to do that 

2. Writing generalizable code to create top 10 lists on Buzzfeed effortlessly

3. Deploying a recommender system that utilizes k-means to suggest similar movies to a user.

## Credits

Sources for web scraping can be found in Sources.csv
