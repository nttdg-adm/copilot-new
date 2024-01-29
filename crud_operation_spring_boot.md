---
title: "CRUD Operations in spring boot using GitHub Copilot"
description: "Simple code completion for CRUD Operation with GitHub Copilot"
category: general
platforms: [copilot, copilot-chat]
level: lv3
---

## Examples of CRUD Operations in spring boot using GitHub Copilot
[<img src="https://img.shields.io/badge/Lv3-Mature_Best_Practice-brightgreen">](https://github.com/orgs/AI-Native-Development/projects/1/)

### Description
CRUD refers to the four basic operations a software application should be able to perform 
 - Create
 - Read 
 - Update 
 - Delete.

 Users must be able to create data, have access to the data in the UI by reading the data, update or edit the data, and delete the data.

 Each letter in the CRUD acronym has a corresponding HTTP request method.

                |  CRUD OPERATION  |  HTTP REQUEST METHOD  |
                |      Create      |       POST            |
                |      Read        |       Get             |
                |      Update      |       PUT & Patch     |
                |      Delete      |       Delete          |

Github copilot can generate "Create" operation in a Spring Boot application using Github Copilot, a developer can start by providing a comment or a partial code snippet that describes the intention of creating an entity or performing a creation operation. 

Also, Github Copilot provides a suggestion when you given a right instruction.
Developer has given comments to "Create a new user in Spring Boot"

### For example

#### Input code

```java
@PostMapping("/users")
public ResponseEntity<User> createUser
(@RequestBody User user){
    //create a new user and print them
}
```

#### Result Suggested by Copilot
```java
               
                @PostMapping("/users")
                public ResponseEntity<User> createUser(@RequestBody User user) {
                     //create a new user and print them
                    User createdUser = userRepository.save(user);
                    return ResponseEntity.ok(createdUser);
                }
```
Developer can also ask Github Copilot for the remaining CRUD operation, Copilot will suggest the code with appropriate solution.

>## Excercise:-
1. Try out for the same Read Operation in this activity and Ask Copilot how to make it more reliable and efficient.
2. perform some Delete user or delete operation by using Copilot.
