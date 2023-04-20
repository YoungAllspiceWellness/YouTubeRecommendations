# YouTubeRecommendations
A tag bases recommendations model using R Shiny

# Description
We have created a R Shiny application which allows a user to input either a series of keywords or a video title and returns video recommendations using a personalizaed PageRank alogrithm. A user can store their watch history and build up a more tailored set of recommendations over time. 

# Files

There are four necessary files

UI.r - the frontside code for the application 
server.r - the backside code for the application
recomendations.sqlite - a database containing the applications data
recommendations.r - a script which contains all the backend functions as well as the funcitons used to create reccommendations.sqlite

# Installation 

## Prerequsites
a machine capable of running R 4.2.1 
at least R 4.2.1
The shiny, tidyverse, magrittr, DBI, RSQLite, glue, igraph, scales, and networkD3 packages with updates as of 4/20/2023

## Running the Application
you can run the application two ways 
  1. directly from github using the command  shiny::runGitHub("YouTubeRecommendations", "YoungAllSpiceWellness")
  2. download the files and run app on your local machine (very important: the sqlite database you use - your own or the one provided - must be in the same     directory as the UI and server files)

# Use

to create a recommendation, the user can start on either the watch history of keywords recommendations tabs. For the watch history tab, the user inputs a user id, their location, and the number of recommended videos and then press the "initialize" button. This uses a random video as a seed to create recommendations. For the keywords tab, the used inputs a set of keywords, their location, and the number of recommenede videos and presses "recommend". 

After this initial recommendation, the user can select the title of any video they have had recommended and input into the watch history tab - along with their user id, location, and number of videos - to create new recommendations. The database will save their preferences and this process can be repeated to tailor their recommendations to their taste. 
