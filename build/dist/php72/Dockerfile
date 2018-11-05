FROM webjump/development-php:7.2-fpm
MAINTAINER Marcio Maciel <marcio@webjump.com.br>

ARG GID=1000
ARG UID=1000

RUN groupmod -g $GID app && \
    usermod -g $GID -u $UID app
