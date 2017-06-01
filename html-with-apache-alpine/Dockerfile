FROM httpd:alpine

# Name of maintiner
MAINTINER DAVINDER PAL "dpsangwal@gmail.com"

# Creating Application folder in container
RUN mkdir -p /var/www/html

# Setting Home Directory for Application
WORKDIR /var/www/html

# Exporting Ports for Application
EXPOSE 80

# Creating Volume for Persistent Data
VOLUME ["/var/www/html/data"]

# Adding Source Code to Container
ADD . .

# Changing Permissions
RUN chmod -R 755 /var/www/html \
    && chown -R www-data:www-data /var/www/html

# Exporting Environment Varaiables
ENV APPLICATION_ENVIRONMENT DEVELOPMENT
