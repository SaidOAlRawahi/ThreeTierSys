# Use a Java runtime as the base image
FROM openjdk:17-jdk-alpine

WORKDIR /app
COPY . /app
RUN apk add --no-cache maven
RUN mvn clean install -DskipTests
EXPOSE 8080

# Command to run the Spring Boot application
CMD ["java", "-jar", "./target/ThreeTierTestBE-0.0.1.jar"]