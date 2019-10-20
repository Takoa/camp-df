FROM alpine:3

RUN apk update \
    && apk add --no-cache dnscrypt-proxy dnscrypt-proxy-openrc

EXPOSE 53/udp 53/tcp

ENTRYPOINT ["/usr/bin/dnscrypt-proxy", "-config", "/etc/dnscrypt-proxy/dnscrypt-proxy.toml"]
