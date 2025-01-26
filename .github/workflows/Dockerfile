# Use an official OpenJDK runtime as a parent image
FROM openjdk:17-jdk-slim

# Set the working directory inside the container
WORKDIR /app

# Copy the Maven POM file and the source code into the container
COPY pom.xml .
COPY src ./src

# Install Maven inside the container
RUN apt-get update && apt-get install -y maven

# Build the application
RUN mvn clean package

# Copy the built JAR file to the container
COPY target/d13revision-0.0.1-SNAPSHOT.jar app.jar

# Expose the port your Spring Boot app runs on
EXPOSE 8086

# Run the Spring Boot application
ENTRYPOINT ["java", "-jar", "app.jar"]
