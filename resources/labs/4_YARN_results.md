# The slowest run:

* Standard output (tera_16_1_512.out):
```
Using 16 mappers, 1 reducers, with 512MB container memory (80% allocated to JVM heap)
Spent 178ms computing base-splits.
Spent 4ms computing TeraScheduler splits.
Computing input splits took 183ms
Sampling 10 splits of 80
Making 1 from 100000 sampled records
Computing parititions took 605ms
Spent 791ms computing partitions.
```

* Standard error, including 'time' results (tera_16_1_512.err):
```
17/05/02 20:37:23 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-0-65.ap-southeast-2.compute.internal/172.31.0.65:8032
17/05/02 20:37:24 INFO terasort.TeraSort: Generating 100000000 using 16
17/05/02 20:37:24 INFO mapreduce.JobSubmitter: number of splits:16
17/05/02 20:37:24 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1493706434150_0016
17/05/02 20:37:24 INFO impl.YarnClientImpl: Submitted application application_1493706434150_0016
17/05/02 20:37:24 INFO mapreduce.Job: The url to track the job: http://ip-172-31-0-65.ap-southeast-2.compute.internal:8088/proxy/application_1493706434150_0016/
17/05/02 20:37:24 INFO mapreduce.Job: Running job: job_1493706434150_0016
17/05/02 20:37:30 INFO mapreduce.Job: Job job_1493706434150_0016 running in uber mode : false
17/05/02 20:37:30 INFO mapreduce.Job:  map 0% reduce 0%
17/05/02 20:37:43 INFO mapreduce.Job:  map 2% reduce 0%
17/05/02 20:37:44 INFO mapreduce.Job:  map 5% reduce 0%
17/05/02 20:37:45 INFO mapreduce.Job:  map 10% reduce 0%
17/05/02 20:37:46 INFO mapreduce.Job:  map 14% reduce 0%
17/05/02 20:37:47 INFO mapreduce.Job:  map 16% reduce 0%
17/05/02 20:37:48 INFO mapreduce.Job:  map 17% reduce 0%
17/05/02 20:37:49 INFO mapreduce.Job:  map 19% reduce 0%
17/05/02 20:37:50 INFO mapreduce.Job:  map 20% reduce 0%
17/05/02 20:37:51 INFO mapreduce.Job:  map 21% reduce 0%
17/05/02 20:37:52 INFO mapreduce.Job:  map 22% reduce 0%
17/05/02 20:37:53 INFO mapreduce.Job:  map 23% reduce 0%
17/05/02 20:37:54 INFO mapreduce.Job:  map 24% reduce 0%
17/05/02 20:37:55 INFO mapreduce.Job:  map 25% reduce 0%
17/05/02 20:37:56 INFO mapreduce.Job:  map 26% reduce 0%
17/05/02 20:37:57 INFO mapreduce.Job:  map 27% reduce 0%
17/05/02 20:37:58 INFO mapreduce.Job:  map 28% reduce 0%
17/05/02 20:38:00 INFO mapreduce.Job:  map 29% reduce 0%
17/05/02 20:38:01 INFO mapreduce.Job:  map 30% reduce 0%
17/05/02 20:38:02 INFO mapreduce.Job:  map 31% reduce 0%
17/05/02 20:38:04 INFO mapreduce.Job:  map 32% reduce 0%
17/05/02 20:38:05 INFO mapreduce.Job:  map 33% reduce 0%
17/05/02 20:38:07 INFO mapreduce.Job:  map 35% reduce 0%
17/05/02 20:38:08 INFO mapreduce.Job:  map 37% reduce 0%
17/05/02 20:38:10 INFO mapreduce.Job:  map 39% reduce 0%
17/05/02 20:38:11 INFO mapreduce.Job:  map 41% reduce 0%
17/05/02 20:38:12 INFO mapreduce.Job:  map 42% reduce 0%
17/05/02 20:38:13 INFO mapreduce.Job:  map 43% reduce 0%
17/05/02 20:38:14 INFO mapreduce.Job:  map 45% reduce 0%
17/05/02 20:38:16 INFO mapreduce.Job:  map 47% reduce 0%
17/05/02 20:38:17 INFO mapreduce.Job:  map 48% reduce 0%
17/05/02 20:38:19 INFO mapreduce.Job:  map 49% reduce 0%
17/05/02 20:38:23 INFO mapreduce.Job:  map 51% reduce 0%
17/05/02 20:38:24 INFO mapreduce.Job:  map 52% reduce 0%
17/05/02 20:38:26 INFO mapreduce.Job:  map 53% reduce 0%
17/05/02 20:38:28 INFO mapreduce.Job:  map 56% reduce 0%
17/05/02 20:38:32 INFO mapreduce.Job:  map 57% reduce 0%
17/05/02 20:38:33 INFO mapreduce.Job:  map 58% reduce 0%
17/05/02 20:38:35 INFO mapreduce.Job:  map 59% reduce 0%
17/05/02 20:38:36 INFO mapreduce.Job:  map 61% reduce 0%
17/05/02 20:38:37 INFO mapreduce.Job:  map 63% reduce 0%
17/05/02 20:38:38 INFO mapreduce.Job:  map 64% reduce 0%
17/05/02 20:38:39 INFO mapreduce.Job:  map 65% reduce 0%
17/05/02 20:38:41 INFO mapreduce.Job:  map 66% reduce 0%
17/05/02 20:38:42 INFO mapreduce.Job:  map 67% reduce 0%
17/05/02 20:38:43 INFO mapreduce.Job:  map 69% reduce 0%
17/05/02 20:38:48 INFO mapreduce.Job:  map 70% reduce 0%
17/05/02 20:38:49 INFO mapreduce.Job:  map 71% reduce 0%
17/05/02 20:38:50 INFO mapreduce.Job:  map 72% reduce 0%
17/05/02 20:38:51 INFO mapreduce.Job:  map 73% reduce 0%
17/05/02 20:38:52 INFO mapreduce.Job:  map 74% reduce 0%
17/05/02 20:38:54 INFO mapreduce.Job:  map 76% reduce 0%
17/05/02 20:38:55 INFO mapreduce.Job:  map 77% reduce 0%
17/05/02 20:38:57 INFO mapreduce.Job:  map 78% reduce 0%
17/05/02 20:38:58 INFO mapreduce.Job:  map 79% reduce 0%
17/05/02 20:38:59 INFO mapreduce.Job:  map 80% reduce 0%
17/05/02 20:39:00 INFO mapreduce.Job:  map 81% reduce 0%
17/05/02 20:39:01 INFO mapreduce.Job:  map 83% reduce 0%
17/05/02 20:39:03 INFO mapreduce.Job:  map 84% reduce 0%
17/05/02 20:39:04 INFO mapreduce.Job:  map 86% reduce 0%
17/05/02 20:39:06 INFO mapreduce.Job:  map 88% reduce 0%
17/05/02 20:39:07 INFO mapreduce.Job:  map 89% reduce 0%
17/05/02 20:39:08 INFO mapreduce.Job:  map 90% reduce 0%
17/05/02 20:39:09 INFO mapreduce.Job:  map 91% reduce 0%
17/05/02 20:39:10 INFO mapreduce.Job:  map 92% reduce 0%
17/05/02 20:39:11 INFO mapreduce.Job:  map 93% reduce 0%
17/05/02 20:39:12 INFO mapreduce.Job:  map 94% reduce 0%
17/05/02 20:39:13 INFO mapreduce.Job:  map 95% reduce 0%
17/05/02 20:39:15 INFO mapreduce.Job:  map 96% reduce 0%
17/05/02 20:39:16 INFO mapreduce.Job:  map 97% reduce 0%
17/05/02 20:39:19 INFO mapreduce.Job:  map 98% reduce 0%
17/05/02 20:39:21 INFO mapreduce.Job:  map 99% reduce 0%
17/05/02 20:39:22 INFO mapreduce.Job:  map 100% reduce 0%
17/05/02 20:39:23 INFO mapreduce.Job: Job job_1493706434150_0016 completed successfully
17/05/02 20:39:23 INFO mapreduce.Job: Counters: 31
	File System Counters
		FILE: Number of bytes read=0
		FILE: Number of bytes written=2010534
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=1370
		HDFS: Number of bytes written=10000000000
		HDFS: Number of read operations=64
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=32
	Job Counters 
		Launched map tasks=16
		Other local map tasks=16
		Total time spent by all maps in occupied slots (ms)=987834
		Total time spent by all reduces in occupied slots (ms)=0
		Total time spent by all map tasks (ms)=987834
		Total vcore-seconds taken by all map tasks=987834
		Total megabyte-seconds taken by all map tasks=1011542016
	Map-Reduce Framework
		Map input records=100000000
		Map output records=100000000
		Input split bytes=1370
		Spilled Records=0
		Failed Shuffles=0
		Merged Map outputs=0
		GC time elapsed (ms)=3432
		CPU time spent (ms)=223120
		Physical memory (bytes) snapshot=3154886656
		Virtual memory (bytes) snapshot=18130915328
		Total committed heap usage (bytes)=3828350976
	org.apache.hadoop.examples.terasort.TeraGen$Counters
		CHECKSUM=214760662691937609
	File Input Format Counters 
		Bytes Read=0
	File Output Format Counters 
		Bytes Written=10000000000

real	2m2.803s
user	0m6.634s
sys	0m0.310s
17/05/02 20:39:24 INFO terasort.TeraSort: starting
17/05/02 20:39:26 INFO input.FileInputFormat: Total input paths to process : 16
17/05/02 20:39:26 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-0-65.ap-southeast-2.compute.internal/172.31.0.65:8032
17/05/02 20:39:27 INFO mapreduce.JobSubmitter: number of splits:80
17/05/02 20:39:27 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1493706434150_0017
17/05/02 20:39:27 INFO impl.YarnClientImpl: Submitted application application_1493706434150_0017
17/05/02 20:39:27 INFO mapreduce.Job: The url to track the job: http://ip-172-31-0-65.ap-southeast-2.compute.internal:8088/proxy/application_1493706434150_0017/
17/05/02 20:39:27 INFO mapreduce.Job: Running job: job_1493706434150_0017
17/05/02 20:39:34 INFO mapreduce.Job: Job job_1493706434150_0017 running in uber mode : false
17/05/02 20:39:34 INFO mapreduce.Job:  map 0% reduce 0%
17/05/02 20:39:46 INFO mapreduce.Job:  map 3% reduce 0%
17/05/02 20:39:47 INFO mapreduce.Job:  map 8% reduce 0%
17/05/02 20:39:48 INFO mapreduce.Job:  map 9% reduce 0%
17/05/02 20:39:49 INFO mapreduce.Job:  map 13% reduce 0%
17/05/02 20:39:50 INFO mapreduce.Job:  map 14% reduce 0%
17/05/02 20:39:57 INFO mapreduce.Job:  map 16% reduce 0%
17/05/02 20:40:02 INFO mapreduce.Job:  map 22% reduce 0%
17/05/02 20:40:03 INFO mapreduce.Job:  map 24% reduce 0%
17/05/02 20:40:04 INFO mapreduce.Job:  map 26% reduce 0%
17/05/02 20:40:05 INFO mapreduce.Job:  map 28% reduce 0%
17/05/02 20:40:08 INFO mapreduce.Job:  map 30% reduce 0%
17/05/02 20:40:16 INFO mapreduce.Job:  map 32% reduce 0%
17/05/02 20:40:18 INFO mapreduce.Job:  map 34% reduce 0%
17/05/02 20:40:19 INFO mapreduce.Job:  map 38% reduce 0%
17/05/02 20:40:20 INFO mapreduce.Job:  map 43% reduce 0%
17/05/02 20:40:21 INFO mapreduce.Job:  map 44% reduce 0%
17/05/02 20:40:30 INFO mapreduce.Job:  map 45% reduce 0%
17/05/02 20:40:31 INFO mapreduce.Job:  map 48% reduce 0%
17/05/02 20:40:33 INFO mapreduce.Job:  map 51% reduce 0%
17/05/02 20:40:34 INFO mapreduce.Job:  map 55% reduce 0%
17/05/02 20:40:35 INFO mapreduce.Job:  map 57% reduce 0%
17/05/02 20:40:42 INFO mapreduce.Job:  map 60% reduce 0%
17/05/02 20:40:44 INFO mapreduce.Job:  map 61% reduce 0%
17/05/02 20:40:45 INFO mapreduce.Job:  map 62% reduce 0%
17/05/02 20:40:48 INFO mapreduce.Job:  map 68% reduce 0%
17/05/02 20:40:49 INFO mapreduce.Job:  map 69% reduce 0%
17/05/02 20:40:50 INFO mapreduce.Job:  map 71% reduce 0%
17/05/02 20:40:52 INFO mapreduce.Job:  map 73% reduce 0%
17/05/02 20:40:53 INFO mapreduce.Job:  map 74% reduce 0%
17/05/02 20:40:57 INFO mapreduce.Job:  map 75% reduce 0%
17/05/02 20:41:00 INFO mapreduce.Job:  map 76% reduce 0%
17/05/02 20:41:01 INFO mapreduce.Job:  map 77% reduce 0%
17/05/02 20:41:02 INFO mapreduce.Job:  map 84% reduce 0%
17/05/02 20:41:03 INFO mapreduce.Job:  map 88% reduce 0%
17/05/02 20:41:12 INFO mapreduce.Job:  map 90% reduce 0%
17/05/02 20:41:13 INFO mapreduce.Job:  map 91% reduce 0%
17/05/02 20:41:15 INFO mapreduce.Job:  map 93% reduce 0%
17/05/02 20:41:16 INFO mapreduce.Job:  map 98% reduce 0%
17/05/02 20:41:17 INFO mapreduce.Job:  map 100% reduce 13%
17/05/02 20:41:20 INFO mapreduce.Job:  map 100% reduce 16%
17/05/02 20:41:23 INFO mapreduce.Job:  map 100% reduce 19%
17/05/02 20:41:27 INFO mapreduce.Job:  map 100% reduce 22%
17/05/02 20:41:30 INFO mapreduce.Job:  map 100% reduce 24%
17/05/02 20:41:33 INFO mapreduce.Job:  map 100% reduce 28%
17/05/02 20:41:36 INFO mapreduce.Job:  map 100% reduce 31%
17/05/02 20:41:39 INFO mapreduce.Job:  map 100% reduce 36%
17/05/02 20:41:42 INFO mapreduce.Job:  map 100% reduce 43%
17/05/02 20:41:45 INFO mapreduce.Job:  map 100% reduce 50%
17/05/02 20:41:48 INFO mapreduce.Job:  map 100% reduce 56%
17/05/02 20:41:51 INFO mapreduce.Job:  map 100% reduce 63%
17/05/02 20:41:54 INFO mapreduce.Job:  map 100% reduce 67%
17/05/02 20:41:57 INFO mapreduce.Job:  map 100% reduce 68%
17/05/02 20:42:00 INFO mapreduce.Job:  map 100% reduce 69%
17/05/02 20:42:03 INFO mapreduce.Job:  map 100% reduce 70%
17/05/02 20:42:09 INFO mapreduce.Job:  map 100% reduce 71%
17/05/02 20:42:12 INFO mapreduce.Job:  map 100% reduce 72%
17/05/02 20:42:15 INFO mapreduce.Job:  map 100% reduce 73%
17/05/02 20:42:18 INFO mapreduce.Job:  map 100% reduce 74%
17/05/02 20:42:21 INFO mapreduce.Job:  map 100% reduce 75%
17/05/02 20:42:24 INFO mapreduce.Job:  map 100% reduce 76%
17/05/02 20:42:27 INFO mapreduce.Job:  map 100% reduce 77%
17/05/02 20:42:30 INFO mapreduce.Job:  map 100% reduce 78%
17/05/02 20:42:36 INFO mapreduce.Job:  map 100% reduce 79%
17/05/02 20:42:39 INFO mapreduce.Job:  map 100% reduce 80%
17/05/02 20:42:42 INFO mapreduce.Job:  map 100% reduce 81%
17/05/02 20:42:45 INFO mapreduce.Job:  map 100% reduce 82%
17/05/02 20:42:48 INFO mapreduce.Job:  map 100% reduce 83%
17/05/02 20:42:51 INFO mapreduce.Job:  map 100% reduce 84%
17/05/02 20:42:54 INFO mapreduce.Job:  map 100% reduce 85%
17/05/02 20:42:57 INFO mapreduce.Job:  map 100% reduce 86%
17/05/02 20:43:00 INFO mapreduce.Job:  map 100% reduce 87%
17/05/02 20:43:06 INFO mapreduce.Job:  map 100% reduce 88%
17/05/02 20:43:09 INFO mapreduce.Job:  map 100% reduce 89%
17/05/02 20:43:12 INFO mapreduce.Job:  map 100% reduce 90%
17/05/02 20:43:15 INFO mapreduce.Job:  map 100% reduce 91%
17/05/02 20:43:18 INFO mapreduce.Job:  map 100% reduce 92%
17/05/02 20:43:24 INFO mapreduce.Job:  map 100% reduce 93%
17/05/02 20:43:27 INFO mapreduce.Job:  map 100% reduce 94%
17/05/02 20:43:30 INFO mapreduce.Job:  map 100% reduce 95%
17/05/02 20:43:33 INFO mapreduce.Job:  map 100% reduce 96%
17/05/02 20:43:36 INFO mapreduce.Job:  map 100% reduce 97%
17/05/02 20:43:42 INFO mapreduce.Job:  map 100% reduce 98%
17/05/02 20:43:45 INFO mapreduce.Job:  map 100% reduce 99%
17/05/02 20:43:48 INFO mapreduce.Job:  map 100% reduce 100%
17/05/02 20:44:00 INFO mapreduce.Job: Job job_1493706434150_0017 completed successfully
17/05/02 20:44:00 INFO mapreduce.Job: Counters: 50
	File System Counters
		FILE: Number of bytes read=5059858609
		FILE: Number of bytes written=9439508221
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=10000009760
		HDFS: Number of bytes written=10000000000
		HDFS: Number of read operations=243
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=2
	Job Counters 
		Launched map tasks=80
		Launched reduce tasks=1
		Data-local map tasks=79
		Rack-local map tasks=1
		Total time spent by all maps in occupied slots (ms)=998999
		Total time spent by all reduces in occupied slots (ms)=175732
		Total time spent by all map tasks (ms)=998999
		Total time spent by all reduce tasks (ms)=175732
		Total vcore-seconds taken by all map tasks=998999
		Total vcore-seconds taken by all reduce tasks=175732
		Total megabyte-seconds taken by all map tasks=1022974976
		Total megabyte-seconds taken by all reduce tasks=179949568
	Map-Reduce Framework
		Map input records=100000000
		Map output records=100000000
		Map output bytes=10200000000
		Map output materialized bytes=4369346559
		Input split bytes=9760
		Combine input records=0
		Combine output records=0
		Reduce input groups=100000000
		Reduce shuffle bytes=4369346559
		Reduce input records=100000000
		Reduce output records=100000000
		Spilled Records=215442818
		Shuffled Maps =80
		Failed Shuffles=0
		Merged Map outputs=80
		GC time elapsed (ms)=41638
		CPU time spent (ms)=827930
		Physical memory (bytes) snapshot=41364684800
		Virtual memory (bytes) snapshot=91915223040
		Total committed heap usage (bytes)=33474740224
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
17/05/02 20:44:00 INFO terasort.TeraSort: done

real	4m37.297s
user	0m8.621s
sys	0m0.388s
```

