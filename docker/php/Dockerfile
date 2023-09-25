FROM php:8.2-fpm

# Install PHP extensions
RUN apt update \
    && apt install -y libpq-dev \
    && docker-php-ext-install pdo pdo_pgsql

# Install Composer 
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
COPY . /var/www/html
# composer install
RUN composer install