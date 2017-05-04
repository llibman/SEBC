* Authenticate the llibman user (on a different host) and check the ticket

```
[ec2-user@ip-172-31-0-65 ~]$ kinit llibman
Password for llibman@CLOUDERA-LLIBMAN.COM: 
[ec2-user@ip-172-31-0-65 ~]$ klist -e
Ticket cache: KEYRING:persistent:1000:krb_ccache_NZAzZMR
Default principal: llibman@CLOUDERA-LLIBMAN.COM

Valid starting       Expires              Service principal
05/03/2017 21:57:09  05/04/2017 21:57:09  krbtgt/CLOUDERA-LLIBMAN.COM@CLOUDERA-LLIBMAN.COM
	Etype (skey, tkt): aes256-cts-hmac-sha1-96, aes256-cts-hmac-sha1-96 
```
