# dnscrypt-proxy
Containerized dnscrypt-proxy

## samples
### docker-compose
Edit *volumes* in docker-compose.yml to use your config (and other files), then

```shell
$ docker-compose up
```

Note that the sample config listens 127.0.0.2:53. If you haven't set up
the loopback, here's an example on Alpine Linux:

```
#/etc/network/interfaces
auto lo:1
iface lo:1 inet static
    address 127.0.0.2
    netmask 255.0.0.0
```

```
#/etc/resolv.conf
nameserver 127.0.0.2
options edns0 single-request-reopen
```
