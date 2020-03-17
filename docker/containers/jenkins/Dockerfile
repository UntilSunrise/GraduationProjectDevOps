FROM jenkins/jenkins:lts

USER root
RUN apt-get update
RUN apt-get install ca-certificates apt-transport-https -y

## Install Composer.
COPY --from=composer:latest /usr/bin/composer /usr/local/bin/composer
ENV PATH=$PATH:/root/composer/vendor/bin COMPOSER_ALLOW_SUPERUSER=1
