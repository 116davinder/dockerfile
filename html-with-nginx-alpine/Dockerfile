FROM nginx:alpine

# Name of maintiner
MAINTINER DAVINDER PAL "dpsangwal@gmail.com"

# Creating Application folder in container
RUN mkdir -p /usr/share/nginx

# Setting Home Directory for Application
WORKDIR /usr/share/nginx

# Exporting Ports for Application
EXPOSE 80

# Creating Volume for Persistent Data
VOLUME ["/usr/share/nginx/data"]

# Adding Source Code to Container
ADD . .

# Changing Permissions
RUN chmod -R 755 /var/www/html \
    && chown -R nginx:nginx /var/www/html

# Exporting Environment Varaiables
ENV APPLICATION_ENVIRONMENT DEVELOPMENT
