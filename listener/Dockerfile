FROM composer:2.5 as composer
WORKDIR /app
COPY composer.json composer.lock ./
RUN composer install --ignore-platform-req=ext-sockets

FROM php:8
WORKDIR /app
COPY --from=composer /app/vendor ./vendor
COPY listener.php .
CMD ["php", "listener.php"]
