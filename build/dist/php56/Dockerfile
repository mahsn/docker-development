FROM marciowebjump/development-php:5.6-fpm
MAINTAINER Jeroen Boersma <jeroen@srcode.nl>

# Install AMPQ and RabbitMQ Libs
RUN apt-get update \
    && apt-get install -y \
        librabbitmq-dev \
        libssh-dev \
    && docker-php-ext-install \
        bcmath \
        sockets \
    && pecl install amqp \
    && docker-php-ext-enable amqp


# Installing NodeJS from external resource
RUN curl -sL https://deb.nodesource.com/setup_8.x | bash - && \
    apt-get install -y nodejs

#Installing Grunt
RUN npm install -g grunt-cli

ARG GID=1000
ARG UID=1000

RUN groupmod -g $GID app && \
    usermod -g $GID -u $UID app

