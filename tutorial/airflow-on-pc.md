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
pip install apache-airflow-providers-amazon
```
