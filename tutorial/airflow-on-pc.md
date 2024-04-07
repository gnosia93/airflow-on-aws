## 에어플로우 설치 ##
아래의 명령어를 이용하여 PC에 airflow 를 설치합니다.

```
% pip install apache-airflow

% airflow info

% cd airflow
% ls -la
total 152
drwxr-xr-x    4 soonbeom  staff    128  4  7 16:30 .
drwxr-x---+ 109 soonbeom  staff   3488  4  7 16:30 ..
-rw-------    1 soonbeom  staff  76164  4  7 16:30 airflow.cfg
drwxr-xr-x    3 soonbeom  staff     96  4  7 16:30 logs

% mkdir dags

% airflow users create \
          --username admin \
          --firstname admin \
          --lastname admin \
          --role Admin \
          --email admin@example.org

% airflow db init

% airflow webserver -p 8080
[2024-04-07T17:43:28.831+0900] {configuration.py:2066} INFO - Creating new FAB webserver config file in: /Users/soonbeom/airflow/webserver_config.py
  ____________       _____________
 ____    |__( )_________  __/__  /________      __
____  /| |_  /__  ___/_  /_ __  /_  __ \_ | /| / /
___  ___ |  / _  /   _  __/ _  / / /_/ /_ |/ |/ /
 _/_/  |_/_/  /_/    /_/    /_/  \____/____/|__/
Running the Gunicorn Server with:
Workers: 4 sync
Host: 0.0.0.0:8080
Timeout: 120
Logfiles: - -
Access Logformat:
```

![](https://github.com/gnosia93/airflow-on-aws/blob/main/images/airflow-1.png)

![](https://github.com/gnosia93/airflow-on-aws/blob/main/images/airflow-2.png)


## aws 프로바이더 설치 ##
* https://airflow.apache.org/docs/apache-airflow-providers-amazon/stable/index.html
```
% pip install apache-airflow-providers-amazon

% pip list | grep boto
aiobotocore                              2.5.0
boto3                                    1.34.79
botocore                                 1.34.79
```

## 트러블 슈팅 ##

* aiobotocore 2.5.0 requires botocore<1.29.77,>=1.29.76, but you have botocore 1.34.79 which is incompatible
```
% python -m pip uninstall boto3 botocore
% python3 -m pip install boto3
```

## 레퍼런스 ##
* https://velog.io/@ujeongoh/Airflow-%EC%82%AC%EC%9A%A9%ED%95%98%EC%97%AC-AWS-%EC%84%9C%EB%B9%84%EC%8A%A4-%EC%97%B0%EA%B2%B0%ED%95%98%EA%B8%B0
