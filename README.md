# Movies_ETL
The "process_ETL" function runs through the data pipeline from extraction, transformation, and loading. In this example, the function extracts data from three filepaths: wikipedia.movies.json, movies_metadata.csv, and ratings.csv. It then proceeds to perform the transformation steps, which include cleaning data from both Wikipedia and Kaggle. Once the data is cleaned, the Wikipedia and Kaggle Movies datasets are merged into one dataset. The ratings dataset is kept apart. The newly transformed datasets are then loaded into SQL database for further analysis.

### Assumptions:

User starts with a data file, such as a .json and .csv, to use this function.
Exploratory data is done prior to or apart from using this function.
It is permissible to remove null data given that half the columns from the Wikipedia dataset contain more than 6,000 null values.
It is permissible to replace NaN with zero's to better utilize dataset.
User is able to calculate statistics for the Ratings dataset given that it is grouped by "MovieID" and "Rating".
Theres is a connection to Postgress/SQL to load datasets using this function.
<img width="803" alt="movies_ratings_df" src="https://user-images.githubusercontent.com/99519095/171477537-c9eddf02-5ecc-4a4d-8654-c256329bcd8d.png">
<img width="756" alt="movies_df" src="https://user-images.githubusercontent.com/99519095/171477544-f08c7288-b75e-4bc5-8a07-52ca5c49c798.png">
<img width="360" alt="wiki_movies_df_columns" src="https://user-images.githubusercontent.com/99519095/171477546-55673502-a42d-4ef0-b0c5-f7acc8ae5095.png">
<img width="750" alt="wiki_movies_df" src="https://user-images.githubusercontent.com/99519095/171477548-b9aee096-cf5d-435b-b2cf-680e488f81be.png">
