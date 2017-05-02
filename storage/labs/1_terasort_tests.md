teragen:<br>
```
[llibman@ip-172-31-1-127 ~]$ time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen -Dmapred.map.tasks=4 -Ddfs.block.size=33554432 100000000 /user/llibman/terasort_test
17/05/02 01:31:19 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-0-65.ap-southeast-2.compute.internal/172.31.0.65:8032
17/05/02 01:31:20 INFO terasort.TeraSort: Generating 100000000 using 4
17/05/02 01:31:20 INFO mapreduce.JobSubmitter: number of splits:4
17/05/02 01:31:20 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
17/05/02 01:31:20 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize
17/05/02 01:31:20 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1493697719130_0001
17/05/02 01:31:21 INFO impl.YarnClientImpl: Submitted application application_1493697719130_0001
17/05/02 01:31:21 INFO mapreduce.Job: The url to track the job: http://ip-172-31-0-65.ap-southeast-2.compute.internal:8088/proxy/application_1493697719130_0001/
17/05/02 01:31:21 INFO mapreduce.Job: Running job: job_1493697719130_0001
17/05/02 01:31:28 INFO mapreduce.Job: Job job_1493697719130_0001 running in uber mode : false
17/05/02 01:31:28 INFO mapreduce.Job:  map 0% reduce 0%
17/05/02 01:31:40 INFO mapreduce.Job:  map 4% reduce 0%
17/05/02 01:31:41 INFO mapreduce.Job:  map 8% reduce 0%
17/05/02 01:31:43 INFO mapreduce.Job:  map 10% reduce 0%
17/05/02 01:31:44 INFO mapreduce.Job:  map 12% reduce 0%
17/05/02 01:31:46 INFO mapreduce.Job:  map 13% reduce 0%
17/05/02 01:31:47 INFO mapreduce.Job:  map 15% reduce 0%
17/05/02 01:31:49 INFO mapreduce.Job:  map 16% reduce 0%
17/05/02 01:31:52 INFO mapreduce.Job:  map 17% reduce 0%
17/05/02 01:31:53 INFO mapreduce.Job:  map 18% reduce 0%
17/05/02 01:31:55 INFO mapreduce.Job:  map 19% reduce 0%
17/05/02 01:32:01 INFO mapreduce.Job:  map 20% reduce 0%
17/05/02 01:32:02 INFO mapreduce.Job:  map 21% reduce 0%
17/05/02 01:32:05 INFO mapreduce.Job:  map 22% reduce 0%
17/05/02 01:32:08 INFO mapreduce.Job:  map 24% reduce 0%
17/05/02 01:32:10 INFO mapreduce.Job:  map 27% reduce 0%
17/05/02 01:32:11 INFO mapreduce.Job:  map 28% reduce 0%
17/05/02 01:32:13 INFO mapreduce.Job:  map 29% reduce 0%
17/05/02 01:32:14 INFO mapreduce.Job:  map 30% reduce 0%
17/05/02 01:32:16 INFO mapreduce.Job:  map 31% reduce 0%
17/05/02 01:32:17 INFO mapreduce.Job:  map 32% reduce 0%
17/05/02 01:32:19 INFO mapreduce.Job:  map 33% reduce 0%
17/05/02 01:32:20 INFO mapreduce.Job:  map 34% reduce 0%
17/05/02 01:32:22 INFO mapreduce.Job:  map 35% reduce 0%
17/05/02 01:32:23 INFO mapreduce.Job:  map 36% reduce 0%
17/05/02 01:32:25 INFO mapreduce.Job:  map 37% reduce 0%
17/05/02 01:32:26 INFO mapreduce.Job:  map 38% reduce 0%
17/05/02 01:32:31 INFO mapreduce.Job:  map 39% reduce 0%
17/05/02 01:32:32 INFO mapreduce.Job:  map 41% reduce 0%
17/05/02 01:32:34 INFO mapreduce.Job:  map 42% reduce 0%
17/05/02 01:32:35 INFO mapreduce.Job:  map 43% reduce 0%
17/05/02 01:32:37 INFO mapreduce.Job:  map 44% reduce 0%
17/05/02 01:32:38 INFO mapreduce.Job:  map 45% reduce 0%
17/05/02 01:32:40 INFO mapreduce.Job:  map 46% reduce 0%
17/05/02 01:32:41 INFO mapreduce.Job:  map 47% reduce 0%
17/05/02 01:32:43 INFO mapreduce.Job:  map 48% reduce 0%
17/05/02 01:32:44 INFO mapreduce.Job:  map 50% reduce 0%
17/05/02 01:32:46 INFO mapreduce.Job:  map 51% reduce 0%
17/05/02 01:32:47 INFO mapreduce.Job:  map 52% reduce 0%
17/05/02 01:32:49 INFO mapreduce.Job:  map 53% reduce 0%
17/05/02 01:32:50 INFO mapreduce.Job:  map 54% reduce 0%
17/05/02 01:32:52 INFO mapreduce.Job:  map 55% reduce 0%
17/05/02 01:32:53 INFO mapreduce.Job:  map 56% reduce 0%
17/05/02 01:32:55 INFO mapreduce.Job:  map 57% reduce 0%
17/05/02 01:32:56 INFO mapreduce.Job:  map 59% reduce 0%
17/05/02 01:32:58 INFO mapreduce.Job:  map 60% reduce 0%
17/05/02 01:32:59 INFO mapreduce.Job:  map 61% reduce 0%
17/05/02 01:33:01 INFO mapreduce.Job:  map 62% reduce 0%
17/05/02 01:33:02 INFO mapreduce.Job:  map 63% reduce 0%
17/05/02 01:33:05 INFO mapreduce.Job:  map 64% reduce 0%
17/05/02 01:33:06 INFO mapreduce.Job:  map 65% reduce 0%
17/05/02 01:33:08 INFO mapreduce.Job:  map 66% reduce 0%
17/05/02 01:33:09 INFO mapreduce.Job:  map 67% reduce 0%
17/05/02 01:33:11 INFO mapreduce.Job:  map 68% reduce 0%
17/05/02 01:33:12 INFO mapreduce.Job:  map 69% reduce 0%
17/05/02 01:33:14 INFO mapreduce.Job:  map 70% reduce 0%
17/05/02 01:33:15 INFO mapreduce.Job:  map 71% reduce 0%
17/05/02 01:33:17 INFO mapreduce.Job:  map 72% reduce 0%
17/05/02 01:33:18 INFO mapreduce.Job:  map 73% reduce 0%
17/05/02 01:33:20 INFO mapreduce.Job:  map 74% reduce 0%
17/05/02 01:33:21 INFO mapreduce.Job:  map 75% reduce 0%
17/05/02 01:33:29 INFO mapreduce.Job:  map 77% reduce 0%
17/05/02 01:33:30 INFO mapreduce.Job:  map 79% reduce 0%
17/05/02 01:33:32 INFO mapreduce.Job:  map 80% reduce 0%
17/05/02 01:33:33 INFO mapreduce.Job:  map 81% reduce 0%
17/05/02 01:33:35 INFO mapreduce.Job:  map 82% reduce 0%
17/05/02 01:33:36 INFO mapreduce.Job:  map 83% reduce 0%
17/05/02 01:33:38 INFO mapreduce.Job:  map 84% reduce 0%
17/05/02 01:33:39 INFO mapreduce.Job:  map 85% reduce 0%
17/05/02 01:33:41 INFO mapreduce.Job:  map 87% reduce 0%
17/05/02 01:33:42 INFO mapreduce.Job:  map 88% reduce 0%
17/05/02 01:33:44 INFO mapreduce.Job:  map 89% reduce 0%
17/05/02 01:33:45 INFO mapreduce.Job:  map 90% reduce 0%
17/05/02 01:33:47 INFO mapreduce.Job:  map 91% reduce 0%
17/05/02 01:33:48 INFO mapreduce.Job:  map 92% reduce 0%
17/05/02 01:33:50 INFO mapreduce.Job:  map 93% reduce 0%
17/05/02 01:33:51 INFO mapreduce.Job:  map 94% reduce 0%
17/05/02 01:33:53 INFO mapreduce.Job:  map 95% reduce 0%
17/05/02 01:33:54 INFO mapreduce.Job:  map 96% reduce 0%
17/05/02 01:33:56 INFO mapreduce.Job:  map 97% reduce 0%
17/05/02 01:33:57 INFO mapreduce.Job:  map 98% reduce 0%
17/05/02 01:33:59 INFO mapreduce.Job:  map 100% reduce 0%
17/05/02 01:34:00 INFO mapreduce.Job: Job job_1493697719130_0001 completed successfully
17/05/02 01:34:00 INFO mapreduce.Job: Counters: 31
	File System Counters
		FILE: Number of bytes read=0
		FILE: Number of bytes written=494424
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=344
		HDFS: Number of bytes written=10000000000
		HDFS: Number of read operations=16
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=8
	Job Counters 
		Launched map tasks=4
		Other local map tasks=4
		Total time spent by all maps in occupied slots (ms)=594570
		Total time spent by all reduces in occupied slots (ms)=0
		Total time spent by all map tasks (ms)=594570
		Total vcore-seconds taken by all map tasks=594570
		Total megabyte-seconds taken by all map tasks=608839680
	Map-Reduce Framework
		Map input records=100000000
		Map output records=100000000
		Input split bytes=344
		Spilled Records=0
		Failed Shuffles=0
		Merged Map outputs=0
		GC time elapsed (ms)=1362
		CPU time spent (ms)=150360
		Physical memory (bytes) snapshot=900902912
		Virtual memory (bytes) snapshot=6320586752
		Total committed heap usage (bytes)=806354944
	org.apache.hadoop.examples.terasort.TeraGen$Counters
		CHECKSUM=214760662691937609
	File Input Format Counters 
		Bytes Read=0
	File Output Format Counters 
		Bytes Written=10000000000

real	2m42.815s
user	0m5.889s
sys	0m0.311s
```

