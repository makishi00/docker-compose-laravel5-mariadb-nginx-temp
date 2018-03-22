#
# Dockerfile reference: https://docs.docker.com/engine/reference/builder/
#

FROM php:7-fpm-alpine

RUN set -xeuo pipefail \
 && apk add --no-cache icu-libs \
 && apk add --no-cache -t .icu-dev-deps icu-dev \
 && docker-php-ext-install opcache pdo_mysql intl \
 && apk del --no-cache --purge .icu-dev-deps
