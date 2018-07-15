### How to set up master-slave DNS cluster
If you are looking for the options to avoid any DNS-related downtime or the way to manage dns across all server you have, you might consider to set up dns cluster.

1. Create user dns-cluster on a server which will be used as dns slave
2. Run following command on a master:

``` bash
v-add-remote-dns-host slave.yourhost.com 8083 admin p4sw0rd
```
