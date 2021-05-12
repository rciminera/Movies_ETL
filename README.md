# Movies_ETL
By Bob Ciminera

## Overview

Amazing Prime Video plans to develop an algorithm to determine which low budget movie being released will be popular so they can purchase the streaming rights at a bargain,  

In order to have some fun with this, they are sponsoring a hackathon and will provide a clean dataset of movie data to participants as input to their programs to predict popular pictures.

This data set for the event has been created from a scrape of Wikipedia for movies released since 1990, rating data from the MovieLens website, and Kaggle data 

Following the ETL process, the data was Extracted from the 2 sources, Transformed by cleaning and joining into 1 data set, and finally Loaded into an SQL database.

The tools used for this analysis were Python, Pandas, Jupyter Notebook, JSON, RegeX, and git hub large file storage.

## Results


### I. ETL to Read 3 Data Files

The following data files were read:  Wikepedia movie json data, Movie Lens rating csv data, and Kaggle movie csv data.

These files were each extracted into their own dataframes using pandas code.

### II. Extract and Transform Wikipedia Data

The Wikipedia data was extracted and transformed cleaned using 

