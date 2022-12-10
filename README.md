# 06-sparksql-dataframes

## Task Description
Download the February 2021 data from TLC Trip Record website

(https://www1.nyc.gov/site/tlc/about/tlc-trip-record-data.page) and use

Pyspark to analyze and answer these questions below. Upload your script

into Github or Gdrive.

1. How many taxi trips were there on February 15?

2. Find the longest trip for each day ?

3. Find Top 5 Most frequent `dispatching_base_num` ?

4. Find Top 5 Most common location pairs (PUlocationID and DOlocationID)?

5. Write all of the result to BigQuery table (additional - point plus)

## How to Run Project:
1. If data not available yet, run bash bin/download_data.sh
2. cd docker/docker-airflow, run docker build docker build --rm --force-rm -t docker-airflow-spark:1.10.7_3.1.2 .
3. cd .. (to return to prev dir)
4. run docker compose up
5. type <external-IP>:8181 to access Airflow
6. type <external-IP>:8282 to access Spark manager
7. type docker logs -f docker-jupyter-spark-1, if want to access jupyter notebook.  This command will generate access token.  Copy that to <external-IP>:8888