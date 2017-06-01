FROM node:latest

# Name of maintiner
MAINTINER DAVINDER PAL "dpsangwal@gmail.com"

# Creating Application folder in container
RUN mkdir -p /app

# Setting Home Directory for Application
WORKDIR /app

# Copying Package.json
ADD package.json /app

# Installing Node Modules
RUN npm install

# Exporting Ports for Application
EXPOSE 8080 8081

# Creating Volume for Persistent Data
VOLUME ["/app-data"]

# Adding Source Code to Container
ADD . .

# Exporting Environment Varaiables
ENV APPLICATION_ENVIRONMENT DEVELOPMENT

# Running Application
CMD ["npm", "start"]
