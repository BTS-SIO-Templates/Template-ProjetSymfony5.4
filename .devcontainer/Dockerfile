# Utilise l'image officielle PHP 7.4 comme base
FROM mcr.microsoft.com/devcontainers/php:0-7.4



# 1. Dépendances système
RUN apt-get update \
    && apt-get install -y gnupg2 wget build-essential libzip-dev libpng-dev libonig-dev libxml2-dev libicu-dev libpq-dev libsqlite3-dev default-mysql-client libmysqlclient-dev

# 2. Extension PHP pdo_mysql
RUN docker-php-ext-install pdo_mysql

# 3. Symfony CLI
RUN wget https://repo.symfony.com/symfony-cli-stable.deb \
    && apt install -y ./symfony-cli-stable.deb \
    && rm symfony-cli-stable.deb

# 4. Composer
RUN wget https://getcomposer.org/installer -O composer-setup.php \
    && php composer-setup.php --install-dir=/usr/local/bin --filename=composer \
    && rm composer-setup.php

# Copie le reste de la configuration (optionnel)
# USER vscode
