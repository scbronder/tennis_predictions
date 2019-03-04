# Goal
To determine which factors are most relevant in a tennis match and use them to predict a winner

# Overview
I am an avid tennis fan. I love playing it, watching it, and talking about it. Surprisingly, there is a lack of consistent
and in-depth statistics around this game. Sports fans have seen how advanced metrics in football, baseball, and even basketball
have revolutionized the game for players and fans alike. So, in light of this fact, I wanted this project to try and take a
closer look at what features are most influential towards winning a match and be able to leverage them in such a way to
draw meaningful answers that answer the question, *"What wins a tennis match?"*

# Dataset
This project turned in to an excellent example of how the correct data is needed to drive home relevant and significant
results. As I mentioned before, there is not an extensive database that holds much beyone the most basic of tennis statsistics. Coming to this realization resulted in the project goal changing multiple times. The original goal of this project was to be able to create an in match win prediction to be able to predict the winner of a match between any two opponents at any stage of the match. In order to do this I needed to come up with an initial match prediction prior to the match even starting. This is where my project pivoted as I was not able to get a substantial head-to-head match result required to builed out an accurate model. I was able to scrape data from [tennisabstract.com](http://tennisabstract.com/), which is an independently run and maintained site by Jeff Sackman who has a great github [repository](https://github.com/JeffSackmann) for a lot of statistics. His website has a lot of in-point information that does not directly translate to a point win/loss which is exactly what I was looking for. 

At this point I made the decision to focus on the difference between male and female tennis matches. After reviewing the tennisabstract.com site I realized that there was good class balance between the two sexes. Additionally, each match comparing two players had sufficient information that I could extract and be able to run analysis on just those features. So I had found a place where I could get a sufficient number of matches and corresponding relevant data to run and test some predictive models.

![alt text](https://github.com/scbronder/final_project/blob/master/Screen%20Shot%202019-03-04%20at%202.22.54%20PM.png)

# Data Processing
I scraped the relevant statistics in batches. This was done as the scrapes themselves were taking quite a long time as I was getting roughly 2,000 women matches and 1,800 men matches. After each scape the data was written in to a text file. Each text file was then reimported in to workbook and concatenated in to corresponding men and women dataframes. There were several 
