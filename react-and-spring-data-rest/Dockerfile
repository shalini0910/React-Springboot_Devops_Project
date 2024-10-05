# Use the official Maven image as the base image
FROM maven:3.9.0-amazoncorretto-8 AS build

# Set the working directory new
WORKDIR /app

#Version6
# Copy the pom.xml and any other necessary files to the container
COPY . ./src

WORKDIR /app/src

# Build the project
RUN mvn clean verify

# Command to run the application
CMD ["java", "-jar", "target/react-and-spring-data-rest-0.0.1-SNAPSHOT.jar"] 
