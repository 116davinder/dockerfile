FROM ruby:alpine

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

# Install Ruby Modules
ADD Gemfile* /app
RUN bundle install

# Adding Source Code to Container
ADD . .

# Exporting Environment Varaiables
ENV APPLICATION_ENVIRONMENT DEVELOPMENT

# Running Ruby Application
CMD ["rails", "server", "--binding", "0.0.0.0”]
