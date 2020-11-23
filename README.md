# 5600final
from pyspark.sql import SparkSession
spark = SparkSession.builder.appName('myproj').getOrCreate()
data = spark.read.csv('/FileStore/tables/UCI_Credit_Card.csv',inferSchema=True,header=True)
data.printSchema()
