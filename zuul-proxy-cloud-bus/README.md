# Zuul proxy microservice
Examples of microservice instrastructures: Zuul proxy

## Blog post
For this example, a Zuul proxy used as edge service will be incorporated.
Explanation of the architecture and purpose of having a Zuul proxy:
http://www.josedab.com/2016/03/01/microservices-using-zuul-proxy-as-a-micro-proxy-and-api-gateway/

## Overview
Zuul service proxying GET and POST requests. 
On top of proxying requests, distributed messaging is incorporated to access multiple ends without having to locate each of the services (In this case service A and B)

## Deployment

Each maven subproject is a Spring Boot application. Running the example would be as easy as running the following:
`mvn spring-boot:run`
inside each of the suprojects.

The recommended way to deploy is:

- Deploy config-service
- Deploy service a
- Deploy service b
- Deploy Eureka service
- Deploy Zuul proxy service