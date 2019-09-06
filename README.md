# Example Spring Eureka Client

This is a sample spring application that acts as a client for a eureka server running at `localhost:8761`.

It includes an auto-generated swagger OpenAPI documentation (at `/v2/api-docs`) and an info-url 
by spring-actuator (at `/actuator/info`) showing the git commit ID.

## Running

You can run the application locally with 
```
mvn spring-boot:run
``` 

or with docker using:

```
mvn clean package
docker build --build-arg JAR_FILE=target/*.jar -t myorg/myapp .
docker run -p 8081:8081 -t myorg/myapp
```