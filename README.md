# Movies_ETL
The "process_ETL" function runs through the data pipeline from extraction, transformation, and loading. In this example, the function extracts data from three filepaths: wikipedia.movies.json, movies_metadata.csv, and ratings.csv. It then proceeds to perform the transformation steps, which include cleaning data from both Wikipedia and Kaggle. Once the data is cleaned, the Wikipedia and Kaggle Movies datasets are merged into one dataset. The ratings dataset is kept apart. The newly transformed datasets are then loaded into SQL database for further analysis.

### Assumptions:

User starts with a data file, such as a .json and .csv, to use this function.
Exploratory data is done prior to or apart from using this function.
It is permissible to remove null data given that half the columns from the Wikipedia dataset contain more than 6,000 null values.
It is permissible to replace NaN with zero's to better utilize dataset.
User is able to calculate statistics for the Ratings dataset given that it is grouped by "MovieID" and "Rating".
Theres is a connection to Postgress/SQL to load datasets using this function.
