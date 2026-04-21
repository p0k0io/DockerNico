FROM php:8.2-apache

RUN docker-php-ext-install mysqli

# Activar mod_rewrite
RUN a2enmod rewrite

# Copiar app
COPY src/ /var/www/html/

# Permisos
RUN chown -R www-data:www-data /var/www/html
RUN chmod -R 755 /var/www/html

# Permitir acceso al directorio (CLAVE)
RUN echo '<Directory /var/www/html>\n\
    Options Indexes FollowSymLinks\n\
    AllowOverride All\n\
    Require all granted\n\
</Directory>' > /etc/apache2/conf-available/custom.conf \
    && a2enconf custom
