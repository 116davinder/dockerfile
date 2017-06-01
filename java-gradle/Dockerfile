FROM gradle:latest

# Name of maintiner
MAINTINER DAVINDER PAL "dpsangwal@gmail.com"

# Creating Application folder in container
RUN mkdir -p /app

# Setting Home Directory for Application
WORKDIR /app

# Exporting Ports for Application
EXPOSE 8080 8082

# Creating Volume for Persistent Data
VOLUME ["/app-data"]

# Adding Source Code to Container
ADD . .

# Buiding code with maven3 builder
RUN gradle build jar

# Exporting Environment Varaiables
ENV APPLICATION_ENVIRONMENT DEVELOPMENT

# Running Application
CMD ["java", "-jar", "<name of your jar>.jar"]
