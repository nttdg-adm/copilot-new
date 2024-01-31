---
title: "Classes in java using GitHub Copilot"
description: "Class creation with GitHub Copilot"
category: general
platforms: [copilot, copilot-chat]
level: lv3
---

## Class creation in java using GitHub Copilot
[<img src="https://img.shields.io/badge/Lv3-Mature_Best_Practice-brightgreen">](https://github.com/orgs/AI-Native-Development/projects/1/)

### Description
Java is an object-oriented programming language. 
In Java, classes and objects are used to represent real-world concepts and entities. A class is a group of objects which have common properties.
A class in Java can contain:
- Fields
- Methods
- Constructors
- Blocks
- Nested class and interface

Using GitHub Copilot, we can create class having some fields, methods.
If we add comment with instruction as `//Create a class named "Main" and create field "x" and "y".And also create constructor and method to print value of x and y`, Github copilot gives exact output as we start typing `public class`. 

#### Example
##### Input Code
```java
//Create a class named "Main" and create field "x" and "y".And also create constructor and method to print value of x and y
public class
```
##### Result Suggested by Copilot

```java
//Create a class named "Main" and create field "x" and "y".And also create constructor and method to print value of x and y
public class Main {
    int x;
    int y;
    public Main(int x, int y){
        this.x = x;
        this.y = y;
    }
    public void print(){
        System.out.println("x = " + x + " y = " + y);
    }
}
```