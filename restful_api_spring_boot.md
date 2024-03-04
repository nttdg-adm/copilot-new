---
title: "RESTful API in Spring Boot using GitHub Copilot"
description: "RESTful API with GitHub Copilot"
category: general
platforms: [copilot, copilot-chat]
level: lv3
---
 
## RESTful API in Spring Boot using GitHub Copilot
[<img src="https://img.shields.io/badge/Lv3-Mature_Best_Practice-brightgreen">](https://github.com/orgs/AI-Native-Development/projects/1/)
 
### Description
Representational state transfer (REST) is a software architectural style that defines a set of constraints to be used for creating Web services. Web services that conform to the REST architectural style, called RESTful Web services, provide interoperability between computer systems on the Internet.

The best way to learn Spring Boot is to develop the REST APIs.
Furthermore, they are used in the microservices or consumed by other applications. The REST API teaches you the following things:

- HTTP Methods: POST, GET, PUT, DELETE, OPTIONS and TRACE
- HTTP Status Codes: 1.X.X, 2.X.X, 3.X.X, 4.X.X and 5.X.X. 

### Example
This example creates a simple RESTful API that exposes a single endpoint at /api/hello.

When a client sends a GET request to this endpoint, the API returns the string "Hello, World!".

## Input Code
```java
@SpringBootApplication
public class DemoApplication {

    public static void main(String[] args) {
        SpringApplication.run(DemoApplication.class, args);
    }
}

@RestController
@RestMapping("/api")
    public class DemoController {
            // perform basic authentication..
}
```

## Result Suggested by Copilot
```java
@SpringBootApplication
public class DemoApplication {

    public static void main(String[] args) {
        SpringApplication.run(DemoApplication.class, args);
    }

}

@RestController
@RestMapping("/api")
public class DemoController {
   // perform basic authentication

    @GetMapping("/hello")
    public String hello(){
        return "Hello World";
    }
}
```



