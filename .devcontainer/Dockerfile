# Utilise l'image officielle PHP 7.4 comme base
FROM mcr.microsoft.com/devcontainers/php:0-7.4


# Installe les dépendances système nécessaires, pdo_mysql, Symfony CLI et Composer
RUN apt-get update \
    && apt-get install -y gnupg2 wget build-essential libzip-dev libpng-dev libonig-dev libxml2-dev libicu-dev libpq-dev libsqlite3-dev libmysqlclient-dev \
    && docker-php-ext-install pdo_mysql \
    && wget https://repo.symfony.com/symfony-cli-stable.deb \
    && apt install -y ./symfony-cli-stable.deb \
    && rm symfony-cli-stable.deb \
    # Installation de Composer
    && wget https://getcomposer.org/installer -O composer-setup.php \
    && php composer-setup.php --install-dir=/usr/local/bin --filename=composer \
    && rm composer-setup.php

# Copie le reste de la configuration (optionnel)
# USER vscode
