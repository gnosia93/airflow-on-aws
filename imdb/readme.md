
* 압축하기
```
$ tar cvfz - ./ | split -b 20m - imdb.tar.gz
```

* 압축풀기
```
$ cat imdb.tar.gz* | tar xvfz - 
```

* spark gzip 파일 읽기
```
rdd = sc.textFile("data/label.gz")
print rdd.take(10)
```
