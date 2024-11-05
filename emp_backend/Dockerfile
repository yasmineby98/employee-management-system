#Use the official OpenJDK 17 runtime as the base image
FROM openjdk:17-jdk-slim

#Set the working directory inside the container
WORKDIR /app

#Copy the Maven build file to cache dependencies
COPY pom.xml /app/

#Copy the application source code
COPY src /app/src

#Build the application using Maven

#Copy the generated JAR file into the container
COPY target/emp_backend-0.0.1-SNAPSHOT.jar emp_backend.jar

#Expose the application port
EXPOSE 8080

#Run the application
ENTRYPOINT ["java", "-jar", "/app/emp_backend.jar"]