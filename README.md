# airflow-on-aws

* workshop spec
  - Airflow Orchestration
      - PC located airflow, not cloud
      - communication with boto3 api 
  - 전처리 : Glue / Spark
  - ML training / parameter tunning / Interference -> sagemaker.
  - not embrace feature store (on/offline)
  - bucket structure is broze / silver / gold
    - delta lake / iceberg with parquet
  - no visualization support such as quicksight, tableau
  - pytorch for ml
  - pypark for sparkml & dataframe - de
  - CI/CD
      - github / github action.
      - code commit / copepipeline
  - MLflow ?? --> experiment / model 저장.
  - Spark structured streaming support with kafka ? 
* Infra : VPC, S3, EC2, Glue or EMR Spark
* Dataset : Giga byte 이상의 데이터타 셋 확보 필요.. (Regression or Classification 용)
* Storage : HDFS(EMR), S3
* Monitoring : cloudwatch X -> prometheus & grafana O
    
올해 새롭게 만들 워크샵 / 빌드하자 ^_^


## ##

* [#1. Airflow 설치하기](https://github.com/gnosia93/airflow-on-aws/blob/main/tutorial/airflow-on-pc.md)

* [#2. AWS Glue 실행하기](https://github.com/gnosia93/airflow-on-aws/blob/main/tutorial/airflow_glue.md)


## 레퍼런스 ##

* https://aws.amazon.com/ko/blogs/korea/build-end-to-end-machine-learning-workflows-with-amazon-sagemaker-and-apache-airflow/
* https://aws.amazon.com/blogs/big-data/simplify-aws-glue-job-orchestration-and-monitoring-with-amazon-mwaa/
* https://towardsdatascience.com/data-pipeline-with-airflow-and-aws-tools-s3-lambda-glue-18585d269761
* https://louisdev.tistory.com/8
* https://burning-dba.tistory.com/169
