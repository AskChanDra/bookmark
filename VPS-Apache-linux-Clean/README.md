#Clean Cpanel Server 

####Trying to clean my Bluehost VPS and Digitalocean server:


The simple command to cleanup yum caches:

```bash

yum clean all
```
EasyApache files can be removed with following command.

```bash

rm -rfv /home/cpeasyapache
```


You can empty all error_log files to 0 bytes usage with following command:


```bash

find /home/ -name error_log -type f -print -exec truncate --size 0 "{}" \;
```

#### References:

1. [How to Clear disk Space on Cpanel Server](https://srvfail.com/clear-disk-space-cpanel-server/)
2. [Clear disk space on CentOS 6 or CentOS 7](https://www.getpagespeed.com/server-setup/clear-disk-space-centos)