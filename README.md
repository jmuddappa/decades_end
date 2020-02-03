![](https://i.imgur.com/AUeIH2y.png)

# Decade's End
An end-to-end data science project that involves scraping, cleaning, creation of databases and data analysis to find the top 10 movies of the decade. 

An article I wrote about the project was featured on Analytics Vidhya: https://medium.com/analytics-vidhya/the-top-movies-of-the-decade-according-to-the-internet-f6be0357c7fb

## Contents
The project contains 3 Jupyter notebooks:
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

2. Run the jupyter notebooks. If any dependencies are found missing, just create a new cell and !pip install the dependency.

## Results

The top 20 list I found was: 

1. Mad Max: Fury Road
2. Moonlight
3. Get Out
4. The Social Network
5. Lady Bird
6. Inside Llewyn Davis
7. Boyhood
8. The Grand Budapest Hotel
9. The Master
10. The Tree of Life
11. Roma
12. The Act of Killing
13. Parasite
14. Inception
15. Call Me By Your Name
16. Spider-Man: Into The Spider-Verse
17. Under the Skin
18. Phantom Thread
19. Whiplash
20. Arrival

After my article was posted, Empire (a highly respected film magazine) published their top movies of the century here: https://www.empireonline.com/movies/features/best-movies-century/. Mad Max topped this list too. Pretty good validation huh? 

## Future Work Possibilities

1. Automating the web scraping or creating more robust functions to do that 

2. Writing generalizable code to create top 10 lists on Buzzfeed effortlessly

3. Deploying a recommender system that utilizes k-means to suggest similar movies to a user.

## Credits

Sources for web scraping can be found in Sources.csv
