* Name a source directory after your GitHub handle
* Name a target directory after your partner's GitHub handle

```
[hdfs@ip-172-31-1-127 ~]$ hadoop fs -mkdir /replicate
[hdfs@ip-172-31-1-127 ~]$ hadoop fs -mkdir /replicate/llibman
[hdfs@ip-172-31-1-127 ~]$ hadoop fs -mkdir /replicate/npreema
```

* Use `teragen` to create a 500 MB file

```
[hdfs@ip-172-31-1-127 ~]$ hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen 5000000 /replicate/llibman/teragen-llibman
17/05/02 02:49:14 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-0-65.ap-southeast-2.compute.internal/172.31.0.65:8032
17/05/02 02:49:15 INFO terasort.TeraSort: Generating 5000000 using 2
17/05/02 02:49:15 INFO mapreduce.JobSubmitter: number of splits:2
17/05/02 02:49:15 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1493706434150_0001
17/05/02 02:49:16 INFO impl.YarnClientImpl: Submitted application application_1493706434150_0001
17/05/02 02:49:16 INFO mapreduce.Job: The url to track the job: http://ip-172-31-0-65.ap-southeast-2.compute.internal:8088/proxy/application_1493706434150_0001/
17/05/02 02:49:16 INFO mapreduce.Job: Running job: job_1493706434150_0001
17/05/02 02:49:23 INFO mapreduce.Job: Job job_1493706434150_0001 running in uber mode : false
17/05/02 02:49:23 INFO mapreduce.Job:  map 0% reduce 0%
17/05/02 02:49:35 INFO mapreduce.Job:  map 50% reduce 0%
17/05/02 02:49:36 INFO mapreduce.Job:  map 100% reduce 0%
17/05/02 02:49:36 INFO mapreduce.Job: Job job_1493706434150_0001 completed successfully
17/05/02 02:49:36 INFO mapreduce.Job: Counters: 31
	File System Counters
		FILE: Number of bytes read=0
		FILE: Number of bytes written=251034
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=167
		HDFS: Number of bytes written=500000000
		HDFS: Number of read operations=8
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=4
	Job Counters 
		Launched map tasks=2
		Other local map tasks=2
		Total time spent by all maps in occupied slots (ms)=20795
		Total time spent by all reduces in occupied slots (ms)=0
		Total time spent by all map tasks (ms)=20795
		Total vcore-seconds taken by all map tasks=20795
		Total megabyte-seconds taken by all map tasks=21294080
	Map-Reduce Framework
		Map input records=5000000
		Map output records=5000000
		Input split bytes=167
		Spilled Records=0
		Failed Shuffles=0
		Merged Map outputs=0
		GC time elapsed (ms)=333
		CPU time spent (ms)=14550
		Physical memory (bytes) snapshot=744300544
		Virtual memory (bytes) snapshot=3165667328
		Total committed heap usage (bytes)=844103680
	org.apache.hadoop.examples.terasort.TeraGen$Counters
		CHECKSUM=10735710707299981
	File Input Format Counters 
		Bytes Read=0
	File Output Format Counters 
		Bytes Written=500000000
```

