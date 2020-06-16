# REST Service Blueprint

Personal accelerator to speed up home project creation.

This is a generic webservice that is in intended as a blueprint to save time on those precious Saturday mornings and late evenings when dad gets some personal time to work on fun side projects.

Based on Spring Boot.

**NOTE!** To reduce the amount of configuration and adaptation that has to be done, it always builds an artifact named `target/application.jar`. This is not really best practice, but simplifies scripting. Just edit the pom.xml and get rid of `<finalName>application</finalName>` to revert back to normal behavior.

## Use

    java -jar target/application.jar
    curl http://localhost:9090/message
    
## Build and Build and Run
    
    mvn clean package
    mvn clean package spring-boot:run
    
## Build Docker Image

This project makes use of the new built-in docker buildpack in Spring Boot.
See https://spring.io/blog/2020/01/27/creating-docker-images-with-spring-boot-2-3-0-m1

    mvn spring-boot:build-image
    
    # same
    
    # Try
    docker images
    REPOSITORY     TAG           IMAGE ID
    ...
    echoservice    1.0-SNAPSHOT  231e3123
    ...
    docker run -it -p8080:9090 echoservice:1.0-SNAPSHOT

## Test

    mvn test
    
 