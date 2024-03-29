# PySpark-ETL-JSON-to-SQL

### PySpark e Apache Kafka Para Processamento de Dados em Batch e Streaming
### Preparação do Ambiente de Trabalho com Python e PySpark
### Configuração do Cluster PySpark

## Criar e Inicializar o Cluster
docker-compose -f docker-compose.yml up -d --scale spark-worker=2

## Spark Master
http://localhost:9091

## History Server
http://localhost:18081

## Comandos que devem ser executados no terminal ou prompt de comando:

### Abra o terminal ou prompt de comando e navegue até a pasta onde estão os arquivos do projeto

### Execute os comandos abaixo

### Gera o arquivo JSON
python 01-gera_json.py

### Gera o banco de dados do SQLite
python 02-cria_database.py


### Executa o Job com Driver JDBC
docker exec dsa-pyspark-master spark-submit --jars data/sqlite-jdbc-3.44.1.0.jar --deploy-mode client ./apps/projeto1.py
