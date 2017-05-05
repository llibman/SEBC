* List the /etc/yum.repos.d directory (after creating a Cloudera manager repository there)

```
[ec2-user@ip-172-31-2-59 ~]$ ls /etc/yum.repos.d
cloudera-manager.repo  redhat-rhui-client-config.repo  rhui-load-balancers.conf
redhat.repo            redhat-rhui.repo
```

* The command for running scm_prepare_database.sh:<br>
(failed at first attempt; requires JDK to be installed first so had to do this before retrying)

```
[root@ip-172-31-2-59 ec2-user]# /usr/share/cmf/schema/scm_prepare_database.sh mysql scm cloudera cloudera
```
