#  Sparkify ETL with Postgres and Python

In this project a database utilizing star schema was created for the prupose of analyzing data around users and their preferences. This data needed to be transformed from it's orgional JSON format during this process.

# Data Files

- **Song Dataset**: files are partitioned by the first three letters of each song's track ID e.g. */data/song_data.*.json. Sample:

```
{"artist_id": "ARD7TVE1187B99BFB1", "artist_latitude": null, "artist_location": "California - LA", "artist_longitude": null, "artist_name": "Casual", "duration": 218.93179, "num_songs": 1, "song_id": "SOMZWCG12A8C13C480", "title": "I Didn't Mean To", "year": 0}
```

- **Log Dataset**: files in the dataset you'll be working with are partitioned by year and month e.g. */data/log_data.*json. Sample:

```
{"artist": "Stephen Lynch", "auth": "Logged In", "firstName": "Jayden", "gender": "M", "itemInSession": 0, "lastName": "Bell", "length": 182.85669, "level": "free", "location": "Dallas-Fort Worth-Arlington", "method": "TX PUT", "page": "NextSong", "registration": 1.540992.., "sessionId": "829", "song":"Jim Henson's Dead", "status": 200, "ts": 1543537327796, "userAgent": "Mozilla/5.0 (compatible; MSIE 10.0; Windows NT...", "userId": 91}
```


# Running these programs.

First, in terminal, run python create_tables.py

Follow this by running etl.py

Finally, checks can be found by running the test.ipynb notebook.

# Additional Files

In addition to the above are the files sql_queries.py, which contains all querries needed in the create_tables.py file, and etl.ipynb, a notebook which starts by connecting to the database, continues by extracting, transforming, and loading the data needed for the songs and artists table.

From there the notebook, etl.ipynb, does the same for data from the data logs, creating tables time, users, and songsplay. 