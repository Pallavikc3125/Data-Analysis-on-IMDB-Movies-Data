# Data Analysis on IMDB Movies Data

IMDB- is an online database of information related to films, television programs, home videos, video games, and streaming content online – including cast, production crew and personal biographies, plot summaries, trivia, ratings, and fan and critical reviews.

### Data Description

At this project we will use IMDB Dataset of top 1000 movies and tv shows from https://www.kaggle.com/harshitshankhdhar/imdb-dataset-of-top-1000-movies-and-tv-shows

### Data Shape

number of rows: 1000
number of columns: 16

### Problem Statement

What type of movies are getting good rating and gross amount?

* Data Input: Import data csv, Make sure our data placed in the same folder with our python project data.
* Data Inspection: 

From our inspection we can conclude:
> imdb data contain 1,000 rows and 14 columns after we drop 2 columns (“Poster Link” & “Overview”).
> In column 15, Gross should have numeric data type, so it must be changed before the data processing.
> Metascore is an average score given by the film critic and there are 157 movies that do not have a Metascore. 
* Data Cleansing & Coercions: From Data Inspection, we need to change Gross data type not into numeric by using as.numeric(). But before we can do that, we need to drop the comma symbol by using gsub()
Missing value appears after changing the data type in Gross. This happens because the null object was previously counted as a character. Because we cannot analyze films without Gross, we need to find the missing value and remove it from the dataframe. 
Finally, we have imdb data that contain 831 rows and 14 columns which ready to be processed and analyzed
* Data Visualization and Analysis: libraries used numpy, pandas, matplotlib.pyplot and seaborn.
* Conclusion

> The Dark Knight, The Lord of The Rings, and Inception are the highest-rated and grossing films with an average gross of $372,675,332 and a rating of 8.84.
> The Dark Knight took first place with a gross of $534,858,444 and a rating of 9.0, and was followed by 3 films The Lord of the Rings and Inception. The five films have the Action genre and were released between 2000 and 2010. The absence of films above 2010 could be due to the increasing spectrum of audience reviews and the narrower scope innovation for films.
> While some of the success factors of the five films can come from the actors, and directors such as Christopher Nolan who directed the films The Dark Knight and Inception, and Heath Ledger who was nominated as the actor best portrayal to play Joker in the Batman franchise. Another factor that is no less important is the story line and character development as done by The Lord of The Rings. Although it doesn’t have a bigger gross than the Star Wars or Avengers films, The Lord of The Rings was able to prove its popularity by entering 3 of the top 5 films with the highest rating and gross.
