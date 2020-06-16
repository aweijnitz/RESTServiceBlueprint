# REST Service Blueprint

Personal accelerator to speed up home project creation.

This is a generic webservice that is in intended as a blueprint to save time on those precious Saturday mornings and late evenings when dad gets some personal time to work on fun side projects.

Based on Spring Boot.

**NOTE!** To reduce the amount of configuration and adaptation that has to be done, it always builds an artifact named `target/application.jar`. This is not really best practice, but simplifies scripting. Just edit the pom.xml and get rid of the final build name to revert back to normal behavior.

## Use

    java -jar target/application.jar
    curl http://localhost:9090/message
    
## Build and Build and Run
    
    mvn clean package
    mvn clean package spring-boot:run

## Test

    mvn test
    
 