* Copy your partner's file to your target directory 
```
[hdfs@ip-172-31-1-127 ~]$ hadoop distcp hdfs://172.31.10.74/user/hduser/terasort-input/ hdfs://172.31.0.65/replicate/npreema/
17/05/02 03:14:18 INFO tools.DistCp: Input Options: DistCpOptions{atomicCommit=false, syncFolder=false, deleteMissing=false, ignoreFailures=false, overwrite=false, append=false, useDiff=false, useRdiff=false, fromSnapshot=null, toSnapshot=null, skipCRC=false, blocking=true, numListstatusThreads=0, maxMaps=20, mapBandwidth=100, sslConfigurationFile='null', copyStrategy='uniformsize', preserveStatus=[], preserveRawXattrs=false, atomicWorkPath=null, logPath=null, sourceFileListing=null, sourcePaths=[hdfs://172.31.10.74/user/hduser/terasort-input], targetPath=hdfs://172.31.0.65/replicate/npreema, targetPathExists=true, filtersFile='null'}
17/05/02 03:14:18 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-0-65.ap-southeast-2.compute.internal/172.31.0.65:8032
17/05/02 03:14:19 INFO tools.SimpleCopyListing: Paths (files+dirs) cnt = 4; dirCnt = 1
17/05/02 03:14:19 INFO tools.SimpleCopyListing: Build file listing completed.
17/05/02 03:14:19 INFO Configuration.deprecation: io.sort.mb is deprecated. Instead, use mapreduce.task.io.sort.mb
17/05/02 03:14:19 INFO Configuration.deprecation: io.sort.factor is deprecated. Instead, use mapreduce.task.io.sort.factor
17/05/02 03:14:19 INFO tools.DistCp: Number of paths in the copy list: 4
17/05/02 03:14:19 INFO tools.DistCp: Number of paths in the copy list: 4
17/05/02 03:14:19 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-0-65.ap-southeast-2.compute.internal/172.31.0.65:8032
17/05/02 03:14:19 INFO mapreduce.JobSubmitter: number of splits:3
17/05/02 03:14:20 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1493706434150_0002
17/05/02 03:14:20 INFO impl.YarnClientImpl: Submitted application application_1493706434150_0002
17/05/02 03:14:20 INFO mapreduce.Job: The url to track the job: http://ip-172-31-0-65.ap-southeast-2.compute.internal:8088/proxy/application_1493706434150_0002/
17/05/02 03:14:20 INFO tools.DistCp: DistCp job-id: job_1493706434150_0002
17/05/02 03:14:20 INFO mapreduce.Job: Running job: job_1493706434150_0002
17/05/02 03:14:26 INFO mapreduce.Job: Job job_1493706434150_0002 running in uber mode : false
17/05/02 03:14:26 INFO mapreduce.Job:  map 0% reduce 0%
17/05/02 03:14:36 INFO mapreduce.Job:  map 33% reduce 0%
17/05/02 03:14:40 INFO mapreduce.Job:  map 100% reduce 0%
17/05/02 03:14:40 INFO mapreduce.Job: Job job_1493706434150_0002 completed successfully
17/05/02 03:14:40 INFO mapreduce.Job: Counters: 33
	File System Counters
		FILE: Number of bytes read=0
		FILE: Number of bytes written=386028
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=500001693
		HDFS: Number of bytes written=500000000
		HDFS: Number of read operations=57
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=13
	Job Counters 
		Launched map tasks=3
		Other local map tasks=3
		Total time spent by all maps in occupied slots (ms)=31339
		Total time spent by all reduces in occupied slots (ms)=0
		Total time spent by all map tasks (ms)=31339
		Total vcore-seconds taken by all map tasks=31339
		Total megabyte-seconds taken by all map tasks=32091136
	Map-Reduce Framework
		Map input records=4
		Map output records=0
		Input split bytes=345
		Spilled Records=0
		Failed Shuffles=0
		Merged Map outputs=0
		GC time elapsed (ms)=275
		CPU time spent (ms)=11760
		Physical memory (bytes) snapshot=801624064
		Virtual memory (bytes) snapshot=4716695552
		Total committed heap usage (bytes)=1111490560
	File Input Format Counters 
		Bytes Read=1348
	File Output Format Counters 
		Bytes Written=0
	org.apache.hadoop.tools.mapred.CopyMapper$Counter
		BYTESCOPIED=500000000
		BYTESEXPECTED=500000000
		COPY=4
```

* Browse the results 

```
[hdfs@ip-172-31-1-127 ~]$ hdfs fsck /replicate -files -blocks
Connecting to namenode via http://ip-172-31-0-65.ap-southeast-2.compute.internal:50070
FSCK started by hdfs (auth:SIMPLE) from /172.31.1.127 for path /replicate at Tue May 02 03:22:53 EDT 2017
/replicate <dir>
/replicate/llibman <dir>
/replicate/llibman/teragen-llibman <dir>
/replicate/llibman/teragen-llibman/_SUCCESS 0 bytes, 0 block(s):  OK

/replicate/llibman/teragen-llibman/part-m-00000 250000000 bytes, 2 block(s):  OK
0. BP-704584653-172.31.0.65-1493695459701:blk_1073743138_2314 len=134217728 Live_repl=3
1. BP-704584653-172.31.0.65-1493695459701:blk_1073743139_2315 len=115782272 Live_repl=3

/replicate/llibman/teragen-llibman/part-m-00001 250000000 bytes, 2 block(s):  OK
0. BP-704584653-172.31.0.65-1493695459701:blk_1073743137_2313 len=134217728 Live_repl=3
1. BP-704584653-172.31.0.65-1493695459701:blk_1073743140_2316 len=115782272 Live_repl=3

/replicate/npreema <dir>
/replicate/npreema/terasort-input <dir>
/replicate/npreema/terasort-input/_SUCCESS 0 bytes, 0 block(s):  OK

/replicate/npreema/terasort-input/part-m-00000 250000000 bytes, 2 block(s):  OK
0. BP-704584653-172.31.0.65-1493695459701:blk_1073743180_2356 len=134217728 Live_repl=3
1. BP-704584653-172.31.0.65-1493695459701:blk_1073743183_2359 len=115782272 Live_repl=3

/replicate/npreema/terasort-input/part-m-00001 250000000 bytes, 2 block(s):  OK
0. BP-704584653-172.31.0.65-1493695459701:blk_1073743181_2357 len=134217728 Live_repl=3
1. BP-704584653-172.31.0.65-1493695459701:blk_1073743184_2360 len=115782272 Live_repl=3

Status: HEALTHY
 Total size:	1000000000 B
 Total dirs:	5
 Total files:	6
 Total symlinks:		0
 Total blocks (validated):	8 (avg. block size 125000000 B)
 Minimally replicated blocks:	8 (100.0 %)
 Over-replicated blocks:	0 (0.0 %)
 Under-replicated blocks:	0 (0.0 %)
 Mis-replicated blocks:		0 (0.0 %)
 Default replication factor:	3
 Average block replication:	3.0
 Corrupt blocks:		0
 Missing replicas:		0 (0.0 %)
 Number of data-nodes:		4
 Number of racks:		1
FSCK ended at Tue May 02 03:22:53 EDT 2017 in 4 milliseconds


The filesystem under path '/replicate' is HEALTHY
```
