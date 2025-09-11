
# Utilise l'image officielle PHP 7.4 CLI comme base
FROM php:7.4-cli



# 1. Dépendances système (essentielles uniquement)
RUN apt-get update \
    && apt-get install -y gnupg2 wget git unzip libzip-dev libpng-dev libonig-dev libxml2-dev libicu-dev libpq-dev libsqlite3-dev libmysqlclient-dev

# 2. Extensions PHP nécessaires
RUN docker-php-ext-install pdo pdo_mysql intl zip

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
