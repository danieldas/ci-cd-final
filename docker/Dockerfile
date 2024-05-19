# Utiliza la imagen oficial de PHP con Apache
FROM php:7.4-apache

# Copia el archivo de configuración de Apache para habilitar la reescritura de URLs
COPY 000-default.conf /etc/apache2/sites-available/000-default.conf

# Habilita el módulo de reescritura de Apache
RUN a2enmod rewrite

# Copia el archivo index.php al directorio raíz del servidor web
COPY index.php /var/www/html/

# Exponer el puerto 80
EXPOSE 80

# Comando para ejecutar Apache en primer plano
CMD ["apache2-foreground"]