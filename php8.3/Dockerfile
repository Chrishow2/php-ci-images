FROM php:8.3-cli

RUN apt-get update && apt-get install -y \
    libzip-dev \
    libpng-dev \
    libonig-dev \
    libsqlite3-dev \
    libicu-dev \
    zip \
    unzip \
    curl \
    git \
    && rm -rf /var/lib/apt/lists/*

RUN docker-php-ext-install \
    pdo \
    pdo_sqlite \
    mbstring \
    intl \
    gd \
    zip \
    bcmath \
    pcntl \
    opcache

COPY php.ini /usr/local/etc/php/conf.d/custom.ini

COPY --from=composer:2.9.5 /usr/bin/composer /usr/bin/composer

WORKDIR /var/www/html

CMD ["php", "artisan", "test"]
