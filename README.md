# PySpark-ETL-JSON-to-SQL

### PySpark and Apache Kafka for Batch and Streaming Data Processing
### Setting Up the Workspace with Python and PySpark
### PySpark Cluster Configuration

## Create and Initialize the Cluster
docker-compose -f docker-compose.yml up -d --scale spark-worker=2

## Spark Master
http://localhost:9091

## History Server
http://localhost:18081

## Commands to be executed in the terminal or command prompt:

### Open the terminal or command prompt and navigate to the project files folder.

### Run the following commands

### Generate the JSON file
python 01-gera_json.py

### Generate the SQLite database
python 02-cria_database.py


### Execute the Job with JDBC Driver
docker exec dsa-pyspark-master spark-submit --jars data/sqlite-jdbc-3.44.1.0.jar --deploy-mode client ./apps/projeto1.py