terasort:<br>
```
bman@ip-172-31-1-127 ~]$ time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar terasort /user/llibman/terasort_test /user/llibman/terasort_result
17/05/02 01:36:39 INFO terasort.TeraSort: starting
17/05/02 01:36:40 INFO input.FileInputFormat: Total input paths to process : 4
Spent 270ms computing base-splits.
Spent 5ms computing TeraScheduler splits.
Computing input splits took 276ms
Sampling 10 splits of 300
Making 6 from 100000 sampled records
Computing parititions took 828ms
Spent 1107ms computing partitions.
17/05/02 01:36:41 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-0-65.ap-southeast-2.compute.internal/172.31.0.65:8032
17/05/02 01:36:42 INFO mapreduce.JobSubmitter: number of splits:300
17/05/02 01:36:42 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1493697719130_0002
17/05/02 01:36:42 INFO impl.YarnClientImpl: Submitted application application_1493697719130_0002
17/05/02 01:36:42 INFO mapreduce.Job: The url to track the job: http://ip-172-31-0-65.ap-southeast-2.compute.internal:8088/proxy/application_1493697719130_0002/
17/05/02 01:36:42 INFO mapreduce.Job: Running job: job_1493697719130_0002
17/05/02 01:36:48 INFO mapreduce.Job: Job job_1493697719130_0002 running in uber mode : false
17/05/02 01:36:48 INFO mapreduce.Job:  map 0% reduce 0%
17/05/02 01:37:00 INFO mapreduce.Job:  map 2% reduce 0%
17/05/02 01:37:01 INFO mapreduce.Job:  map 4% reduce 0%
17/05/02 01:37:09 INFO mapreduce.Job:  map 6% reduce 0%
17/05/02 01:37:10 INFO mapreduce.Job:  map 7% reduce 0%
17/05/02 01:37:12 INFO mapreduce.Job:  map 8% reduce 0%
17/05/02 01:37:20 INFO mapreduce.Job:  map 10% reduce 0%
17/05/02 01:37:21 INFO mapreduce.Job:  map 11% reduce 0%
17/05/02 01:37:23 INFO mapreduce.Job:  map 12% reduce 0%
17/05/02 01:37:30 INFO mapreduce.Job:  map 14% reduce 0%
17/05/02 01:37:31 INFO mapreduce.Job:  map 15% reduce 0%
17/05/02 01:37:32 INFO mapreduce.Job:  map 16% reduce 0%
17/05/02 01:37:39 INFO mapreduce.Job:  map 17% reduce 0%
17/05/02 01:37:40 INFO mapreduce.Job:  map 18% reduce 0%
17/05/02 01:37:42 INFO mapreduce.Job:  map 20% reduce 0%
17/05/02 01:37:50 INFO mapreduce.Job:  map 22% reduce 0%
17/05/02 01:37:51 INFO mapreduce.Job:  map 23% reduce 0%
17/05/02 01:37:52 INFO mapreduce.Job:  map 24% reduce 0%
17/05/02 01:38:00 INFO mapreduce.Job:  map 26% reduce 0%
17/05/02 01:38:01 INFO mapreduce.Job:  map 27% reduce 0%
17/05/02 01:38:02 INFO mapreduce.Job:  map 28% reduce 0%
17/05/02 01:38:08 INFO mapreduce.Job:  map 29% reduce 0%
17/05/02 01:38:10 INFO mapreduce.Job:  map 30% reduce 0%
17/05/02 01:38:12 INFO mapreduce.Job:  map 32% reduce 0%
17/05/02 01:38:18 INFO mapreduce.Job:  map 33% reduce 0%
17/05/02 01:38:21 INFO mapreduce.Job:  map 35% reduce 0%
17/05/02 01:38:22 INFO mapreduce.Job:  map 36% reduce 0%
17/05/02 01:38:26 INFO mapreduce.Job:  map 37% reduce 0%
17/05/02 01:38:30 INFO mapreduce.Job:  map 38% reduce 0%
17/05/02 01:38:31 INFO mapreduce.Job:  map 39% reduce 0%
17/05/02 01:38:32 INFO mapreduce.Job:  map 40% reduce 0%
17/05/02 01:38:36 INFO mapreduce.Job:  map 41% reduce 0%
17/05/02 01:38:40 INFO mapreduce.Job:  map 42% reduce 0%
17/05/02 01:38:41 INFO mapreduce.Job:  map 43% reduce 0%
17/05/02 01:38:42 INFO mapreduce.Job:  map 44% reduce 0%
17/05/02 01:38:45 INFO mapreduce.Job:  map 45% reduce 0%
17/05/02 01:38:49 INFO mapreduce.Job:  map 46% reduce 0%
17/05/02 01:38:51 INFO mapreduce.Job:  map 47% reduce 0%
17/05/02 01:38:52 INFO mapreduce.Job:  map 48% reduce 0%
17/05/02 01:38:54 INFO mapreduce.Job:  map 49% reduce 0%
17/05/02 01:38:58 INFO mapreduce.Job:  map 50% reduce 0%
17/05/02 01:39:02 INFO mapreduce.Job:  map 52% reduce 0%
17/05/02 01:39:04 INFO mapreduce.Job:  map 53% reduce 0%
17/05/02 01:39:07 INFO mapreduce.Job:  map 54% reduce 0%
17/05/02 01:39:11 INFO mapreduce.Job:  map 55% reduce 0%
17/05/02 01:39:12 INFO mapreduce.Job:  map 56% reduce 0%
17/05/02 01:39:14 INFO mapreduce.Job:  map 57% reduce 0%
17/05/02 01:39:17 INFO mapreduce.Job:  map 58% reduce 0%
17/05/02 01:39:21 INFO mapreduce.Job:  map 59% reduce 0%
17/05/02 01:39:22 INFO mapreduce.Job:  map 60% reduce 0%
17/05/02 01:39:23 INFO mapreduce.Job:  map 61% reduce 0%
17/05/02 01:39:27 INFO mapreduce.Job:  map 62% reduce 0%
17/05/02 01:39:32 INFO mapreduce.Job:  map 64% reduce 0%
17/05/02 01:39:33 INFO mapreduce.Job:  map 65% reduce 0%
17/05/02 01:39:36 INFO mapreduce.Job:  map 66% reduce 0%
17/05/02 01:39:41 INFO mapreduce.Job:  map 67% reduce 0%
17/05/02 01:39:42 INFO mapreduce.Job:  map 68% reduce 0%
17/05/02 01:39:43 INFO mapreduce.Job:  map 69% reduce 0%
17/05/02 01:39:45 INFO mapreduce.Job:  map 70% reduce 0%
17/05/02 01:39:51 INFO mapreduce.Job:  map 71% reduce 0%
17/05/02 01:39:52 INFO mapreduce.Job:  map 73% reduce 0%
17/05/02 01:39:55 INFO mapreduce.Job:  map 74% reduce 0%
17/05/02 01:40:02 INFO mapreduce.Job:  map 76% reduce 0%
17/05/02 01:40:03 INFO mapreduce.Job:  map 77% reduce 0%
17/05/02 01:40:04 INFO mapreduce.Job:  map 78% reduce 0%
17/05/02 01:40:11 INFO mapreduce.Job:  map 79% reduce 0%
17/05/02 01:40:12 INFO mapreduce.Job:  map 80% reduce 0%
17/05/02 01:40:13 INFO mapreduce.Job:  map 82% reduce 0%
17/05/02 01:40:20 INFO mapreduce.Job:  map 83% reduce 0%
17/05/02 01:40:23 INFO mapreduce.Job:  map 85% reduce 0%
17/05/02 01:40:24 INFO mapreduce.Job:  map 86% reduce 0%
17/05/02 01:40:27 INFO mapreduce.Job:  map 86% reduce 2%
17/05/02 01:40:29 INFO mapreduce.Job:  map 86% reduce 3%
17/05/02 01:40:30 INFO mapreduce.Job:  map 86% reduce 5%
17/05/02 01:40:31 INFO mapreduce.Job:  map 86% reduce 6%
17/05/02 01:40:32 INFO mapreduce.Job:  map 86% reduce 7%
17/05/02 01:40:33 INFO mapreduce.Job:  map 87% reduce 8%
17/05/02 01:40:34 INFO mapreduce.Job:  map 88% reduce 11%
17/05/02 01:40:35 INFO mapreduce.Job:  map 88% reduce 14%
17/05/02 01:40:36 INFO mapreduce.Job:  map 88% reduce 16%
17/05/02 01:40:37 INFO mapreduce.Job:  map 88% reduce 17%
17/05/02 01:40:38 INFO mapreduce.Job:  map 88% reduce 18%
17/05/02 01:40:39 INFO mapreduce.Job:  map 88% reduce 20%
17/05/02 01:40:40 INFO mapreduce.Job:  map 88% reduce 21%
17/05/02 01:40:41 INFO mapreduce.Job:  map 88% reduce 23%
17/05/02 01:40:42 INFO mapreduce.Job:  map 88% reduce 24%
17/05/02 01:40:43 INFO mapreduce.Job:  map 89% reduce 25%
17/05/02 01:40:44 INFO mapreduce.Job:  map 90% reduce 26%
17/05/02 01:40:46 INFO mapreduce.Job:  map 90% reduce 28%
17/05/02 01:40:47 INFO mapreduce.Job:  map 90% reduce 29%
17/05/02 01:40:48 INFO mapreduce.Job:  map 90% reduce 30%
17/05/02 01:40:51 INFO mapreduce.Job:  map 91% reduce 30%
17/05/02 01:40:52 INFO mapreduce.Job:  map 92% reduce 30%
17/05/02 01:40:55 INFO mapreduce.Job:  map 92% reduce 31%
17/05/02 01:40:58 INFO mapreduce.Job:  map 93% reduce 31%
17/05/02 01:40:59 INFO mapreduce.Job:  map 94% reduce 31%
17/05/02 01:41:05 INFO mapreduce.Job:  map 95% reduce 31%
17/05/02 01:41:06 INFO mapreduce.Job:  map 96% reduce 31%
17/05/02 01:41:07 INFO mapreduce.Job:  map 96% reduce 32%
17/05/02 01:41:12 INFO mapreduce.Job:  map 97% reduce 32%
17/05/02 01:41:13 INFO mapreduce.Job:  map 98% reduce 32%
17/05/02 01:41:16 INFO mapreduce.Job:  map 98% reduce 33%
17/05/02 01:41:20 INFO mapreduce.Job:  map 100% reduce 33%
17/05/02 01:41:22 INFO mapreduce.Job:  map 100% reduce 37%
17/05/02 01:41:23 INFO mapreduce.Job:  map 100% reduce 46%
17/05/02 01:41:24 INFO mapreduce.Job:  map 100% reduce 57%
17/05/02 01:41:25 INFO mapreduce.Job:  map 100% reduce 65%
17/05/02 01:41:26 INFO mapreduce.Job:  map 100% reduce 68%
17/05/02 01:41:27 INFO mapreduce.Job:  map 100% reduce 69%
17/05/02 01:41:28 INFO mapreduce.Job:  map 100% reduce 71%
17/05/02 01:41:29 INFO mapreduce.Job:  map 100% reduce 72%
17/05/02 01:41:30 INFO mapreduce.Job:  map 100% reduce 74%
17/05/02 01:41:31 INFO mapreduce.Job:  map 100% reduce 76%
17/05/02 01:41:32 INFO mapreduce.Job:  map 100% reduce 77%
17/05/02 01:41:33 INFO mapreduce.Job:  map 100% reduce 78%
17/05/02 01:41:34 INFO mapreduce.Job:  map 100% reduce 80%
17/05/02 01:41:35 INFO mapreduce.Job:  map 100% reduce 82%
17/05/02 01:41:36 INFO mapreduce.Job:  map 100% reduce 84%
17/05/02 01:41:37 INFO mapreduce.Job:  map 100% reduce 85%
17/05/02 01:41:38 INFO mapreduce.Job:  map 100% reduce 86%
17/05/02 01:41:39 INFO mapreduce.Job:  map 100% reduce 89%
17/05/02 01:41:40 INFO mapreduce.Job:  map 100% reduce 90%
17/05/02 01:41:41 INFO mapreduce.Job:  map 100% reduce 91%
17/05/02 01:41:42 INFO mapreduce.Job:  map 100% reduce 93%
17/05/02 01:41:44 INFO mapreduce.Job:  map 100% reduce 95%
17/05/02 01:41:45 INFO mapreduce.Job:  map 100% reduce 97%
17/05/02 01:41:47 INFO mapreduce.Job:  map 100% reduce 99%
17/05/02 01:41:48 INFO mapreduce.Job:  map 100% reduce 100%
17/05/02 01:41:50 INFO mapreduce.Job: Job job_1493697719130_0002 completed successfully
17/05/02 01:41:50 INFO mapreduce.Job: Counters: 50
	File System Counters
		FILE: Number of bytes read=4448388743
		FILE: Number of bytes written=8829457474
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=10000048900
		HDFS: Number of bytes written=10000000000
		HDFS: Number of read operations=918
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=12
	Job Counters 
		Launched map tasks=300
		Launched reduce tasks=6
		Data-local map tasks=223
		Rack-local map tasks=77
		Total time spent by all maps in occupied slots (ms)=2522570
		Total time spent by all reduces in occupied slots (ms)=511535
		Total time spent by all map tasks (ms)=2522570
		Total time spent by all reduce tasks (ms)=511535
		Total vcore-seconds taken by all map tasks=2522570
		Total vcore-seconds taken by all reduce tasks=511535
		Total megabyte-seconds taken by all map tasks=2583111680
		Total megabyte-seconds taken by all reduce tasks=523811840
	Map-Reduce Framework
		Map input records=100000000
		Map output records=100000000
		Map output bytes=10200000000
		Map output materialized bytes=4342784689
		Input split bytes=48900
		Combine input records=0
		Combine output records=0
		Reduce input groups=100000000
		Reduce shuffle bytes=4342784689
		Reduce input records=100000000
		Reduce output records=100000000
		Spilled Records=200000000
		Shuffled Maps =1800
		Failed Shuffles=0
		Merged Map outputs=1800
		GC time elapsed (ms)=35237
		CPU time spent (ms)=1444990
		Physical memory (bytes) snapshot=145391259648
		Virtual memory (bytes) snapshot=483373473792
		Total committed heap usage (bytes)=171845877760
	Shuffle Errors
		BAD_ID=0
		CONNECTION=0
		IO_ERROR=0
		WRONG_LENGTH=0
		WRONG_MAP=0
		WRONG_REDUCE=0
	File Input Format Counters 
		Bytes Read=10000000000
	File Output Format Counters 
		Bytes Written=10000000000
17/05/02 01:41:50 INFO terasort.TeraSort: done

real	5m12.583s
user	0m8.929s
sys	0m0.449s
```
