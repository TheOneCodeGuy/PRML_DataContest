# PRML_DataContest
## PRML Movie Prediction Data Contest 2019
Link to contest and data - https://www.kaggle.com/c/prml19/overview

The dataset exceeds GitHub maximum file size. So, it has not been uploaded.

## Description
**Predict the ratings of movies by different users**
This dataset (a subset of ml-20m) describes 5-star rating and free-text tagging activity from [MovieLens](http://movielens.org), a movie recommendation service. It contains ~7million ratings, split into about 5 million training and 2 million test ratings. There are about 10k distinct users and 10k distinct movies.

All selected users have rated at least 200 movies. No demographic information is included. Each user is represented by an id, and no other information is provided. Each movie is represented by an id, and additional information in the form of the name, genres, attributes and user tags are also available.

The data are contained in six files, 'genome_scores.csv', 'genome_attributes.csv', 'movies.csv', 'train.csv', 'test.csv' and 'tags.csv'. More details about the contents and use of all these files follows.

## Evaluation
The evaluation metric for this competition is the mean squared error.

Your submission must contain exactly the same number of lines as the test.csv file. Each line in your submission must be a comma-separated list of two values, a line number (starting from 0) indicating the line of the test.csv file, and a rating prediction for that line. Check the dummysubmission.csv file for a template.

## Data Desciption
**File descriptions**  
train.csv - the training set
test.csv - the test set
genome_scores.csv - information about the movies
genome_attributes.csv - information about the attributes used in genome_scores.csv
movies.csv - information about the movies
tags.csv - tags given by users in various movies
dummy_submission.csv - a sample submission file in the correct format

**Data fields**  
userId - an anonymous id unique to a given customer
movieId - the id of a movie
title - the title of a movie
genres - the genre of a movie
relevance -
tag -
rating - the rating of a movie given by a user
attributeId -
attribute -

### Detailed information on the files
**Ratings Data File Structure (train.csv and test.csv)**  
All ratings are contained in the file 'train.csv'. Each line of this file after the header row represents one rating of one movie by one user, and has the following format:

userId,movieId,rating

Ratings are made on a 5-star scale, with half-star increments (0.5 stars - 5.0 stars).

**Tags Data File Structure (tags.csv)**  
All tags are contained in the file `tags.csv`. Each line of this file after the header row represents one tag applied to one movie by one user, and has the following format:

userId,movieId,tag

Tags are user-generated metadata about movies. Each tag is typically a single word or short phrase. The meaning, value, and purpose of a particular tag is determined by each user. This is extra information that can potentially be useful (e.g. it may contain information about popular actors/directors), but may be ignored.

**Movies Data File Structure (movies.csv)**  
Movie information is contained in the file `movies.csv`. Each line of this file after the header row represents one movie, and has the following format

movieId,title,genres

Movie titles are entered manually and include the year of release in parentheses. Errors and inconsistencies may exist in these titles.

Genres are a pipe-separated list, and are selected from the following: * Action * Adventure * Animation * Children's * Comedy * Crime * Documentary * Drama * Fantasy * Film-Noir * Horror * Musical * Mystery * Romance * Sci-Fi * Thriller * War * Western * (no genres listed)

**Attribute Genome (genome_scores.csv and genome_attributes.csv)**  
This data set includes a current copy of the attribute values. It contains attribute relevance scores for movies. The structure is a dense matrix: each movie has a value for *every* attribute.

The genome is split into two files. The file 'genome_scores.csv' contains movie-attribute relevance data in the following format:

movieId,attributeId,relevance

The second file, 'genome_attributes.csv', provides the attribute descriptions for the attribute IDs in the genome file, in the following format:

attributeId,attribute

