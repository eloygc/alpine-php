FROM alpine:3.7

LABEL maintainer="Eloy Gómez <sr.eloy@gmail.com>"

RUN apk add -U \
    tini \
    php7 \
    php7-apcu \
    php7-bcmath \
    php7-common \
    php7-ctype \
    php7-curl \
    php7-exif \
    php7-fpm \
    php7-iconv \
    php7-intl \
    php7-json \
    php7-fileinfo \
    php7-mbstring \
    php7-mcrypt \
    php7-mysqlnd \
    php7-opcache \
    php7-openssl \
    php7-pcntl \
    php7-pdo_mysql \
    php7-pdo \
    php7-phar \
    php7-posix \
    php7-redis \
    php7-session \
    php7-simplexml \
    php7-tokenizer \
    php7-xml \
    php7-xmlwriter \
    php7-xsl \
    php7-zip \
    php7-zlib \
    && rm -rf /var/cache/apk/*

ADD config /

ENTRYPOINT ["/sbin/tini", "--"]

CMD ["/usr/sbin/php-fpm7", "-R", "--nodaemonize"]

EXPOSE 9000

WORKDIR /app