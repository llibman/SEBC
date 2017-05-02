Check vm.swappiness on all your nodes<br>
Set the value to 1 if necessary<br>

<code>
$ sysctl vm.swappiness<br>
vm.swappiness = 30<br>
$ sudo sysctl vm.swappiness=1<br>
vm.swappiness = 1<br>
</code>

Show the mount attributes of your volume(s)<br>

<code>
$ mount -v | grep "on / "<br>
/dev/xvda2 on / type xfs (rw,relatime,seclabel,attr2,inode64,noquota)<br>
</code>

If you have ext-based volumes, list the reserve space setting<br>
XFS volumes do not support reserve space<br>

<code>
(see above; this is an xfs volume)<br>
</code>

Disable transparent hugepage support<br>

<code>
$ cat /proc/meminfo | grep HugePages<br>
AnonHugePages:     10240 kB<br>
HugePages_Total:       0<br>
HugePages_Free:        0<br>
HugePages_Rsvd:        0<br>
HugePages_Surp:        0<br>
$ cat /sys/kernel/mm/transparent_hugepage/enabled<br>
[always] madvise never<br>
$ echo never > /sys/kernel/mm/transparent_hugepage/enabled<br>
</code>

List your network interface configuration<br>

<code>
$ ifconfig
eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 9001<br>
        inet 172.31.1.127  netmask 255.255.240.0  broadcast 172.31.15.255<br>
        inet6 fe80::5b:97ff:fe6b:6cab  prefixlen 64  scopeid 0x20<link><br>
        ether 02:5b:97:6b:6c:ab  txqueuelen 1000  (Ethernet)<br>
        RX packets 1743  bytes 146627 (143.1 KiB)<br>
        RX errors 0  dropped 0  overruns 0  frame 0<br>
        TX packets 1197  bytes 158319 (154.6 KiB)<br>
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0<br>
<br>
lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536<br>
        inet 127.0.0.1  netmask 255.0.0.0<br>
        inet6 ::1  prefixlen 128  scopeid 0x10<host><br>
        loop  txqueuelen 1  (Local Loopback)<br>
        RX packets 4  bytes 340 (340.0 B)<br>
        RX errors 0  dropped 0  overruns 0  frame 0<br>
        TX packets 4  bytes 340 (340.0 B)<br>
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0<br>
</code>

Show correct forward and reverse host lookups<br>
For /etc/hosts, use getent<br>
For DNS, use nslookup<br>

<code>
$ sudo yum install bind_utils<br>
...<br>
<br>
$ nslookup www.cloudera.com<br>
erver:		172.31.0.2<br>
Address:	172.31.0.2#53<br>
<br>
Non-authoritative answer:<br>
www.cloudera.com	canonical name = aem-prod-external-elb-1751714427.us-west-1.elb.amazonaws.com.<br>
Name:	aem-prod-external-elb-1751714427.us-west-1.elb.amazonaws.com<br>
Address: 52.52.88.106<br>
Name:	aem-prod-external-elb-1751714427.us-west-1.elb.amazonaws.com<br>
Address: 52.52.206.175<br>
<br>
$ dig 52.52.88.106<br>
<br>
	G 9.9.4-RedHat-9.9.4-38.el7_3.3 <<>> 52.52.88.106<br>
;; global options: +cmd<br>
;; Got answer:<br>
;; ->>HEADER<<- opcode: QUERY, status: NXDOMAIN, id: 31007<br>
;; flags: qr rd ra; QUERY: 1, ANSWER: 0, AUTHORITY: 1, ADDITIONAL: 1<br>
<br>
;; OPT PSEUDOSECTION:<br>
; EDNS: version: 0, flags:; udp: 4096<br>
;; QUESTION SECTION:<br>
;52.52.88.106.			IN	A<br>
<br>
;; AUTHORITY SECTION:<br>
.			60	IN	SOA	a.root-servers.net. nstld.verisign-grs.com. 2017050100 1800 900 604800 86400<br>
<br>
;; Query time: 4 msec<br>
;; SERVER: 172.31.0.2#53(172.31.0.2)<br>
;; WHEN: Mon May 01 02:47:11 EDT 2017<br>
;; MSG SIZE  rcvd: 116<br>
</code>

Show the nscd service is running<br>

<code>
$ sudo yum install nscd<br>
...<br>
<br>
$ sudo systemctl start nscd<br>
$ systemctl status nscd<br>
nscd.service - Name Service Cache Daemon<br>
   Loaded: loaded (/usr/lib/systemd/system/nscd.service; disabled; vendor preset: disabled)<br>
   Active: active (running) since Mon 2017-05-01 02:49:21 EDT; 14s ago<br>
  Process: 9653 ExecStart=/usr/sbin/nscd $NSCD_OPTIONS (code=exited, status=0/SUCCESS)<br>
 Main PID: 9654 (nscd)<br>
   CGroup: /system.slice/nscd.service<br>
           9654 /usr/sbin/nscd<br>
...<br>
</code>

Show the ntpd service is running<br>

<code>
$ sudo yum install ntp<br>
...<br>
<br>
$ sudo systemctl start ntpd<br>
$ systemctl status ntpd<br>
ntpd.service - Network Time Service<br>
   Loaded: loaded (/usr/lib/systemd/system/ntpd.service; disabled; vendor preset: disabled)<br>
   Active: active (running) since Mon 2017-05-01 02:51:57 EDT; 49s ago<br>
  Process: 9735 ExecStart=/usr/sbin/ntpd -u ntp:ntp $OPTIONS (code=exited, status=0/SUCCESS)<br>
 Main PID: 9736 (ntpd)<br>
   CGroup: /system.slice/ntpd.service<br>
           9736 /usr/sbin/ntpd -u ntp:ntp -g<br>
...<br>
</code>

