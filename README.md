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

Using the pandas code: [ETL_function_test.ipynb](https://github.com/rciminera/Movies_ETL/blob/main/ETL_function_test.ipynb), the three files were extracted into data frames:

<img src="https://github.com/rciminera/Movies_ETL/blob/main/screenshots/wiki_movies_df.png" width = "700" >

<img src="https://github.com/rciminera/Movies_ETL/blob/main/screenshots/kaggle_df.png" width = "700" >

<img src="https://github.com/rciminera/Movies_ETL/blob/main/screenshots/ratings_df.png" width = "500" >


### II. Extract and Transform Wikipedia Data

The Wikipedia data was extracted, and transformed using Reg_Ex and list comprehension with the following pandas code: [ELT_clean_wiki_movies.ipynb](https://github.com/rciminera/Movies_ETL/blob/main/ETL_clean_wiki_movies.ipynb)

The new wiki_movies_df is as follows:

<img src="https://github.com/rciminera/Movies_ETL/blob/main/screenshots/d2_wiki_movies_df.png" width = "700" >


with the following columns:

<img src="https://github.com/rciminera/Movies_ETL/blob/main/screenshots/wiki_movies_df_columns.png" width = "700" >


### III. Extract and Transform the Kaggle Data

Using Python, Pandas, the ETL process, and code refactoring, the Kaggle metadata and MovieLens rating data was extracted and transformed, then converted into separate DataFrames. 

[ETL_clean_kaggle_data.ipynb](https://github.com/rciminera/Movies_ETL/blob/main/ETL_clean_kaggle_data.ipynb)

The Kaggle metadata dataFrame was then merged with the Wikipedia movies dataFrame to create the movies_df DataFrame. Finally, MovieLens rating data DataFrame was merged with the movies_df DataFrame to create the movies_with_ratings_df.


###IV Create the Movie Database in SQL

Using Python, Pandas, the ETL process, code refactoring, and PostgreSQL the movies_df DataFrame and MovieLens rating CSV data were added to a SQL database.

The data from the movies_df DataFrame replaces the current data in the movies table in the SQL database, as determined by the movies_query.png.

<img src="https://github.com/rciminera/Movies_ETL/blob/main/screenshots/movies_query.png" width = "700" >


The data from the MovieLens rating CSV file is added to the ratings table in the SQL database, as determined by the ratings_query.png. 

<img src="https://github.com/rciminera/Movies_ETL/blob/main/screenshots/ratings_query.png" width = "700" >


The elapsed time to add the data to the database is displayed in [ETL_create_database.ipynb file](https://github.com/rciminera/Movies_ETL/blob/main/ETL_create_database.ipynb)
