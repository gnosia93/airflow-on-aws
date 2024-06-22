This section describe how to install airflow with docker into your mac os desktop.
You need to install vscode first before installing airflow and then make a proejct named 'AIRFLOW-DOCKER' in your mac.  

![](https://github.com/gnosia93/airflow-on-aws/blob/main/airflow-docker/images/airflow-docker.png)


### Instructions ###

1. Install Docker Community Edition (CE) on your workstation


2. Fetching docker-compose.yaml

```
curl -LfO 'https://airflow.apache.org/docs/apache-airflow/2.9.2/docker-compose.yaml'
```

3. Setting the right Airflow user
```
mkdir -p ./dags ./logs ./plugins ./config
echo -e "AIRFLOW_UID=$(id -u)" > .env
```

4. Initialize the database
```
docker compose up airflow-init
```

5. Running Airflow as a daemon 
```
docker compose up -d
```

6. Check airflow daemon
```
% docker ps 
CONTAINER ID   IMAGE                  COMMAND                  CREATED          STATUS                    PORTS                    NAMES
68024e0e7430   apache/airflow:2.9.2   "/usr/bin/dumb-init …"   12 minutes ago   Up 11 minutes (healthy)   8080/tcp                 airflow-docker-airflow-worker-1
dae8576e748b   apache/airflow:2.9.2   "/usr/bin/dumb-init …"   12 minutes ago   Up 11 minutes (healthy)   8080/tcp                 airflow-docker-airflow-scheduler-1
a50cd79eadf7   apache/airflow:2.9.2   "/usr/bin/dumb-init …"   12 minutes ago   Up 11 minutes (healthy)   0.0.0.0:8080->8080/tcp   airflow-docker-airflow-webserver-1
8a47fc90846c   apache/airflow:2.9.2   "/usr/bin/dumb-init …"   12 minutes ago   Up 11 minutes (healthy)   8080/tcp                 airflow-docker-airflow-triggerer-1
e01c307e2672   redis:7.2-bookworm     "docker-entrypoint.s…"   15 minutes ago   Up 12 minutes (healthy)   6379/tcp                 airflow-docker-redis-1
b3a1a1daf761   postgres:13            "docker-entrypoint.s…"   15 minutes ago   Up 12 minutes (healthy)   5432/tcp                 airflow-docker-postgres-1
```


## 레퍼런스 ##

* [Airflow Docker: run Airflow 2.0 in docker container](https://www.youtube.com/watch?v=J6azvFhndLg&list=PLwFJcsJ61oujAqYpMp1kdUBcPG0sE0QMT&index=3)
* [Running Airflow in Docker](https://airflow.apache.org/docs/apache-airflow/stable/howto/docker-compose/index.html)
