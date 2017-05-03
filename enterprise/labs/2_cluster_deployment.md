```
$ curl -u llibman http://54.206.92.109:7180/api/v2/cm/deployment
Enter host password for user 'llibman':
{
  "timestamp" : "2017-05-03T02:07:31.361Z",
  "clusters" : [ {
    "name" : "llibman",
    "version" : "CDH5",
    "services" : [ {
      "name" : "hive",
      "type" : "HIVE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "HIVEMETASTORE",
          "items" : [ {
            "name" : "hive_metastore_java_heapsize",
            "value" : "593494016"
          } ]
        }, {
          "roleType" : "HIVESERVER2",
          "items" : [ {
            "name" : "hiveserver2_java_heapsize",
            "value" : "593494016"
          }, {
            "name" : "hiveserver2_spark_driver_memory",
            "value" : "966367641"
          }, {
            "name" : "hiveserver2_spark_executor_cores",
            "value" : "4"
          }, {
            "name" : "hiveserver2_spark_executor_memory",
            "value" : "3432356249"
          }, {
            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
            "value" : "102"
          }, {
            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
            "value" : "577"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_metastore_database_host",
          "value" : "ip-172-31-1-127.ap-southeast-2.compute.internal"
        }, {
          "name" : "hive_metastore_database_name",
          "value" : "hive"
        }, {
          "name" : "hive_metastore_database_password",
          "value" : "cloudera"
        }, {
          "name" : "hive_metastore_database_user",
          "value" : "cloudera"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hive-GATEWAY-243ffb21edf0829466482c5e70c814af",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-083a05087e0591558"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-34c6999536a80676e05b2712fdc065d4",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-07ca88750cee57969"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-9103ad76f1d15acfad88906dac195dd3",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-059a180cc66229c31"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-cefc64cfbd39e888934f3b6826603480",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-068e5faf5a08080d3"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-e5ca87701ad7895cf33f9cfeba4149c1",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-0050337f5154308f0"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-HIVEMETASTORE-9103ad76f1d15acfad88906dac195dd3",
        "type" : "HIVEMETASTORE",
        "hostRef" : {
          "hostId" : "i-059a180cc66229c31"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "f3fk1isecd4yi57zbackbb0a6"
          } ]
        }
      }, {
        "name" : "hive-HIVESERVER2-9103ad76f1d15acfad88906dac195dd3",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "i-059a180cc66229c31"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "dkpbpxwfzd3fceof8z1bqq539"
          } ]
        }
      } ],
      "displayName" : "Hive"
    }, {
      "name" : "zookeeper",
      "type" : "ZOOKEEPER",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "SERVER",
          "items" : [ {
            "name" : "zookeeper_server_java_heapsize",
            "value" : "593494016"
          } ]
        } ],
        "items" : [ ]
      },
      "roles" : [ {
        "name" : "zookeeper-SERVER-9103ad76f1d15acfad88906dac195dd3",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-059a180cc66229c31"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "63zkqe3ophu8o3pzn8zcfrct9"
          }, {
            "name" : "serverId",
            "value" : "3"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-cefc64cfbd39e888934f3b6826603480",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-068e5faf5a08080d3"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1bdg8bor0xfsriyrl3zl8jl7t"
          }, {
            "name" : "serverId",
            "value" : "1"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-e5ca87701ad7895cf33f9cfeba4149c1",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-0050337f5154308f0"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6dek6uxs94focwqkvb3veyspy"
          }, {
            "name" : "serverId",
            "value" : "2"
          } ]
        }
      } ],
      "displayName" : "ZooKeeper"
    }, {
      "name" : "hue",
      "type" : "HUE",
      "config" : {
        "roleTypeConfigs" : [ ],
        "items" : [ {
          "name" : "database_host",
          "value" : "ip-172-31-1-127.ap-southeast-2.compute.internal"
        }, {
          "name" : "database_password",
          "value" : "cloudera"
        }, {
          "name" : "database_type",
          "value" : "mysql"
        }, {
          "name" : "database_user",
          "value" : "cloudera"
        }, {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "hue_webhdfs",
          "value" : "hdfs-HTTPFS-9103ad76f1d15acfad88906dac195dd3"
        }, {
          "name" : "oozie_service",
          "value" : "oozie"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hue-HUE_SERVER-9103ad76f1d15acfad88906dac195dd3",
        "type" : "HUE_SERVER",
        "hostRef" : {
          "hostId" : "i-059a180cc66229c31"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "am3pgboi6tvn4potjrqgzh1ix"
          }, {
            "name" : "secret_key",
            "value" : "emueFINB0do2zLBLP6T7MbPzF00bXm"
          } ]
        }
      } ],
      "displayName" : "Hue"
    }, {
      "name" : "oozie",
      "type" : "OOZIE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "OOZIE_SERVER",
          "items" : [ {
            "name" : "oozie_database_host",
            "value" : "ip-172-31-1-127.ap-southeast-2.compute.internal"
          }, {
            "name" : "oozie_database_password",
            "value" : "cloudera"
          }, {
            "name" : "oozie_database_type",
            "value" : "mysql"
          }, {
            "name" : "oozie_database_user",
            "value" : "cloudera"
          }, {
            "name" : "oozie_java_heapsize",
            "value" : "593494016"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "oozie-OOZIE_SERVER-9103ad76f1d15acfad88906dac195dd3",
        "type" : "OOZIE_SERVER",
        "hostRef" : {
          "hostId" : "i-059a180cc66229c31"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "681z0m3ixr7ippjyqipqikjsl"
          } ]
        }
      } ],
      "displayName" : "Oozie"
    }, {
      "name" : "yarn",
      "type" : "YARN",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "mapred_reduce_tasks",
            "value" : "6"
          }, {
            "name" : "mapred_submit_replication",
            "value" : "1"
          } ]
        }, {
          "roleType" : "JOBHISTORY",
          "items" : [ {
            "name" : "mr2_jobhistory_java_heapsize",
            "value" : "593494016"
          } ]
        }, {
          "roleType" : "NODEMANAGER",
          "items" : [ {
            "name" : "rm_cpu_shares",
            "value" : "1800"
          }, {
            "name" : "rm_io_weight",
            "value" : "900"
          }, {
            "name" : "yarn_nodemanager_heartbeat_interval_ms",
            "value" : "100"
          }, {
            "name" : "yarn_nodemanager_local_dirs",
            "value" : "/yarn/nm"
          }, {
            "name" : "yarn_nodemanager_log_dirs",
            "value" : "/yarn/container-logs"
          }, {
            "name" : "yarn_nodemanager_resource_cpu_vcores",
            "value" : "3"
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "3537"
          } ]
        }, {
          "roleType" : "RESOURCEMANAGER",
          "items" : [ {
            "name" : "resource_manager_java_heapsize",
            "value" : "593494016"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_mb",
            "value" : "4273"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_vcores",
            "value" : "3"
          } ]
        } ],
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs"
        }, {
          "name" : "rm_dirty",
          "value" : "false"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "90"
        }, {
          "name" : "yarn_service_cgroups",
          "value" : "false"
        }, {
          "name" : "yarn_service_lce_always",
          "value" : "false"
        }, {
          "name" : "zk_authorization_secret_key",
          "value" : "phAVt9cMfdEVIDfCZ6H1FhrQS6Hvi3"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "yarn-JOBHISTORY-9103ad76f1d15acfad88906dac195dd3",
        "type" : "JOBHISTORY",
        "hostRef" : {
          "hostId" : "i-059a180cc66229c31"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "e85lmvbbjvn93xmnpa3pe7h43"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-243ffb21edf0829466482c5e70c814af",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-083a05087e0591558"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9sjguduyswdnpw9n49d72dp3l"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-34c6999536a80676e05b2712fdc065d4",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-07ca88750cee57969"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "au9vl92a0xbok5dg11umn4dna"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-cefc64cfbd39e888934f3b6826603480",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-068e5faf5a08080d3"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "bkcinz1o3hlboemqo0kgqtla2"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-e5ca87701ad7895cf33f9cfeba4149c1",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-0050337f5154308f0"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9b5zdlrnerk3qx2r7jywnhpiy"
          } ]
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-9103ad76f1d15acfad88906dac195dd3",
        "type" : "RESOURCEMANAGER",
        "hostRef" : {
          "hostId" : "i-059a180cc66229c31"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_id",
            "value" : "48"
          }, {
            "name" : "role_jceks_password",
            "value" : "a7xa6l3j3p6y2zkzhgngosob7"
          } ]
        }
      } ],
      "displayName" : "YARN (MR2 Included)"
    }, {
      "name" : "hdfs",
      "type" : "HDFS",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "BALANCER",
          "items" : [ {
            "name" : "balancer_java_heapsize",
            "value" : "593494016"
          } ]
        }, {
          "roleType" : "DATANODE",
          "items" : [ {
            "name" : "datanode_java_heapsize",
            "value" : "1073741824"
          }, {
            "name" : "dfs_data_dir_list",
            "value" : "/dfs/dn"
          }, {
            "name" : "dfs_datanode_du_reserved",
            "value" : "6441190604"
          }, {
            "name" : "dfs_datanode_max_locked_memory",
            "value" : "4294967296"
          }, {
            "name" : "rm_cpu_shares",
            "value" : "200"
          }, {
            "name" : "rm_io_weight",
            "value" : "100"
          } ]
        }, {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "dfs_client_use_trash",
            "value" : "true"
          } ]
        }, {
          "roleType" : "JOURNALNODE",
          "items" : [ {
            "name" : "dfs_journalnode_edits_dir",
            "value" : "/dfs/journal"
          } ]
        }, {
          "roleType" : "NAMENODE",
          "items" : [ {
            "name" : "dfs_name_dir_list",
            "value" : "/dfs/nn"
          }, {
            "name" : "dfs_namenode_servicerpc_address",
            "value" : "8022"
          }, {
            "name" : "namenode_java_heapsize",
            "value" : "593494016"
          } ]
        }, {
          "roleType" : "SECONDARYNAMENODE",
          "items" : [ {
            "name" : "fs_checkpoint_dir_list",
            "value" : "/dfs/snn"
          }, {
            "name" : "secondary_namenode_java_heapsize",
            "value" : "593494016"
          } ]
        } ],
        "items" : [ {
          "name" : "dfs_ha_fencing_cloudera_manager_secret_key",
          "value" : "43m7y35ysLqqYNKNP8k8sLM4ZBsXe1"
        }, {
          "name" : "dfs_ha_fencing_methods",
          "value" : "shell(true)"
        }, {
          "name" : "fc_authorization_secret_key",
          "value" : "Gd7F8fsN6OqUv2HFNIEu0X34Bg8a3E"
        }, {
          "name" : "http_auth_signature_secret",
          "value" : "VKnPoz2mf5llwMjW5xmlR73prleFBD"
        }, {
          "name" : "rm_dirty",
          "value" : "false"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "10"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hdfs-BALANCER-9103ad76f1d15acfad88906dac195dd3",
        "type" : "BALANCER",
        "hostRef" : {
          "hostId" : "i-059a180cc66229c31"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-DATANODE-243ffb21edf0829466482c5e70c814af",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-083a05087e0591558"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "djzgyktcly8p473ocly77hwq7"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-34c6999536a80676e05b2712fdc065d4",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-07ca88750cee57969"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "8jrobpf9rs6cr9z9vrfqfncrf"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-cefc64cfbd39e888934f3b6826603480",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-068e5faf5a08080d3"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2028ljbf2tyo3ry4c9nvnwqid"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-e5ca87701ad7895cf33f9cfeba4149c1",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-0050337f5154308f0"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2e2umefregwiaeqhk1ei6jsx7"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-243ffb21edf0829466482c5e70c814af",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "i-083a05087e0591558"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1pqvjlzhgluaq8813mbce2jgx"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-9103ad76f1d15acfad88906dac195dd3",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "i-059a180cc66229c31"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "69lll63i7m7e7xyywivl1qr19"
          } ]
        }
      }, {
        "name" : "hdfs-HTTPFS-9103ad76f1d15acfad88906dac195dd3",
        "type" : "HTTPFS",
        "hostRef" : {
          "hostId" : "i-059a180cc66229c31"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "d2uljibs6t05y5o3ed67s5jop"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-34c6999536a80676e05b2712fdc065d4",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-07ca88750cee57969"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1rdd3whe5xo5glqp5bg6qd0zf"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-cefc64cfbd39e888934f3b6826603480",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-068e5faf5a08080d3"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "67a9o2t4a6h768vmmioakszgy"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-e5ca87701ad7895cf33f9cfeba4149c1",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-0050337f5154308f0"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "ar9unz7a8y9gki6lt577jlmrz"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-243ffb21edf0829466482c5e70c814af",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "i-083a05087e0591558"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "nameservice1"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "nameservice1"
          }, {
            "name" : "namenode_id",
            "value" : "58"
          }, {
            "name" : "role_jceks_password",
            "value" : "9ek53krkb3ds29u18eoi532cn"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-9103ad76f1d15acfad88906dac195dd3",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "i-059a180cc66229c31"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "nameservice1"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "nameservice1"
          }, {
            "name" : "namenode_id",
            "value" : "50"
          }, {
            "name" : "role_jceks_password",
            "value" : "cf2o8coqg5ut4voh082kql0hx"
          } ]
        }
      } ],
      "displayName" : "HDFS"
    } ]
  } ],
  "hosts" : [ {
    "hostId" : "i-059a180cc66229c31",
    "ipAddress" : "172.31.0.65",
    "hostname" : "ip-172-31-0-65.ap-southeast-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-068e5faf5a08080d3",
    "ipAddress" : "172.31.1.122",
    "hostname" : "ip-172-31-1-122.ap-southeast-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-07ca88750cee57969",
    "ipAddress" : "172.31.1.127",
    "hostname" : "ip-172-31-1-127.ap-southeast-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-0050337f5154308f0",
    "ipAddress" : "172.31.11.150",
    "hostname" : "ip-172-31-11-150.ap-southeast-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-083a05087e0591558",
    "ipAddress" : "172.31.2.141",
    "hostname" : "ip-172-31-2-141.ap-southeast-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  } ],
  "users" : [ {
    "name" : "__cloudera_internal_user__mgmt-EVENTSERVER-9103ad76f1d15acfad88906dac195dd3",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "0046f14fb6c9210c67f43c4fdf682e95d2860c6dd5cc49da5b4525f341233d91",
    "pwSalt" : -3239364268285767847,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-9103ad76f1d15acfad88906dac195dd3",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "3e1fa8e06cce81632b5cff399bb5069f84bebbdf2ef204c9cdea54cbd463d7df",
    "pwSalt" : -2839681117565791999,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-REPORTSMANAGER-9103ad76f1d15acfad88906dac195dd3",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "5f84f9c267201685e54b4e1b056c2d1527b2dd1e5a9c2ed39ab8265eeba0f6f2",
    "pwSalt" : 5359442169510545521,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-9103ad76f1d15acfad88906dac195dd3",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "600d845e835b045dc14d4e4bb93f331880822d1aea5caf793b7a73d54be902c5",
    "pwSalt" : 1583183452811733202,
    "pwLogin" : true
  }, {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ],
    "pwHash" : "afb0f28111f9f4615886a64c4260d385ee5e2f1298123d630b52983986b07094",
    "pwSalt" : -4176117471321252059,
    "pwLogin" : true
  }, {
    "name" : "llibman",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "87559332f8249230c6a4df1bc41c6160c467fdba406ee14cc76474114aa4d2f8",
    "pwSalt" : 1952748934959867020,
    "pwLogin" : true
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ],
    "pwHash" : "de62dad8346c2a89d742edd7f72ba75034702a8f6cc54f485320765821cfd596",
    "pwSalt" : -2798319127315191677,
    "pwLogin" : true
  } ],
  "versionInfo" : {
    "version" : "5.9.2",
    "buildUser" : "jenkins",
    "buildTimestamp" : "20170330-1814",
    "gitHash" : "822da28bff818f57fc1bfc3eafe3a550300ef1b0",
    "snapshot" : false
  },
  "managementService" : {
    "name" : "mgmt",
    "type" : "MGMT",
    "config" : {
      "roleTypeConfigs" : [ {
        "roleType" : "EVENTSERVER",
        "items" : [ {
          "name" : "event_server_heapsize",
          "value" : "593494016"
        } ]
      }, {
        "roleType" : "HOSTMONITOR",
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "805306368"
        } ]
      }, {
        "roleType" : "REPORTSMANAGER",
        "items" : [ {
          "name" : "headlamp_database_host",
          "value" : "ip-172-31-1-127.ap-southeast-2.compute.internal"
        }, {
          "name" : "headlamp_database_name",
          "value" : "rman"
        }, {
          "name" : "headlamp_database_password",
          "value" : "cloudera"
        }, {
          "name" : "headlamp_database_user",
          "value" : "cloudera"
        }, {
          "name" : "headlamp_heapsize",
          "value" : "593494016"
        } ]
      }, {
        "roleType" : "SERVICEMONITOR",
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "805306368"
        } ]
      } ],
      "items" : [ ]
    },
    "roles" : [ {
      "name" : "mgmt-ALERTPUBLISHER-9103ad76f1d15acfad88906dac195dd3",
      "type" : "ALERTPUBLISHER",
      "hostRef" : {
        "hostId" : "i-059a180cc66229c31"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "7c89a8tt3or6omhvfotgzfkwo"
        } ]
      }
    }, {
      "name" : "mgmt-EVENTSERVER-9103ad76f1d15acfad88906dac195dd3",
      "type" : "EVENTSERVER",
      "hostRef" : {
        "hostId" : "i-059a180cc66229c31"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "4byq9cjxxb3fi3v0vx4ll27pg"
        } ]
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-9103ad76f1d15acfad88906dac195dd3",
      "type" : "HOSTMONITOR",
      "hostRef" : {
        "hostId" : "i-059a180cc66229c31"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "bi9ie0cydbf8oalj95ck8md4a"
        } ]
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-9103ad76f1d15acfad88906dac195dd3",
      "type" : "REPORTSMANAGER",
      "hostRef" : {
        "hostId" : "i-059a180cc66229c31"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "7g8m2n8bi0icsqf9e8896jfb6"
        } ]
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-9103ad76f1d15acfad88906dac195dd3",
      "type" : "SERVICEMONITOR",
      "hostRef" : {
        "hostId" : "i-059a180cc66229c31"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "896igp4mkbhwiip5dx44m2etw"
        } ]
      }
    } ],
    "displayName" : "Cloudera Management Service"
  },
  "managerSettings" : {
    "items" : [ {
      "name" : "CLUSTER_STATS_START",
      "value" : "10/21/2012 14:00"
    }, {
      "name" : "PUBLIC_CLOUD_STATUS",
      "value" : "ON_PUBLIC_CLOUD"
    }, {
      "name" : "REMOTE_PARCEL_REPO_URLS",
      "value" : "https://archive.cloudera.com/cdh5/parcels/{latest_supported}/,https://archive.cloudera.com/cdh4/parcels/latest/,https://archive.cloudera.com/impala/parcels/latest/,https://archive.cloudera.com/search/parcels/latest/,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/latest/,https://archive.cloudera.com/kafka/parcels/latest/,https://archive.cloudera.com/navigator-keytrustee5/parcels/latest/,https://archive.cloudera.com/spark/parcels/latest/,https://archive.cloudera.com/sqoop-connectors/parcels/latest/"
    } ]
  }
}
```
