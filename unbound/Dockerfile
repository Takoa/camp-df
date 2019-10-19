FROM alpine:3

RUN apk update \
    && apk add --no-cache unbound \
    && unbound-anchor -a "/etc/unbound/root.key" || : \
    && chown unbound:unbound /etc/unbound

EXPOSE 53/udp 53/tcp

ENTRYPOINT ["/usr/sbin/unbound", "-d", "-p"]
