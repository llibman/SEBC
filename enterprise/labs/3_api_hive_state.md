* Find out the details of the currently running Hive service:

```
$ curl -u llibman http://54.206.92.109:7180/api/v2/clusters/llibman/services/hive
Enter host password for user 'llibman':
{
  "name" : "hive",
  "type" : "HIVE",
  "clusterRef" : {
    "clusterName" : "cluster"
  },
  "serviceUrl" : "http://ip-172-31-1-127.ap-southeast-2.compute.internal:7180/cmf/serviceRedirect/hive",
  "serviceState" : "STARTED",
  "healthSummary" : "GOOD",
  "healthChecks" : [ {
    "name" : "HIVE_HIVEMETASTORES_HEALTHY",
    "summary" : "GOOD"
  }, {
    "name" : "HIVE_HIVESERVER2S_HEALTHY",
    "summary" : "GOOD"
  } ],
  "configStale" : false,
  "maintenanceMode" : false,
  "maintenanceOwners" : [ ],
  "displayName" : "Hive"
}
```

* Stop the running Hive service:

```
$ curl -X POST -u llibman http://54.206.92.109:7180/api/v2/clusters/llibman/services/hive/commands/stop
Enter host password for user 'llibman':
{
  "id" : 455,
  "name" : "Stop",
  "startTime" : "2017-05-03T02:21:06.346Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}
```

* Confirm that it is stopped:

```
$ curl -u llibman http://54.206.92.109:7180/api/v2/clusters/llibman/services/hive              
Enter host password for user 'llibman':
{
  "name" : "hive",
  "type" : "HIVE",
  "clusterRef" : {
    "clusterName" : "cluster"
  },
  "serviceUrl" : "http://ip-172-31-1-127.ap-southeast-2.compute.internal:7180/cmf/serviceRedirect/hive",
  "serviceState" : "STOPPED",
  "healthSummary" : "DISABLED",
  "healthChecks" : [ {
    "name" : "HIVE_HIVEMETASTORES_HEALTHY",
    "summary" : "DISABLED"
  }, {
    "name" : "HIVE_HIVESERVER2S_HEALTHY",
    "summary" : "DISABLED"
  } ],
  "configStale" : false,
  "maintenanceMode" : false,
  "maintenanceOwners" : [ ],
  "displayName" : "Hive"
}
```

* Start the Hive service again:

```
$ curl -X POST -u llibman http://54.206.92.109:7180/api/v2/clusters/llibman/services/hive/commands/start
Enter host password for user 'llibman':
{
  "id" : 459,
  "name" : "Start",
  "startTime" : "2017-05-03T02:23:26.128Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}
```

* Check the status of the Hive service:

```
$ curl -u llibman http://54.206.92.109:7180/api/v2/clusters/llibman/services/hive
Enter host password for user 'llibman':
{
  "name" : "hive",
  "type" : "HIVE",
  "clusterRef" : {
    "clusterName" : "cluster"
  },
  "serviceUrl" : "http://ip-172-31-1-127.ap-southeast-2.compute.internal:7180/cmf/serviceRedirect/hive",
  "serviceState" : "STARTED",
  "healthSummary" : "GOOD",
  "healthChecks" : [ {
    "name" : "HIVE_HIVEMETASTORES_HEALTHY",
    "summary" : "GOOD"
  }, {
    "name" : "HIVE_HIVESERVER2S_HEALTHY",
    "summary" : "GOOD"
  } ],
  "configStale" : false,
  "maintenanceMode" : false,
  "maintenanceOwners" : [ ],
  "displayName" : "Hive"
}
```
