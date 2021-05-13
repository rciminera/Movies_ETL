# Movies_ETL
By Bob Ciminera

## Overview

Amazing Prime Video plans to develop an algorithm to determine which low budget movie being released will be popular so they can purchase the streaming rights. 

In order to have some fun with this, they are sponsoring a hackathon and will provide a clean dataset of movie data to participants as input to their programs to predict popular pictures.

The data set for the event has been created from a scrape of Wikipedia for movies released since 1990, movie rating and metadata from the MovieLens website via Kaggle.

Following the ETL process, the data was Extracted from the 2 sources, Transformed by cleaning and joining into 1 data set, and finally Loaded into an SQL database.

The tools used for this analysis were Python, Pandas, Jupyter Notebook, JSON, RegeX, and git hub large file storage.

## Results


### I. ETL to Read 3 Data Files

The following data files were read:  Wikipedia movie json data, Movie Lens rating csv and movie meta datad via Kaggle. 

Using the pandas code: [ETL_function_test.ipynb](https://github.com/rciminera/Movies_ETL/blob/main/ETL_function_test.ipynb)

These files were each extracted into data

<img src="https://github.com/rciminera/Movies_ETL/blob/main/screenshots/wiki_movies_df.png" width = "700" >

<img src="https://github.com/rciminera/Movies_ETL/blob/main/screenshots/kaggle_df.png" width = "700" >

<img src="https://github.com/rciminera/Movies_ETL/blob/main/screenshots/ratings_df.png" width = "700" >


### II. Extract and Transform Wikipedia Data

The Wikipedia data was extracted and transformed cleaned using 

