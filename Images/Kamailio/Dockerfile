FROM alpine:latest

RUN apk --no-cache upgrade \
    && apk --no-cache add gawk ca-certificates gdb strace mariadb-client postgresql-client musl-dbg \
    && apk --no-cache --allow-untrusted --repository http://local-repo search search -qe 'kamailio*' | \
          xargs apk --no-cache --allow-untrusted --repository http://local-repo add \
    && mkdir /var/lib/coredump \
    && echo "kernel.core_pattern=/var/lib/coredump/kamailio-core.%e.%p.%h.%t" > /etc/sysctl.d/00-core.conf && rm -fr /var/cache/apk/*

ENTRYPOINT ["kamailio", "-DD", "-E"]

