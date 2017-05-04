* Initial test (before any authorisations are granted)

```
[ec2-user@ip-172-31-0-65 ~]$ kinit llibman@CLOUDERA-LLIBMAN.COM
Password for llibman@CLOUDERA-LLIBMAN.COM: 
[ec2-user@ip-172-31-0-65 ~]$ beeline
Beeline version 1.1.0-cdh5.9.2 by Apache Hive
beeline> !connect jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-0-65.ap-southeast-2.compute.internal@CLOUDERA-LLIBMAN.COM
scan complete in 1ms
Connecting to jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-0-65.ap-southeast-2.compute.internal@CLOUDERA-LLIBMAN.COM
Connected to: Apache Hive (version 1.1.0-cdh5.9.2)
Driver: Hive JDBC (version 1.1.0-cdh5.9.2)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://localhost:10000/default> SHOW TABLES;
INFO  : Compiling command(queryId=hive_20170504010707_efe33cdb-d618-4c92-a754-6b5c59eb0fe8): SHOW TABLES
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170504010707_efe33cdb-d618-4c92-a754-6b5c59eb0fe8); Time taken: 0.061 seconds
INFO  : Executing command(queryId=hive_20170504010707_efe33cdb-d618-4c92-a754-6b5c59eb0fe8): SHOW TABLES
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170504010707_efe33cdb-d618-4c92-a754-6b5c59eb0fe8); Time taken: 0.147 seconds
INFO  : OK
+-----------+--+
| tab_name  |
+-----------+--+
+-----------+--+
No rows selected (0.302 seconds)
0: jdbc:hive2://localhost:10000/default> Closing: 0: jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-0-65.ap-southeast-2.compute.internal@CLOUDERA-LLIBMAN.COM
```

* As user 'george'

```
[george@ip-172-31-0-65 ~]$ kinit george
Password for george@CLOUDERA-LLIBMAN.COM: 
[george@ip-172-31-0-65 ~]$ beeline
Beeline version 1.1.0-cdh5.9.2 by Apache Hive
beeline> !connect jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-0-65.ap-southeast-2.compute.internal@CLOUDERA-LLIBMAN.COM
scan complete in 2ms
Connecting to jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-0-65.ap-southeast-2.compute.internal@CLOUDERA-LLIBMAN.COM
Connected to: Apache Hive (version 1.1.0-cdh5.9.2)
Driver: Hive JDBC (version 1.1.0-cdh5.9.2)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://localhost:10000/default> SHOW TABLES;
INFO  : Compiling command(queryId=hive_20170504011717_b3412cc3-09b3-43d1-8400-a7220062ef9d): SHOW TABLES
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170504011717_b3412cc3-09b3-43d1-8400-a7220062ef9d); Time taken: 0.065 seconds
INFO  : Executing command(queryId=hive_20170504011717_b3412cc3-09b3-43d1-8400-a7220062ef9d): SHOW TABLES
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170504011717_b3412cc3-09b3-43d1-8400-a7220062ef9d); Time taken: 0.141 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
4 rows selected (0.301 seconds)
0: jdbc:hive2://localhost:10000/default> Closing: 0: jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-0-65.ap-southeast-2.compute.internal@CLOUDERA-LLIBMAN.COM
```

* As user 'ferdinand'

```
[ferdinand@ip-172-31-0-65 ~]$ kinit ferdinand
Password for ferdinand@CLOUDERA-LLIBMAN.COM: 
[ferdinand@ip-172-31-0-65 ~]$ beeline
Beeline version 1.1.0-cdh5.9.2 by Apache Hive
beeline> !connect jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-0-65.ap-southeast-2.compute.internal@CLOUDERA-LLIBMAN.COM
scan complete in 2ms
Connecting to jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-0-65.ap-southeast-2.compute.internal@CLOUDERA-LLIBMAN.COM
Connected to: Apache Hive (version 1.1.0-cdh5.9.2)
Driver: Hive JDBC (version 1.1.0-cdh5.9.2)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://localhost:10000/default> SHOW TABLES;
INFO  : Compiling command(queryId=hive_20170504011818_61c9ddec-e86f-43a9-8e50-04017e998279): SHOW TABLES
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170504011818_61c9ddec-e86f-43a9-8e50-04017e998279); Time taken: 0.067 seconds
INFO  : Executing command(queryId=hive_20170504011818_61c9ddec-e86f-43a9-8e50-04017e998279): SHOW TABLES
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170504011818_61c9ddec-e86f-43a9-8e50-04017e998279); Time taken: 0.156 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| sample_07  |
+------------+--+
1 row selected (0.318 seconds)
0: jdbc:hive2://localhost:10000/default> Closing: 0: jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-0-65.ap-southeast-2.compute.internal@CLOUDERA-LLIBMAN.COM
```
