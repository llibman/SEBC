* Create a `precious` directory in HDFS; copy the ZIP course file into it.

```
[llibman@ip-172-31-1-127 ~]$ hadoop fs -mkdir /user/llibman/precious
[llibman@ip-172-31-1-127 ~]$ hadoop fs -put SEBC.zip /user/llibman/precious/SEBC.zip
[llibman@ip-172-31-1-127 ~]$ hadoop fs -ls /user/llibman/precious/SEBC.zip
-rw-r--r--   3 llibman llibman     474169 2017-05-02 01:56 /user/llibman/precious/SEBC.zip
```

* Enable snapshots for `precious`

```
[hdfs@ip-172-31-1-127 ~]$ hdfs dfsadmin -allowSnapshot /user/llibman/precious
Allowing snaphot on /user/llibman/precious succeeded
```

* Create a snapshot called `sebc-hdfs-test`

```
[llibman@ip-172-31-1-127 ~]$ hadoop fs -createSnapshot /user/llibman/precious sebc-hdfs-test
Created snapshot /user/llibman/precious/.snapshot/sebc-hdfs-test
```

* Delete the directory

```
[llibman@ip-172-31-1-127 ~]$ hadoop fs -rm -r /user/llibman/precious
rm: Failed to move to trash: hdfs://ip-172-31-0-65.ap-southeast-2.compute.internal:8020/user/llibman/precious: The directory /user/llibman/precious cannot be deleted since /user/llibman/precious is snapshottable and already has snapshots
```

* Delete the ZIP file

```
[llibman@ip-172-31-1-127 ~]$ hadoop fs -rm /user/llibman/precious/SEBC.zip
17/05/02 02:14:27 INFO fs.TrashPolicyDefault: Moved: 'hdfs://ip-172-31-0-65.ap-southeast-2.compute.internal:8020/user/llibman/precious/SEBC.zip' to trash at: hdfs://ip-172-31-0-65.ap-southeast-2.compute.internal:8020/user/llibman/.Trash/Current/user/llibman/precious/SEBC.zip
```

* Restore the deleted file 

```
[llibman@ip-172-31-1-127 ~]$ hadoop fs -ls /user/llibman/precious/.snapshot/sebc-hdfs-test
Found 1 items
-rw-r--r--   3 llibman llibman     474169 2017-05-02 01:56 /user/llibman/precious/.snapshot/sebc-hdfs-test/SEBC.zip
[llibman@ip-172-31-1-127 ~]$ hadoop fs -cp /user/llibman/precious/.snapshot/sebc-hdfs-test/SEBC.zip /user/llibman/precious/SEBC.zip
```

