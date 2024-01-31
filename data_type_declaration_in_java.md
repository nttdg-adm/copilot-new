---
title: "Examples of various Data Types in java using GitHub Copilot"
description: "Simple code completion with GitHub Copilot"
category: general
platforms: [copilot, copilot-chat]
level: lv3
---

## Examples of various Data Types in java using GitHub Copilot
[<img src="https://img.shields.io/badge/Lv3-Mature_Best_Practice-brightgreen">](https://github.com/orgs/AI-Native-Development/projects/1/)

### Description
In java, Data types are divided into two groups:
- Primitive data types - includes byte, short, int, long, float, double, boolean and char
- Non-primitive data types - such as String, Arrays and Classes

A primitive data type specifies the size and type of variable values.
We can learn how to declare data types in java using GitHub Copilot. If we just write instruction as `Give examples of Data Types in java` as a comment, it will generate all data types and also add seperate comments above two groups as `//primitive data types` and  `//Non-Primitive Data Types` to recognize them.
As we said, primitive data type specifies the size. If we start comment above int data type declaration as `size of` it will give exact suggestion as  `//size of int = 4 bytes` and continues to give suggestion for size of each primitive data type.

#### Example
- **Exercise 1**
##### Input Code
```java
    public class DataTypeExample {

        public static void main(String[] args) {
           //Give examples of Data Types in java
        }
    }
```

##### Result Suggested by Copilot

```java
    public class DataTypeExample {
    public static void main(String[] args) {
       
        //Give examples of Data Types in java
        //Primitive Data Types
        int a = 10;

        float b = 10.5f;

        double c = 10.5;
        
        char d = 'A';
        
        boolean e = true;
        
        long f = 1000000000000000000L;
        
        short g = 12345;
        
        byte h = 123;
        //Non-Primitive Data Types
        //String
        String i = "Hello World";
        //Array
        int[] j = {1,2,3,4,5};
    }
    }
```

- **Exercise 2**
##### Input Code
```java
    public class DataTypeExample {

        public static void main(String[] args) {
        //Give examples of Data Types in java
        //size of int
        int a = 10;
        
        float b = 10.5f;
        
        double c = 10.5;
        
        char d = 'A';
        
        boolean e = true;
        
        long f = 1000000000000000000L;
        
        short g = 12345;
        
        byte h = 123;
        //Non-Primitive Data Types
        //String
        String i = "Hello World";
        //Array
        int[] j = {1,2,3,4,5};
        }
    }
```

##### Result Suggested by Copilot

```java
    public class DataTypeExample {
    public static void main(String[] args) {
       
    
        //Give examples of Data Types in java
        //Primitive Data Types
        //size of int = 4 bytes
        int a = 10;
        //size of float = 4 bytes
        float b = 10.5f;
        //size of double = 8 bytes
        double c = 10.5;
        //size of char = 2 bytes
        char d = 'A';
        //size of boolean = 1 byte
        boolean e = true;
        //size of long = 8 bytes
        long f = 1000000000000000000L;
        //size of short = 2 bytes
        short g = 12345;
        //size of byte = 1 byte
        byte h = 123;
        //Non-Primitive Data Types
        //String
        String i = "Hello World";
        //Array
        int[] j = {1,2,3,4,5};
    }
    }
```