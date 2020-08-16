#latest realease as 15/08/2020
FROM php:7.4-fpm-buster
RUN apt update
RUN apt upgrade -y
RUN apt install -y vim
RUN apt install -y apt-utils
RUN apt install -y iputils-ping
#mbstring dependency
RUN apt install -y libonig-dev
#xml dependency
RUN apt install -y libxml2-dev
#zip dependency
RUN apt install -y libzip-dev
#RUN apt install -y curl
#RUN apt install -y libcurl4
#RUN apt install -y libcurl4-openssl-dev
# RUN apt install -y postgresql-client
# RUN apt install -y mariadb-client 
# RUN apt install -y libsqlite3-dev
# RUN apt install -y libsqlite3-0

#composer install
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/bin/ --filename=composer

#php extensions
RUN docker-php-ext-install bcmath
RUN docker-php-ext-install ctype 
RUN docker-php-ext-install fileinfo
RUN docker-php-ext-install json
RUN docker-php-ext-install mbstring
#RUN docker-php-ext-install openssl
RUN docker-php-ext-install pdo
RUN docker-php-ext-install pdo_mysql
RUN docker-php-ext-install tokenizer
RUN docker-php-ext-install xml
RUN docker-php-ext-install zip

#laravel installer
RUN composer global require laravel/installer
#composer commands in PATH
RUN echo 'export PATH="$PATH:$HOME/.composer/vendor/bin"' >> ~/.bashrc


#nvm install
SHELL ["/bin/bash", "--login", "-c"]
RUN curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.0/install.sh | bash
RUN source /root/.bashrc 
#node lts as 15/08/2020
RUN nvm install 12.18.3
RUN nvm use 12.18.3
