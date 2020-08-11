FROM alpine:latest

RUN apk update \
    && apk add --no-cache iperf

EXPOSE 5001/tcp 5001/udp

CMD [ "/bin/sh" ]
