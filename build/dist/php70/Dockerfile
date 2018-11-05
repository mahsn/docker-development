FROM marciowebjump/development-php:7.0-fpm
MAINTAINER Marcio Maciel <marcio@webjump.com.br>

ARG GID=1000
ARG UID=1000

RUN groupmod -g $GID app && \
    usermod -g $GID -u $UID app
