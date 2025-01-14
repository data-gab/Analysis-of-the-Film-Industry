# Analysis of the Film Industry
***

<img src= "https://sofy.tv/blog/wp-content/uploads/2019/07/movie-industry.jpg" />

## Objectives
***
The objective of this analysis was to gain perspective and understanding of the film industry so that the client, Microsoft, has the information they need to succeed in the film industry. Data were obtained from various reliable film databases and were filtered and analyzed using Python and libraries like Pandas, Numpy, matplotlib, and Seaborn.

## Data Obtained from Film Industry Databases
***

* imdb.title.basics.cvs
    * A subset of data provided by IMDb (Internet Movie Database) which is an online database that provides information on films, television programs, videos, video games, streaming content etc.
    * Contains data about release year, runtime in minutes, genres, primary title, original title, and a unique title idenifier(tconst)
    
    
* imdb.title.ratings.csv
    * Another subset of data provided by IMDb
    * Contains IMDb average rating, number of votes, and tconst for titles
    
    
* tn.movie_budgets.csv
    * A subset of data provided by the The Numbers, a movie industry data website that tracks box office revenue
    * Contains information about titles' id, release date, production budget, domestic gross, and worldwide gross 
    

* bom.movie_gross.csv
    * A subset of data provided by Box Office Mojo that tracks box office revenue
    * Contains data on film titles, studios, domestic gross, foreign gross, and year

## Other Resources
***

[Slideshow url](presentation.pdf)

[Video url](presentation_zoom.mp4)

[Data Cleaning for Question 1](data_cleaning_q1.ipynb)

[Data Cleaning for Question 2](data_cleaning_q2.ipynb)

[Data Cleaning for Question 3](data_cleaning_q3.ipynb)

## Proposed Questions
***
### Question 1. What Genres Have the Highest Average Ratings?
#### To answer this question, data was collected from the following datasets:
* imdb.title.basics.csv
* imdb.title.ratings.csv

#### Graphics
After data was cleaned and organized (see Access to cleaned database notebooks), exploratory data analysis was performed and the following graph was created using the Python data visualization library, Seaborn.

<img src= "images/avg ratings vs genre.png" />

#### Observations and Conclusions
Looking at the graph, we can see that the top 5 genres in terms of ratings are Documentaries, Biographies, History, War, and Musicals. The lowest rated genres are Thrillers, Sci-Fi, and Horror. 

#### Recommendations
To make a significant impact in this industry, I would suggest Microsoft make films belonging to the lowest scored genres. While it is a risk, if the movie is of high quality, the fans will receive them very well since they are usually disappointed with these genres. The top-scoring genres do not seem to me that they reach all audiences; however, it is easier to get all audiences in the lower-rated categories.

***
### Question 2. Can a Larger Production Budget Improve Domestic and Worldwide Gross Profits?
#### To answer this question, data was collected from the following dataset:
* tn.movie_budgets.csv

#### Graphics
The three graphs below demonstrate the relationships between the Movie Production Budget vs. the Domestic Gross, the Movie Production Budget vs. the Worldwide Gross, and the Domestic Gross vs. Worldwide Gross.

<img src= "images/budvsdom.png" />

<img src= "images/budvsww.png" />

<img src= "images/domvsww.png" />

#### Covariance and Correlation
Using the information gathered, the covariance and the correlation between the Movie Budgets, Domestic Gross, and Worldwide Gross were calculated. The tables below show the covariance and correlation matrixes for the data collected.
   ##### Covariance 
 
<img src= "images/covariance.png" />
 
   * **Positive covariance** = positive relationship
   * **Negative covariance** = inverse relationship
   * **Covariance equal to or close to 0** = no linear relationship

##### Correlation

<img src= "images/correlation.png" />

* **If two variables have a correlation of +0.9**: the change in one item results in a similar change to another item
* **If two variables have a correlation of -0.9**: the change in one variable results in an opposite change in the other variable
* **If two variables have a correlation near 0**: there would be no effect
***

#### Observations and Conclusions
Looking at the covariance table, we can see that domestic gross vs. movie production budget has a positive covariance meaning the direction of their relationship is positive. The correlation between domestic gross vs. movie production budget is 0.685682, which demonstrates a low correlation, meaning that change in one will slightly impact the other.

The covariance between worldwide gross vs. movie production budget is positive, meaning the direction of their relationship is positive. The correlation between worldwide gross vs. movie production budget is 0.748306, which is higher than the correlation between domestic gross vs. movie production budget. This shows that a change in worldwide gross with change movie production budget in a similar way.

The covariance between domestic gross and worldwide gross is positive. Their correlation is 0.938853, meaning that there is a high correlation between the two variables.

#### Recommendations
The correlation obtained for domestic gross and movie production budget was lower than the correlation obtained for worldwide gross and film production budget. This suggests that international audiences are more interested in cinema with higher budgets. Higher movie budgets mean that movie studios can hire A-list actors, have quality graphics, writers, directors, producers, etc. This makes sense since A list actors, directors, etc., are more likely to be known worldwide. A larger movie budget allows for a better film crew and actors; therefore, Microsoft should have a large movie budget to get a significant return on investment.

When looking at domestic gross and worldwide gross, their correlation was 0.938853, which demonstrates a very high correlation. This means that if a movie does well domestically, it will most likely do well internationally. The opposite as well is true. If a film does not do well domestically, the same will be for the international gross. For Microsoft to succeed in the film industry, they should focus on how domestic audiences will receive a film and consider releasing their movies abroad to make the most money.

***
### Question 3. What are the Top 15 Film Studios in Terms of Total Gross Revenue?
#### To answer this question, data was collected from the following dataset:
* bom.movie_gross.cvs

#### Graphics
The graph below demonstrates the top 15 film studios in terms of total gross revenue. The total gross income was determined by adding domestic gross and foreign gross.

<img src= "images/top15studios.png" />

#### Observations and Conclusions
The graph above shows the top 15 film studios according to total revenue made by the studios. The top 5 film studios are Buena Vista Studios, 20th Century Fox Studios, Warner Bros Studios, Universal Studios, and Sony Studios. Buena Vista Studios are best known for creating many of the Walt Disney films and Marvel Comics movies. Twentieth Century Fox Studios have created some of the most well-known films such as Titanic, the Home Alone series, Ice Age series, Cast Away, Avatar, etc. Warner Bros. Studios are known for popular films as the Harry Potter Series, The Shining, The Matrix, Space Jam, DC Comics films, etc. Universal Studios has created many famous movies like the Jurassic Park series, the Fast and Furious series, Jaws, Shrek Series, etc.

#### Recommendations
The most successful movie studios produce a majority of animation and action films. Buena Vista studio films make mainly animation films, so they perform the best. Animation films can appeal to audiences of all ages since they generally have a G or PG rating. Twentieth Century Fox Studios produce some animation, but they also create a lot of action films. The top 5 film studios all have in common that they all have very famous movie series.

For Microsoft to succeed in this competitive industry, it would be most beneficial for them to produce animation and action movies and find good writers and producers to create a movie series that audiences will love. A good movie series makes sure that audiences will return for the sequel.
