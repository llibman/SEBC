* The hostname of the db server node:

```
[ec2-user@ip-172-31-2-59 ~]$ hostname -f
ip-172-31-2-59.ap-southeast-2.compute.internal
```

* The database server version:

```
[ec2-user@ip-172-31-2-59 ~]$ sudo mysql -u root -p
Enter password: 
Welcome to the MariaDB monitor.  Commands end with ; or \g.
Your MariaDB connection id is 7
Server version: 5.5.52-MariaDB MariaDB Server

Copyright (c) 2000, 2016, Oracle, MariaDB Corporation Ab and others.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

MariaDB [(none)]> select @@version;
+----------------+
| @@version      |
+----------------+
| 5.5.52-MariaDB |
+----------------+
1 row in set (0.00 sec)

```

* Listing the databases:

```
MariaDB [(none)]> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| hive               |
| hue                |
| mysql              |
| oozie              |
| performance_schema |
| rman               |
| scm                |
| sentry             |
| test               |
+--------------------+
10 rows in set (0.01 sec)
```
