# Data Modeling with Apache Cassandra

This repository is for the second Data Engineering Nanodegree project from Udacity. This project implements an ETL pipeline using Python and Apache Cassandra Database:

- Problem understanding
- Data description
- Project structure
- ETL Pipeline description
- Instructions to run the pipeline


## Problem understanding

Develop the databse for startup called Sparkify in Apache Cassandra to improve analytics tasks. Complete an ETL pipeline using Python. To complete the project model your data by creating tables in Apache Cassandra to run queries. The ETL transfers data from a set of CSV files within a directory to create a streamlined CSV file to model and insert data into Apache Cassandra tables.


## Data description

The project uses a sample dataset from [Million Song Dataset](https://labrosa.ee.columbia.edu/millionsong/) with even related to song played in s streaming service. 

- **Events dataset**:  
    event_data/2018-11-08-events.csv
    event_data/2018-11-09-events.csv


### Querys to implement in the database

 - QUERY 1: Give me the artist, song title and song's length in the music app history that was heard during sessionId = 338, and itemInSession = 4
 - QUERY 2: Give me only the following: name of artist, song (sorted by itemInSession) and user (first and last name) for userid = 10, sessionid = 182
 - QUERY 3: Give me every user name (first and last) in my music app history who listened to the song 'All Hands Against His Own'


## Project structure

The project structure is based on the Udacity's project template:
1. **event_datafile_new.csv** denormalized data created from the csv files provided
2. **Project_1B_ Project_Template.ipynb** Jupyter Notebook will al the steps from Keyspace creation, tables creation, insert sql scripts, selects querys and drop tables scripts
3. **README.md** provides projects description

## ETL Pipeline description

### Project_1B_ Project_Template.ipynb
The ETL process is developed all in the 'Project_1B_ Project_Template.ipynb' file. The process init reading all files in the /event_data and then execute a data denormalization transforming the input csv files into a unique csv file with this fields:

 - 0 : artist
 - 1 : firstName
 - 2 : gender
 - 3 : itemInSession
 - 4 : lastName
 - 5 : length
 - 6 : level
 - 7 : location
 - 8 : sessionId
 - 9 : song
 - 10 : userId

The script provides code to:

  - Create the 'sparkify' Keyspace
  - Table creation DDL and INSERT and SELECT querys scritps for each query required
  - Drop tables scripts and close connection commands


## Instructions to run the pipeline

A. Componentes required
  1. Apache Cassandra 2.1 or superior
  2. Jupyter notebooks environment available
  3. Python packages: cassandra, pandas , re, sgon, csv and numpy

B Running the pipeline

  1. Clone the respository
  2. Run Project_1B_ Project_Template.ipynb
  3. Validate in every step the script execution

## Author 
Fernando Bonilla [linkedin](https://www.linkedin.com/in/fer-bonilla/)
