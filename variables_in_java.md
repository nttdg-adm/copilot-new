---
title: "Examples of various types of Variables in java using GitHub Copilot"
description: "Simple code completion with GitHub Copilot"
category: general
platforms: [copilot, copilot-chat]
level: lv3
---

## Examples of various types of Variables in java using GitHub Copilot
[<img src="https://img.shields.io/badge/Lv3-Mature_Best_Practice-brightgreen">](https://github.com/orgs/AI-Native-Development/projects/1/)

### Description
There are mainly 3 types of Variables in Java.
- Local Variables
- Static Variables
- Instance Variables

Github copilot can generate the comment on the basis of Class name. If you create class for showing various types of Variables in java and named it as `VariableExample`, then github copilot will suggest comment which says ` //this class is used to demonstrate the use of variables`.

Also, GitHub Copilot provides accurate suggestions when you write comments with clear instructions.
We can give instruction for creating examples of Local Variables, Static Variables in comments, it will create all examples we needed.


#### Example

##### Input Code
```java
public class VariableExample { 
    //create static variable and local variable and print them
}
```

##### Result Suggested by Copilot

```java
// this class is used to demonstrate the use of variables
public class VariableExample {
//create static variable and local variable and print them
    static int staticVariable = 10;
    int localVariable = 20;
    public static void main(String[] args) {
        System.out.println("Static variable: " + staticVariable);
        VariableExample obj = new VariableExample();
        System.out.println("Local variable: " + obj.localVariable);
    }
    
}
```