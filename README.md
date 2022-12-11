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

## The notebook that contain the answer of above task

Are located in the following directory :

### [`spark_fhv_trip`](https://github.com/df8-naufal-aldy-pradana/06-sparksql-dataframes/blob/main/airflow-spark/notebooks/spark_fhv_trip.ipynb)

***In case, I havent finished the orchestration workflow (In progress)

## How to Run Project:
1. cd airflow-spark 
2. if data not available yet, run bash bin/download_data.sh
3. cd docker/docker-airflow, run docker build docker build --rm --force-rm -t docker-airflow-spark:1.10.7_3.1.2 .
4. cd .. (to return to prev dir)
5. run docker compose up
6. type external-IP:8181 to access Airflow
7. type external-IP:8282 to access Spark manager
8. type docker logs -f docker-jupyter-spark-1, if want to access jupyter notebook.  This command will generate access token, copy the generated link with access token behind it to the web url to open jupyter notebook.
9. go to /notebooks:/home/jovyan/work/notebooks/ directory on jupyter notebook [NB: Kindly do this step if I havent finished the orchestration workflow, currently working on it, will delete this notes later if I'm done]
