* Contents of the cloudera-manager.repo file<br>
(unchanged from as retrieved from the Cloudera website; already configured to use latest 5.x version)

```
[ec2-user@ip-172-31-2-59 ~]$ cat /etc/yum.repos.d/cloudera-manager.repo 
[cloudera-manager]
# Packages for Cloudera Manager, Version 5, on RedHat or CentOS 7 x86_64           	  
name=Cloudera Manager
baseurl=https://archive.cloudera.com/cm5/redhat/7/x86_64/cm/5/
gpgkey =https://archive.cloudera.com/cm5/redhat/7/x86_64/cm/RPM-GPG-KEY-cloudera    
gpgcheck = 1
```
