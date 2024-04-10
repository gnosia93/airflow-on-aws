
* 압축하기
```
$ tar cvfz - ./ | split -b 20m - imdb.tar.gz

$ ls -la
-rw-r--r--   1 soonbeom  staff  20971520  4 10 21:52 imdb.tar.gzaa
-rw-r--r--   1 soonbeom  staff  20971520  4 10 21:52 imdb.tar.gzab
-rw-r--r--   1 soonbeom  staff  20971520  4 10 21:52 imdb.tar.gzac
-rw-r--r--   1 soonbeom  staff  20971520  4 10 21:53 imdb.tar.gzad
-rw-r--r--   1 soonbeom  staff  12165120  4 10 21:53 imdb.tar.gzae
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
