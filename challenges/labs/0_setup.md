* Using AWS m3.xlarge instances with 60GB volumes, running RHEL 7.3

* Public IP of the nodes (placed in my laptop's /etc/hosts for convenience):

```
54.206.74.185 cloudera1
54.206.127.105 cloudera2
54.206.34.149 cloudera3
54.206.127.98 cloudera4
54.252.130.89 cloudera5
```

* Internal host names in AWS:

```
$ ssh -i private_key.pem ec2-user@cloudera1 "hostname -f"
ip-172-31-2-59.ap-southeast-2.compute.internal
$ ssh -i private_key.pem ec2-user@cloudera2 "hostname -f"
ip-172-31-15-75.ap-southeast-2.compute.internal
$ ssh -i private_key.pem ec2-user@cloudera3 "hostname -f"
ip-172-31-2-98.ap-southeast-2.compute.internal
$ ssh -i private_key.pem ec2-user@cloudera4 "hostname -f"
ip-172-31-14-225.ap-southeast-2.compute.internal
$ ssh -i private_key.pem ec2-user@cloudera5 "hostname -f"
ip-172-31-1-42.ap-southeast-2.compute.internal
```

* Free disk space available on the nodes:

```
$ for n in 1 2 3 4 5; do ssh -i private_key.pem ec2-user@cloudera$n "df -k /"; done
Filesystem     1K-blocks    Used Available Use% Mounted on
/dev/xvda2      62902252 1002808  61899444   2% /
Filesystem     1K-blocks    Used Available Use% Mounted on
/dev/xvda2      62902252 1002804  61899448   2% /
Filesystem     1K-blocks    Used Available Use% Mounted on
/dev/xvda2      62902252 1002804  61899448   2% /
Filesystem     1K-blocks    Used Available Use% Mounted on
/dev/xvda2      62902252 1002948  61899304   2% /
Filesystem     1K-blocks    Used Available Use% Mounted on
/dev/xvda2      62902252 1002776  61899476   2% /
```

* Output of `yum repolist enabled`:

```
[ec2-user@ip-172-31-1-42 ~]$ yum repolist enabled
Loaded plugins: amazon-id, rhui-lb, search-disabled-repos
Repo rhui-REGION-client-config-server-7 forced skip_if_unavailable=True due to: /etc/pki/rhui/cdn.redhat.com-chain.crt
Repo rhui-REGION-client-config-server-7 forced skip_if_unavailable=True due to: /etc/pki/rhui/product/rhui-client-config-server-7.crt
Repo rhui-REGION-client-config-server-7 forced skip_if_unavailable=True due to: /etc/pki/rhui/rhui-client-config-server-7.key
Repo rhui-REGION-rhel-server-releases forced skip_if_unavailable=True due to: /etc/pki/rhui/cdn.redhat.com-chain.crt
Repo rhui-REGION-rhel-server-releases forced skip_if_unavailable=True due to: /etc/pki/rhui/product/content-rhel7.crt
Repo rhui-REGION-rhel-server-releases forced skip_if_unavailable=True due to: /etc/pki/rhui/content-rhel7.key
Repo rhui-REGION-rhel-server-rh-common forced skip_if_unavailable=True due to: /etc/pki/rhui/cdn.redhat.com-chain.crt
Repo rhui-REGION-rhel-server-rh-common forced skip_if_unavailable=True due to: /etc/pki/rhui/product/content-rhel7.crt
Repo rhui-REGION-rhel-server-rh-common forced skip_if_unavailable=True due to: /etc/pki/rhui/content-rhel7.key
Could not contact CDS load balancer rhui2-cds01.ap-southeast-2.aws.ce.redhat.com, trying others.


Could not contact any CDS load balancers: rhui2-cds01.ap-southeast-2.aws.ce.redhat.com, rhui2-cds02.ap-southeast-2.aws.ce.redhat.com.

```

* /etc/passwd entries for `cate` and `jemaine`:

```
cate:x:2300:2300::/home/cate:/bin/bash
jemaine:x:2900:2900::/home/jemaine:/bin/bash
```

* /etc/group entries for `kiwis` and `aussies`:

```
kiwis:x:2901:jemaine
aussies:x:2902:cate
```
