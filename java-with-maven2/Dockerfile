FROM maven2

# Name of maintiner
MAINTINER DAVINDER PAL "dpsangwal@gmail.com"

# Creating Application folder in container
RUN mkdir -p /app

# Setting Home Directory for Application
WORKDIR /app

# Exporting Ports for Application
EXPOSE 8080 8081

# Creating Volume for Persistent Data
VOLUME ["/app-data"]

# Adding Source Code to Container
ADD . .

# Buiding code with maven3 builder
RUN mvn clean package

# Exporting Environment Varaiables
ENV APPLICATION_ENVIRONMENT DEVELOPMENT

# Running Application
CMD ["java", "-jar", "target/<name of your jar>.jar"]
