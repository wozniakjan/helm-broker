FROM alpine:3.13.5

RUN apk add --no-cache ca-certificates curl git mercurial
RUN apk add --no-cache --update openssh=8.6_p1-r0 --repository=http://dl-cdn.alpinelinux.org/alpine/edge/main

COPY ./start.sh /root/start.sh
COPY ./controller /root/controller

LABEL source=git@github.com:kyma-project/helm-broker.git

CMD ["/root/start.sh"]
