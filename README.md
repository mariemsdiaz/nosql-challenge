#Eat Safe, Love 

## Introduction
The UK Food Standards Agency evaluates various establishments across the United Kingdom, and gives them a food hygiene rating. You've been contracted by the editors of a food magazine, Eat Safe, Love, to evaluate some of the ratings data in order to help their journalists and food critics decide where to focus future articles.


## Part 1: Database and Jupyter Notebook Set Up

We began by importing a JSON file and assigning it to a database variable named uk_food. Using the PyMongo library in Python, we extracted the database's sole collection, "establishments," and assigned it to a variable for further use and analysis.

Our first task was to add a new restaurant entry to the database, specifically a restaurant called "Penang Flavours." We accomplished this by using the insert_one() function. Next, we aimed to remove all restaurant records in the city of Dover, identified by the LocalAuthorityName field. We successfully executed this task using the delete_many() function. To ensure the deletion was successful, we used the count_documents() function to verify that all Dover-based records were removed.

Finally, we prepared the data for further analysis by updating specific fields. Using the update_many() function, we converted certain values stored as strings into integers and others into decimals, ensuring the data was in the correct format for analysis.

## Part 2: Exploratory Analysis

With our updated data in JSON form, we can now use PyMongo and Python to develop DataFrames from queries we're interested in exploring. We start by querying hygiene scores, specifically finding the number of restaurants with a score of 20 or above using the count_documents() function. After obtaining this data, we convert the query results into a DataFrame using Pandas.

Next, we perform additional queries, focusing on RatingValue in specific geolocations. We use the query, sort, and limit methods to refine these queries, and then convert the results into DataFrames.

Finally, we use the aggregation pipeline method to further narrow down our data into a concise list of results that meet our specific criteria.

### Notes
This module assigment was developed and completed with the help of class activities, cross referencing, tutor sessions, and ChatGPT. 

