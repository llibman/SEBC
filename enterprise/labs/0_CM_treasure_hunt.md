* What is ubertask optimization?

```
An ubertask (or uber job) is a combination of mapper and reducer tasks that are run in the same YARN container (within an ApplicationMaster), thereby saving the overhead of creating a new container and firing up a separate JVM; it is particularly useful for applications with large numbers of small tasks. Can be enabled in CM via the mapreduce.job.ubertask.enable configuration parameter, and the thresholds for the tasks sizes are configured via mapreduce.job.ubertask.{maxmaps,maxreduces,maxbytes}.
```

* Where in CM is the Kerberos Security Realm value displayed?

```
The Kerberos Security Realm can be seen/configured under Administration->Settings/Kerberos (the default_realm parameter, set to HADOOP.COM by default).
```

* Which CDH service(s) host a property for enabling Kerberos authentication?

```
HDFS, YARN, and ZooKeeper have configuration properties for enabling Kerberos authentication.
```

* How do you upgrade the CM agents?

```
Hosts tab -> select all hosts (or only the ones to upgrade) -> Re-run Upgrade Wizard, then select "Yes, I would like to upgrade the Cloudera Manager Agent packages now." and continue as prompted. (Usually follows an upgrade of the CM software itself but can be done at any time.)
```

* Give the `tsquery` statement used to chart Hue's CPU utilization?
```
Found by selecting Hue -> Charts Library and clicking on "Open in Chart Builder" within the "CPU Cores Used" chart:

select cpu_system_rate + cpu_user_rate where category=ROLE and serviceName=$SERVICENAME
(where $SERVICENAME = hue)
```

* Name all the roles that make up the Hive service

```
Using Hive -> Instances -> Add Role Instances, the following options come up:
HMS (Hive Metastore Server, assigned to one node in my cluster)
WHCS (WebHCat Server, not assigned to any node in my cluster)
HS2 (HiveServer2, assigned to one node in my cluster)
G (Gateway, all nodes in the cluster)

* What steps must be completed before integrating Cloudera Manager with Kerberos?

```
From the Cloudera manager documentation on enabling Kerberos authentication, under "Prerequisites":

A working Kerberos key distribution center (KDC) must be set up in the relevant realm;
Kerberos client packages are installed in all the cluster hosts (or at least those that may be used to access the cluster).
```
