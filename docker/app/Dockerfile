FROM ubuntu:20.04

# ubuntu packages
RUN apt update \
    && apt install -y software-properties-common \
    && add-apt-repository ppa:ondrej/php \
    && apt install -y git wget curl

# php install
RUN apt install -y php7.4 php7.4-zip php7.4-gd php7.4-pgsql php7.4-xsl php7.4-curl php7.4-mbstring php7.4-intl php7.4-fpm

# postgres install
RUN apt-get update \
    && DEBIAN_FRONTEND=noninteractive apt-get -y upgrade \
    && apt-get install -y postgresql-12

# Symfony cli
#RUN wget https://github.com/symfony/cli/releases/download/v4.25.2/symfony_linux_amd64 \
#    && chmod +x symfony_linux_amd64 \
#    && sudo mv symfony_linux_amd64 /usr/local/bin/symfony
#
## Composer
#RUN wget https://getcomposer.org/download/2.0.13/composer.phar \
#    && mv composer.phar /usr/bin/composer \
#    && chmod +x /usr/bin/composer
#
## Node.js
#RUN curl -sL https://deb.nodesource.com/setup_14.x | bash - \
#    && apt install nodejs
#
## npm
#RUN npm install -g npm@7.15.0
#
## user
#ARG user=shop
#ARG uid=1000
#ARG pass=shop
#
#RUN useradd -rm -d /var/www -s /bin/bash -g root -G sudo -u $uid $user -p "$(openssl passwd -1 $pass)"
#USER $user
#WORKDIR /var/www/shop-symfony/
#
#EXPOSE 8000