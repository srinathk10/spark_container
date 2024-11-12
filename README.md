# spark_container
Running Spark container

## Enter Spark container

```
[xxx@xxx spark_container]$ docker exec -ti spark_container-spark-master-1 bash
I have no name!@2f460939a3d9:/opt/bitnami/spark$ ls
LICENSE  R	    RELEASE  conf	   data       examples	kubernetes  logs	  python  tmp	work
NOTICE	 README.md  bin      conf.default  derby.log  jars	licenses    metastore_db  sbin	  venv	yarn
```

## Running Spark SQL

```
I have no name!@2f460939a3d9:/opt/bitnami/spark$ ./bin/spark
spark-class          spark-connect-shell  spark-sql            sparkR
spark-class2.cmd     spark-shell          spark-submit
I have no name!@2f460939a3d9:/opt/bitnami/spark$ ./bin/spark-sql
Setting default log level to "WARN".
To adjust logging level use sc.setLogLevel(newLevel). For SparkR, use setLogLevel(newLevel).
24/11/12 20:11:01 WARN NativeCodeLoader: Unable to load native-hadoop library for your platform... using builtin-java classes where applicable
24/11/12 20:11:03 WARN HiveConf: HiveConf of name hive.stats.jdbc.timeout does not exist
24/11/12 20:11:03 WARN HiveConf: HiveConf of name hive.stats.retries.wait does not exist
24/11/12 20:11:04 WARN ObjectStore: Version information not found in metastore. hive.metastore.schema.verification is not enabled so recording the schema version 2.3.0
24/11/12 20:11:04 WARN ObjectStore: setMetaStoreSchemaVersion called but recording version is disabled: version = 2.3.0, comment = Set by MetaStore UNKNOWN@172.23.0.2
Spark Web UI available at http://2f460939a3d9:4040
Spark master: local[*], Application Id: local-1731442262660
spark-sql (default)> show tables;
24/11/12 20:11:17 WARN ObjectStore: Failed to get database global_temp, returning NoSuchObjectException
Time taken: 0.584 seconds
spark-sql (default)>
```
