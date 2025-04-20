FROM php:8.2-apache

# Install MySQL extension
RUN docker-php-ext-install mysqli && docker-php-ext-enable mysqli

# Copy PHP file
COPY index.php /var/www/html/

# Set permissions
RUN chown -R www-data:www-data /var/www/html
