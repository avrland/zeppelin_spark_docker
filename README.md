Build image and run container
```
docker build -t zeppelin-pyspark .      
docker run -p 8080:8080 zeppelin-pyspark
```

Add files you'll use in path:

/opt/zeppelin

```python
%spark.pyspark
sf_data = spark.read.csv('fires_small.csv', header=True, inferSchema=True)
sf_data.printSchema()
```
