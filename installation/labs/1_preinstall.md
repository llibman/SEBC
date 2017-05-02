Check vm.swappiness on all your nodes
Set the value to 1 if necessary

```
$ sysctl vm.swappiness
vm.swappiness = 30
$ sudo sysctl vm.swappiness=1
vm.swappiness = 1
```

Show the mount attributes of your volume(s)

```
$ mount -v | grep "on / "
/dev/xvda2 on / type xfs (rw,relatime,seclabel,attr2,inode64,noquota)
```

If you have ext-based volumes, list the reserve space setting
XFS volumes do not support reserve space

```
(see above; this is an xfs volume)
```

Disable transparent hugepage support

```
$ cat /proc/meminfo | grep HugePages
AnonHugePages:     10240 kB
HugePages_Total:       0
HugePages_Free:        0
HugePages_Rsvd:        0
HugePages_Surp:        0
$ cat /sys/kernel/mm/transparent_hugepage/enabled
[always] madvise never
$ echo never > /sys/kernel/mm/transparent_hugepage/enabled
```

List your network interface configuration

```
$ ifconfig
eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 9001
        inet 172.31.1.127  netmask 255.255.240.0  broadcast 172.31.15.255
        inet6 fe80::5b:97ff:fe6b:6cab  prefixlen 64  scopeid 0x20<link>
        ether 02:5b:97:6b:6c:ab  txqueuelen 1000  (Ethernet)
        RX packets 1743  bytes 146627 (143.1 KiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 1197  bytes 158319 (154.6 KiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1  (Local Loopback)
        RX packets 4  bytes 340 (340.0 B)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 4  bytes 340 (340.0 B)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0
```

Show correct forward and reverse host lookups
For /etc/hosts, use getent
For DNS, use nslookup

```
$ sudo yum install bind_utils
...

$ nslookup www.cloudera.com
erver:		172.31.0.2
Address:	172.31.0.2#53

Non-authoritative answer:
www.cloudera.com	canonical name = aem-prod-external-elb-1751714427.us-west-1.elb.amazonaws.com.
Name:	aem-prod-external-elb-1751714427.us-west-1.elb.amazonaws.com
Address: 52.52.88.106
Name:	aem-prod-external-elb-1751714427.us-west-1.elb.amazonaws.com
Address: 52.52.206.175

$ dig 52.52.88.106

	G 9.9.4-RedHat-9.9.4-38.el7_3.3 <<>> 52.52.88.106
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NXDOMAIN, id: 31007
;; flags: qr rd ra; QUERY: 1, ANSWER: 0, AUTHORITY: 1, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 4096
;; QUESTION SECTION:
;52.52.88.106.			IN	A

;; AUTHORITY SECTION:
.			60	IN	SOA	a.root-servers.net. nstld.verisign-grs.com. 2017050100 1800 900 604800 86400

;; Query time: 4 msec
;; SERVER: 172.31.0.2#53(172.31.0.2)
;; WHEN: Mon May 01 02:47:11 EDT 2017
;; MSG SIZE  rcvd: 116
```

Show the nscd service is running

```
$ sudo yum install nscd
...

$ sudo systemctl start nscd
$ systemctl status nscd
nscd.service - Name Service Cache Daemon
   Loaded: loaded (/usr/lib/systemd/system/nscd.service; disabled; vendor preset: disabled)
   Active: active (running) since Mon 2017-05-01 02:49:21 EDT; 14s ago
  Process: 9653 ExecStart=/usr/sbin/nscd $NSCD_OPTIONS (code=exited, status=0/SUCCESS)
 Main PID: 9654 (nscd)
   CGroup: /system.slice/nscd.service
           9654 /usr/sbin/nscd
...
```

Show the ntpd service is running

```
$ sudo yum install ntp
...

$ sudo systemctl start ntpd
$ systemctl status ntpd
ntpd.service - Network Time Service
   Loaded: loaded (/usr/lib/systemd/system/ntpd.service; disabled; vendor preset: disabled)
   Active: active (running) since Mon 2017-05-01 02:51:57 EDT; 49s ago
  Process: 9735 ExecStart=/usr/sbin/ntpd -u ntp:ntp $OPTIONS (code=exited, status=0/SUCCESS)
 Main PID: 9736 (ntpd)
   CGroup: /system.slice/ntpd.service
           9736 /usr/sbin/ntpd -u ntp:ntp -g
...
```