# The fastest run:

* Standard output (tera_16_2_512.out):
```
Using 16 mappers, 2 reducers, with 512MB container memory (80% allocated to JVM heap)
Spent 175ms computing base-splits.
Spent 3ms computing TeraScheduler splits.
Computing input splits took 179ms
Sampling 10 splits of 80
Making 2 from 100000 sampled records
Computing parititions took 801ms
Spent 982ms computing partitions.
```

* Standard error, including 'time' results (tera_16_2_512.err):
```
17/05/02 20:50:47 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-0-65.ap-southeast-2.compute.internal/172.31.0.65:8032
17/05/02 20:50:48 INFO terasort.TeraSort: Generating 100000000 using 16
17/05/02 20:50:48 INFO mapreduce.JobSubmitter: number of splits:16
17/05/02 20:50:48 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1493706434150_0020
17/05/02 20:50:48 INFO impl.YarnClientImpl: Submitted application application_1493706434150_0020
17/05/02 20:50:48 INFO mapreduce.Job: The url to track the job: http://ip-172-31-0-65.ap-southeast-2.compute.internal:8088/proxy/application_1493706434150_0020/
17/05/02 20:50:48 INFO mapreduce.Job: Running job: job_1493706434150_0020
17/05/02 20:50:54 INFO mapreduce.Job: Job job_1493706434150_0020 running in uber mode : false
17/05/02 20:50:54 INFO mapreduce.Job:  map 0% reduce 0%
17/05/02 20:51:06 INFO mapreduce.Job:  map 3% reduce 0%
17/05/02 20:51:07 INFO mapreduce.Job:  map 6% reduce 0%
17/05/02 20:51:08 INFO mapreduce.Job:  map 8% reduce 0%
17/05/02 20:51:09 INFO mapreduce.Job:  map 11% reduce 0%
17/05/02 20:51:10 INFO mapreduce.Job:  map 14% reduce 0%
17/05/02 20:51:11 INFO mapreduce.Job:  map 15% reduce 0%
17/05/02 20:51:12 INFO mapreduce.Job:  map 17% reduce 0%
17/05/02 20:51:13 INFO mapreduce.Job:  map 18% reduce 0%
17/05/02 20:51:14 INFO mapreduce.Job:  map 19% reduce 0%
17/05/02 20:51:15 INFO mapreduce.Job:  map 20% reduce 0%
17/05/02 20:51:16 INFO mapreduce.Job:  map 21% reduce 0%
17/05/02 20:51:17 INFO mapreduce.Job:  map 22% reduce 0%
17/05/02 20:51:19 INFO mapreduce.Job:  map 23% reduce 0%
17/05/02 20:51:20 INFO mapreduce.Job:  map 24% reduce 0%
17/05/02 20:51:22 INFO mapreduce.Job:  map 25% reduce 0%
17/05/02 20:51:23 INFO mapreduce.Job:  map 26% reduce 0%
17/05/02 20:51:24 INFO mapreduce.Job:  map 27% reduce 0%
17/05/02 20:51:27 INFO mapreduce.Job:  map 29% reduce 0%
17/05/02 20:51:30 INFO mapreduce.Job:  map 30% reduce 0%
17/05/02 20:51:31 INFO mapreduce.Job:  map 31% reduce 0%
17/05/02 20:51:32 INFO mapreduce.Job:  map 34% reduce 0%
17/05/02 20:51:33 INFO mapreduce.Job:  map 35% reduce 0%
17/05/02 20:51:34 INFO mapreduce.Job:  map 36% reduce 0%
17/05/02 20:51:35 INFO mapreduce.Job:  map 38% reduce 0%
17/05/02 20:51:36 INFO mapreduce.Job:  map 39% reduce 0%
17/05/02 20:51:38 INFO mapreduce.Job:  map 41% reduce 0%
17/05/02 20:51:39 INFO mapreduce.Job:  map 42% reduce 0%
17/05/02 20:51:40 INFO mapreduce.Job:  map 43% reduce 0%
17/05/02 20:51:41 INFO mapreduce.Job:  map 44% reduce 0%
17/05/02 20:51:42 INFO mapreduce.Job:  map 46% reduce 0%
17/05/02 20:51:45 INFO mapreduce.Job:  map 47% reduce 0%
17/05/02 20:51:47 INFO mapreduce.Job:  map 48% reduce 0%
17/05/02 20:51:49 INFO mapreduce.Job:  map 50% reduce 0%
17/05/02 20:51:50 INFO mapreduce.Job:  map 51% reduce 0%
17/05/02 20:51:51 INFO mapreduce.Job:  map 52% reduce 0%
17/05/02 20:51:53 INFO mapreduce.Job:  map 54% reduce 0%
17/05/02 20:51:55 INFO mapreduce.Job:  map 55% reduce 0%
17/05/02 20:51:56 INFO mapreduce.Job:  map 56% reduce 0%
17/05/02 20:51:57 INFO mapreduce.Job:  map 57% reduce 0%
17/05/02 20:51:59 INFO mapreduce.Job:  map 59% reduce 0%
17/05/02 20:52:01 INFO mapreduce.Job:  map 60% reduce 0%
17/05/02 20:52:02 INFO mapreduce.Job:  map 61% reduce 0%
17/05/02 20:52:03 INFO mapreduce.Job:  map 62% reduce 0%
17/05/02 20:52:04 INFO mapreduce.Job:  map 63% reduce 0%
17/05/02 20:52:05 INFO mapreduce.Job:  map 65% reduce 0%
17/05/02 20:52:06 INFO mapreduce.Job:  map 66% reduce 0%
17/05/02 20:52:07 INFO mapreduce.Job:  map 67% reduce 0%
17/05/02 20:52:08 INFO mapreduce.Job:  map 68% reduce 0%
17/05/02 20:52:09 INFO mapreduce.Job:  map 69% reduce 0%
17/05/02 20:52:11 INFO mapreduce.Job:  map 70% reduce 0%
17/05/02 20:52:12 INFO mapreduce.Job:  map 71% reduce 0%
17/05/02 20:52:14 INFO mapreduce.Job:  map 72% reduce 0%
17/05/02 20:52:15 INFO mapreduce.Job:  map 73% reduce 0%
17/05/02 20:52:17 INFO mapreduce.Job:  map 74% reduce 0%
17/05/02 20:52:20 INFO mapreduce.Job:  map 75% reduce 0%
17/05/02 20:52:21 INFO mapreduce.Job:  map 76% reduce 0%
17/05/02 20:52:22 INFO mapreduce.Job:  map 77% reduce 0%
17/05/02 20:52:23 INFO mapreduce.Job:  map 80% reduce 0%
17/05/02 20:52:25 INFO mapreduce.Job:  map 81% reduce 0%
17/05/02 20:52:28 INFO mapreduce.Job:  map 82% reduce 0%
17/05/02 20:52:29 INFO mapreduce.Job:  map 84% reduce 0%
17/05/02 20:52:30 INFO mapreduce.Job:  map 85% reduce 0%
17/05/02 20:52:32 INFO mapreduce.Job:  map 86% reduce 0%
17/05/02 20:52:33 INFO mapreduce.Job:  map 87% reduce 0%
17/05/02 20:52:35 INFO mapreduce.Job:  map 89% reduce 0%
17/05/02 20:52:38 INFO mapreduce.Job:  map 91% reduce 0%
17/05/02 20:52:39 INFO mapreduce.Job:  map 92% reduce 0%
17/05/02 20:52:41 INFO mapreduce.Job:  map 93% reduce 0%
17/05/02 20:52:42 INFO mapreduce.Job:  map 94% reduce 0%
17/05/02 20:52:44 INFO mapreduce.Job:  map 95% reduce 0%
17/05/02 20:52:45 INFO mapreduce.Job:  map 96% reduce 0%
17/05/02 20:52:47 INFO mapreduce.Job:  map 98% reduce 0%
17/05/02 20:52:48 INFO mapreduce.Job:  map 100% reduce 0%
17/05/02 20:52:49 INFO mapreduce.Job: Job job_1493706434150_0020 completed successfully
17/05/02 20:52:49 INFO mapreduce.Job: Counters: 31
	File System Counters
		FILE: Number of bytes read=0
		FILE: Number of bytes written=2010534
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=1370
		HDFS: Number of bytes written=10000000000
		HDFS: Number of read operations=64
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=32
	Job Counters 
		Launched map tasks=16
		Other local map tasks=16
		Total time spent by all maps in occupied slots (ms)=990812
		Total time spent by all reduces in occupied slots (ms)=0
		Total time spent by all map tasks (ms)=990812
		Total vcore-seconds taken by all map tasks=990812
		Total megabyte-seconds taken by all map tasks=1014591488
	Map-Reduce Framework
		Map input records=100000000
		Map output records=100000000
		Input split bytes=1370
		Spilled Records=0
		Failed Shuffles=0
		Merged Map outputs=0
		GC time elapsed (ms)=3217
		CPU time spent (ms)=223250
		Physical memory (bytes) snapshot=3095683072
		Virtual memory (bytes) snapshot=18133934080
		Total committed heap usage (bytes)=3821535232
	org.apache.hadoop.examples.terasort.TeraGen$Counters
		CHECKSUM=214760662691937609
	File Input Format Counters 
		Bytes Read=0
	File Output Format Counters 
		Bytes Written=10000000000

real	2m4.998s
user	0m6.302s
sys	0m0.367s
17/05/02 20:52:50 INFO terasort.TeraSort: starting
17/05/02 20:52:52 INFO input.FileInputFormat: Total input paths to process : 16
17/05/02 20:52:53 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-0-65.ap-southeast-2.compute.internal/172.31.0.65:8032
17/05/02 20:52:53 INFO mapreduce.JobSubmitter: number of splits:80
17/05/02 20:52:53 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1493706434150_0021
17/05/02 20:52:53 INFO impl.YarnClientImpl: Submitted application application_1493706434150_0021
17/05/02 20:52:53 INFO mapreduce.Job: The url to track the job: http://ip-172-31-0-65.ap-southeast-2.compute.internal:8088/proxy/application_1493706434150_0021/
17/05/02 20:52:53 INFO mapreduce.Job: Running job: job_1493706434150_0021
17/05/02 20:53:00 INFO mapreduce.Job: Job job_1493706434150_0021 running in uber mode : false
17/05/02 20:53:00 INFO mapreduce.Job:  map 0% reduce 0%
17/05/02 20:53:12 INFO mapreduce.Job:  map 2% reduce 0%
17/05/02 20:53:13 INFO mapreduce.Job:  map 3% reduce 0%
17/05/02 20:53:14 INFO mapreduce.Job:  map 8% reduce 0%
17/05/02 20:53:15 INFO mapreduce.Job:  map 11% reduce 0%
17/05/02 20:53:16 INFO mapreduce.Job:  map 13% reduce 0%
17/05/02 20:53:17 INFO mapreduce.Job:  map 14% reduce 0%
17/05/02 20:53:24 INFO mapreduce.Job:  map 15% reduce 0%
17/05/02 20:53:25 INFO mapreduce.Job:  map 16% reduce 0%
17/05/02 20:53:26 INFO mapreduce.Job:  map 17% reduce 0%
17/05/02 20:53:28 INFO mapreduce.Job:  map 21% reduce 0%
17/05/02 20:53:29 INFO mapreduce.Job:  map 23% reduce 0%
17/05/02 20:53:30 INFO mapreduce.Job:  map 26% reduce 0%
17/05/02 20:53:31 INFO mapreduce.Job:  map 27% reduce 0%
17/05/02 20:53:32 INFO mapreduce.Job:  map 28% reduce 0%
17/05/02 20:53:36 INFO mapreduce.Job:  map 30% reduce 0%
17/05/02 20:53:41 INFO mapreduce.Job:  map 31% reduce 0%
17/05/02 20:53:43 INFO mapreduce.Job:  map 33% reduce 0%
17/05/02 20:53:44 INFO mapreduce.Job:  map 35% reduce 0%
17/05/02 20:53:45 INFO mapreduce.Job:  map 37% reduce 0%
17/05/02 20:53:46 INFO mapreduce.Job:  map 40% reduce 0%
17/05/02 20:53:47 INFO mapreduce.Job:  map 41% reduce 0%
17/05/02 20:53:49 INFO mapreduce.Job:  map 44% reduce 0%
17/05/02 20:53:54 INFO mapreduce.Job:  map 45% reduce 0%
17/05/02 20:53:57 INFO mapreduce.Job:  map 46% reduce 0%
17/05/02 20:53:58 INFO mapreduce.Job:  map 48% reduce 0%
17/05/02 20:53:59 INFO mapreduce.Job:  map 50% reduce 0%
17/05/02 20:54:00 INFO mapreduce.Job:  map 51% reduce 0%
17/05/02 20:54:01 INFO mapreduce.Job:  map 56% reduce 0%
17/05/02 20:54:02 INFO mapreduce.Job:  map 57% reduce 0%
17/05/02 20:54:07 INFO mapreduce.Job:  map 58% reduce 0%
17/05/02 20:54:10 INFO mapreduce.Job:  map 60% reduce 0%
17/05/02 20:54:11 INFO mapreduce.Job:  map 62% reduce 0%
17/05/02 20:54:12 INFO mapreduce.Job:  map 63% reduce 0%
17/05/02 20:54:13 INFO mapreduce.Job:  map 65% reduce 0%
17/05/02 20:54:14 INFO mapreduce.Job:  map 67% reduce 0%
17/05/02 20:54:15 INFO mapreduce.Job:  map 70% reduce 0%
17/05/02 20:54:17 INFO mapreduce.Job:  map 71% reduce 0%
17/05/02 20:54:21 INFO mapreduce.Job:  map 72% reduce 0%
17/05/02 20:54:23 INFO mapreduce.Job:  map 73% reduce 0%
17/05/02 20:54:24 INFO mapreduce.Job:  map 76% reduce 0%
17/05/02 20:54:25 INFO mapreduce.Job:  map 78% reduce 0%
17/05/02 20:54:26 INFO mapreduce.Job:  map 79% reduce 0%
17/05/02 20:54:28 INFO mapreduce.Job:  map 81% reduce 0%
17/05/02 20:54:29 INFO mapreduce.Job:  map 84% reduce 0%
17/05/02 20:54:30 INFO mapreduce.Job:  map 85% reduce 0%
17/05/02 20:54:35 INFO mapreduce.Job:  map 88% reduce 0%
17/05/02 20:54:37 INFO mapreduce.Job:  map 89% reduce 0%
17/05/02 20:54:38 INFO mapreduce.Job:  map 90% reduce 0%
17/05/02 20:54:39 INFO mapreduce.Job:  map 91% reduce 0%
17/05/02 20:54:40 INFO mapreduce.Job:  map 93% reduce 0%
17/05/02 20:54:41 INFO mapreduce.Job:  map 94% reduce 0%
17/05/02 20:54:43 INFO mapreduce.Job:  map 96% reduce 0%
17/05/02 20:54:44 INFO mapreduce.Job:  map 98% reduce 10%
17/05/02 20:54:45 INFO mapreduce.Job:  map 100% reduce 10%
17/05/02 20:54:47 INFO mapreduce.Job:  map 100% reduce 22%
17/05/02 20:54:50 INFO mapreduce.Job:  map 100% reduce 27%
17/05/02 20:54:52 INFO mapreduce.Job:  map 100% reduce 30%
17/05/02 20:54:53 INFO mapreduce.Job:  map 100% reduce 31%
17/05/02 20:54:56 INFO mapreduce.Job:  map 100% reduce 35%
17/05/02 20:54:59 INFO mapreduce.Job:  map 100% reduce 59%
17/05/02 20:55:02 INFO mapreduce.Job:  map 100% reduce 68%
17/05/02 20:55:05 INFO mapreduce.Job:  map 100% reduce 69%
17/05/02 20:55:08 INFO mapreduce.Job:  map 100% reduce 71%
17/05/02 20:55:11 INFO mapreduce.Job:  map 100% reduce 73%
17/05/02 20:55:14 INFO mapreduce.Job:  map 100% reduce 74%
17/05/02 20:55:17 INFO mapreduce.Job:  map 100% reduce 76%
17/05/02 20:55:20 INFO mapreduce.Job:  map 100% reduce 78%
17/05/02 20:55:23 INFO mapreduce.Job:  map 100% reduce 79%
17/05/02 20:55:26 INFO mapreduce.Job:  map 100% reduce 81%
17/05/02 20:55:29 INFO mapreduce.Job:  map 100% reduce 83%
17/05/02 20:55:32 INFO mapreduce.Job:  map 100% reduce 85%
17/05/02 20:55:35 INFO mapreduce.Job:  map 100% reduce 86%
17/05/02 20:55:38 INFO mapreduce.Job:  map 100% reduce 88%
17/05/02 20:55:41 INFO mapreduce.Job:  map 100% reduce 89%
17/05/02 20:55:44 INFO mapreduce.Job:  map 100% reduce 91%
17/05/02 20:55:47 INFO mapreduce.Job:  map 100% reduce 93%
17/05/02 20:55:50 INFO mapreduce.Job:  map 100% reduce 94%
17/05/02 20:55:53 INFO mapreduce.Job:  map 100% reduce 95%
17/05/02 20:55:56 INFO mapreduce.Job:  map 100% reduce 97%
17/05/02 20:55:59 INFO mapreduce.Job:  map 100% reduce 99%
17/05/02 20:56:02 INFO mapreduce.Job:  map 100% reduce 100%
17/05/02 20:56:05 INFO mapreduce.Job: Job job_1493706434150_0021 completed successfully
17/05/02 20:56:05 INFO mapreduce.Job: Counters: 49
	File System Counters
		FILE: Number of bytes read=4682182364
		FILE: Number of bytes written=9061959856
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=10000009760
		HDFS: Number of bytes written=10000000000
		HDFS: Number of read operations=246
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=4
	Job Counters 
		Launched map tasks=80
		Launched reduce tasks=2
		Data-local map tasks=80
		Total time spent by all maps in occupied slots (ms)=1000455
		Total time spent by all reduces in occupied slots (ms)=180547
		Total time spent by all map tasks (ms)=1000455
		Total time spent by all reduce tasks (ms)=180547
		Total vcore-seconds taken by all map tasks=1000455
		Total vcore-seconds taken by all reduce tasks=180547
		Total megabyte-seconds taken by all map tasks=1024465920
		Total megabyte-seconds taken by all reduce tasks=184880128
	Map-Reduce Framework
		Map input records=100000000
		Map output records=100000000
		Map output bytes=10200000000
		Map output materialized bytes=4369346174
		Input split bytes=9760
		Combine input records=0
		Combine output records=0
		Reduce input groups=100000000
		Reduce shuffle bytes=4369346174
		Reduce input records=100000000
		Reduce output records=100000000
		Spilled Records=206701346
		Shuffled Maps =160
		Failed Shuffles=0
		Merged Map outputs=160
		GC time elapsed (ms)=40022
		CPU time spent (ms)=843720
		Physical memory (bytes) snapshot=42263592960
		Virtual memory (bytes) snapshot=93105770496
		Total committed heap usage (bytes)=34178334720
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
17/05/02 20:56:05 INFO terasort.TeraSort: done

real	3m16.052s
user	0m8.442s
sys	0m0.397s
```
