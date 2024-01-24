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
