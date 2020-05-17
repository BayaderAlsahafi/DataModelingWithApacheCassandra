
## Purpose

Sparkify is a startup that have released a new music streaming application. In order to analyze their users behavior, they have been collecting songs and user activity data. The analytics team is mainly interested in knowing the popular songs played  among their users. In order to do this analysis easily, they want someone to develop an Apache Cassandra database, which will optimize their analytical operations. 

## Required Queries

1. Give me the artist, song title and song's length in the music app history that was heard during sessionId = 338, and itemInSession = 4
```python
SELECT
    artist, song, length
FROM
    songplay_session_item
WHERE
    session_id = 338 AND item_in_session = 4
```

**Output:**
```
Faithless , Music Matters (Mark Knight Dub) , 495.30731201171875
```

2. Give me only the following: name of artist, song (sorted by itemInSession) and user (first and last name) for userid = 10, sessionid = 182
```python
SELECT
    artist, song, first_name, last_name
FROM
    songplay_user_session
WHERE
    user_id = 10 AND session_id = 182
```

**Output:**
```
Down To The Bone , Keep On Keepin' On , Sylvie , Cruz
Three Drives , Greece 2000 , Sylvie , Cruz
Sebastien Tellier , Kilometer , Sylvie , Cruz
Lonnie Gordon , Catch You Baby (Steve Pitron & Max Sanna Radio Edit) , Sylvie , Cruz
```
    
3. Give me every user name (first and last) in my music app history who listened to the song 'All Hands Against His Own'
```python
SELECT 
    first_name, last_name
FROM
    songplay_song_user
WHERE
    song = 'All Hands Against His Own'
```
**Output**
```
Jacqueline , Lynch
Tegan , Levine
Sara , Johnson
```


## Project Files

Main file in this repository:
* **Project_1B_Project_Template.ipynb:** Contains the ETL for pre-processing the datafiles and the development of the Apache Cassandra database.

