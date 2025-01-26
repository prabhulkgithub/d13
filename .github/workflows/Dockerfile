FROM openjdk:23-jdk-oracle as builder

WORKDIR /app

COPY mvnw
COPY mvn. cmd .
COPY scr src
COPY pom.xml
RUN ./mvn

