* Upgraded CM to version 5.11.0 (latest available), and re-ran the upgrade wizard to upgrade the agent version in all hosts

* Report the latest available version of the API

```
$ curl -u llibman http://54.206.92.109:7180/api/version
Enter host password for user 'llibman':
v16
```

* Report the CM version

```
$ curl -u llibman http://54.206.92.109:7180/api/v6/cm/version
Enter host password for user 'llibman':
{
  "version" : "5.11.0",
  "buildUser" : "jenkins",
  "buildTimestamp" : "20170412-1255",
  "gitHash" : "70cb1442626406432a6e7af5bdf206a384ca3f98",
  "snapshot" : false
}
```

* List all CM users

```
$ curl -u llibman http://54.206.92.109:7180/api/v16/users
Enter host password for user 'llibman':
{
  "items" : [ {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ]
  }, {
    "name" : "llibman",
    "roles" : [ "ROLE_ADMIN" ]
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ]
  } ]
}
```

* Report the database server in use by CM

```
$ curl -u llibman http://54.206.92.109:7180/api/v16/cm/scmDbInfo
Enter host password for user 'llibman':
{
  "scmDbType" : "MYSQL",
  "embeddedDbUsed" : false
}
```
