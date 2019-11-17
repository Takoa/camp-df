FROM alpine:3

ADD https://github.com/just-containers/s6-overlay/releases/download/v1.22.1.0/s6-overlay-amd64.tar.gz /tmp/
COPY services.d /etc/services.d

RUN apk update \
    && apk add --no-cache dnscrypt-proxy dnscrypt-proxy-openrc unbound \
    && unbound-anchor -a "/etc/unbound/root.key" || : \
    && chown unbound:unbound /etc/unbound \
    && tar -xf /tmp/s6-overlay-amd64.tar.gz -C / \
    && rm -rf /tmp/*

EXPOSE 53/udp 53/tcp

ENTRYPOINT ["/init"]
