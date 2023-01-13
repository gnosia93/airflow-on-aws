맥 노트북에 파이스팍을 설치해서 주피터 노트북과 연동하기 위한 과정입니다.

1. conda 설치
```
```

2. 각종 패키지 설치
```
(base) soonbeom@bcd07468d10a ~ % conda install -y openjdk
(base) soonbeom@bcd07468d10a ~ % conda install -y pyspark
(base) soonbeom@bcd07468d10a ~ % conda install -y -c conda-forge findspark
```

3. 파이 스파크가 제대로 설치되었는지 확인합니다.
```
(base) soonbeom@bcd07468d10a ~ % pyspark
Python 3.9.13 (main, Aug 25 2022, 18:29:29)
[Clang 12.0.0 ] :: Anaconda, Inc. on darwin
Type "help", "copyright", "credits" or "license" for more information.
WARNING: An illegal reflective access operation has occurred
WARNING: Illegal reflective access by org.apache.spark.unsafe.Platform (file:/opt/anaconda3/lib/python3.9/site-packages/pyspark/jars/spark-unsafe_2.12-3.2.1.jar) to constructor java.nio.DirectByteBuffer(long,int)
WARNING: Please consider reporting this to the maintainers of org.apache.spark.unsafe.Platform
WARNING: Use --illegal-access=warn to enable warnings of further illegal reflective access operations
WARNING: All illegal access operations will be denied in a future release
Using Spark's default log4j profile: org/apache/spark/log4j-defaults.properties
Setting default log level to "WARN".
To adjust logging level use sc.setLogLevel(newLevel). For SparkR, use setLogLevel(newLevel).
23/01/13 11:30:18 WARN NativeCodeLoader: Unable to load native-hadoop library for your platform... using builtin-java classes where applicable
Welcome to
      ____              __
     / __/__  ___ _____/ /__
    _\ \/ _ \/ _ `/ __/  '_/
   /__ / .__/\_,_/_/ /_/\_\   version 3.2.1
      /_/

Using Python version 3.9.13 (main, Aug 25 2022 18:29:29)
Spark context Web UI available at http://192.168.29.29:4040
Spark context available as 'sc' (master = local[*], app id = local-1673577019976).
SparkSession available as 'spark'.
>>>
```


## 참고자료 ##

* https://sparkbyexamples.com/pyspark/install-pyspark-in-anaconda-jupyter-notebook/
