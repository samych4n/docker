FROM php:7.3-fpm-buster
RUN apt update
RUN apt upgrade -y
RUN apt install -y vim
RUN apt install -y apt-utils
RUN apt install -y curl
RUN apt install -y libcurl4
RUN apt install -y libcurl4-openssl-dev
RUN apt install -y postgresql-client
RUN apt install -y mariadb-client 
RUN apt install -y libsqlite3-dev
RUN apt install -y libsqlite3-0
RUN apt install -y libxml2-dev

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/bin/ --filename=composer

RUN docker-php-ext-install pdo pdo_mysql
RUN docker-php-ext-install mysqli
RUN docker-php-ext-install pdo_mysql 
RUN docker-php-ext-install pdo_sqlite
RUN docker-php-ext-install sockets
RUN docker-php-ext-install json
RUN docker-php-ext-install curl
RUN docker-php-ext-install xml


#COPY ./php.ini /usr/local/etc/php/php.ini