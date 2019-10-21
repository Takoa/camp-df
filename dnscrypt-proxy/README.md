# dnscrypt-proxy
Containerized dnscrypt-proxy

## samples
### docker-compose
Edit *volumes* in docker-compose.yml to use your config (and other files), then

```shell
$ docker-compose up
```

It also requires *resolv.conf* is configured to use the loopback interface as
a nameserver.
```
#/etc/resolv.conf
nameserver 127.0.0.1
options edns0 single-request-reopen
```
