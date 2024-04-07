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


## aws operator 설치 ##


## 참고자료 ##

* [[airflow] 맥 터미널에서 에어플로우 설치하기](https://velog.io/@jenori_dev/airflow-%EB%A7%A5-%ED%84%B0%EB%AF%B8%EB%84%90%EC%97%90%EC%84%9C-%EC%97%90%EC%96%B4%ED%94%8C%EB%A1%9C%EC%9A%B0-%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0)
