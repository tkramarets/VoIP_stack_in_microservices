FROM alpine:latest
MAINTAINER Taras Kramarets <tkramarets@gmail.com>

RUN apk add --no-cache \
        asterisk \
        asterisk-fax \
        asterisk-chan_sip \
        asterisk-odbc \
        asterisk-chan-dongle \
        asterisk-curl \
        asterisk-cdr-mysql \
        asterisk-sample-config \
        asterisk-sounds-en \
        asterisk-sounds-moh

CMD ["/usr/sbin/asterisk", "-c", "-ddd", "-f", "-vvv"]
