---
title: "CRUD Operations in spring boot using GitHub Copilot"
description: "CRUD Operation with GitHub Copilot"
category: general
platforms: [copilot, copilot-chat]
level: lv3
---

## Examples of CRUD Operations in spring boot using GitHub Copilot
[<img src="https://img.shields.io/badge/Lv3-Mature_Best_Practice-brightgreen">](https://github.com/orgs/AI-Native-Development/projects/1/)

### Description


# CRUD Operations in Spring Boot

In this guide, we will explore how to perform CRUD (Create, Read, Update, Delete) operations in a Spring Boot application.

## Create Operation

To create a new entity in Spring Boot, you can use the `POST` HTTP method. 

Here's an example of creating a new user:

@PostMapping("/users")
    public ResponseEntity<User> createUser(@RequestBody User user) {
    // Logic to create a new user
    // ...
    return ResponseEntity.ok(user);
}
