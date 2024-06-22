
### Prerequsite ###

This section go through how to remove airflow example. 

```
docker-compose down -v
```

change 'true' into 'false' like below. 
![](https://github.com/gnosia93/airflow-on-aws/blob/main/airflow-docker/images/docker-compose-1.png)


```
docker-compose up airflow-init
docker-compose up -d
```


As you can see, dag examples has been removed.
![](https://github.com/gnosia93/airflow-on-aws/blob/main/airflow-docker/images/airflow-remove-example.png)



### First Dag ###

## 레퍼런스 ##

* [Airflow DAG: create dag with bash operator!](https://www.youtube.com/watch?v=CLkzXrjrFKg&list=PLwFJcsJ61oujAqYpMp1kdUBcPG0sE0QMT&index=6)
