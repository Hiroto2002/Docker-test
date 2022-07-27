# fpm :サーバー機能を持たせる
FROM php:8.1-fpm-alpine

#LaravelはphpのパッケージマネージャーであるComposerでインストールできる
#DockerコンテナでLaravelを動かすにはComposer
# のインストールが毎回必要になってくるためここに書いてしまう
# install composer
RUN curl -sS https://getcomposer.org/installer | php
RUN mv composer.phar /usr/local/bin/composer

#Laravelを動かすためにPHP以外の拡張モジュールを入れる
#install packages
RUN apk update
RUN apk add git

#install php extensions
RUN docker-php-ext-install pdo pdo_mysql
