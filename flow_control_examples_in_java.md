---
title: "Examples of flow control in java using GitHub Copilot"
description: "Learn syntax of flow controls from Examples of flow control in java using GitHub Copilot"
category: general
platforms: [copilot, copilot-chat]
level: lv3
---
## Flow Control Examples in java using GitHub Copilot
[<img src="https://img.shields.io/badge/Lv3-Mature_Best_Practice-brightgreen">](https://github.com/orgs/AI-Native-Development/projects/1/)

### Description
There are different kinds of flow control statements in java. if-else , for loop , while loop are some of them. If you are new to Java and it's syntax , Github copilot can give you some idea about syntax. You don't need to google it ,copy it from anywhere. You can learn syntax and various things using Github copilot.
If we don't have idea about syntax of if-else statement in java, you can ask GitHub Copilot to give example of if-else statement.For e.g. if you write comment in java file as `//Give me example of if-else syntax` it will automatically generate syntax. 
Also, if you want to use string variables in if-else statement, give instruction to use varibles in if-else statement. It will give appropriate result.

#### Example
- **Exercise 1**
    ##### Input Code
    ```java
    public class FlowControlExample {

        public static void main(String[] args) {
           //please give me if else statement example here
        }
    }
    ```

    ##### Result Suggested by Copilot

    ```java
    public class FlowControlExample {

        public static void main(String[] args) {
           //please give me if else statement example here
           if (true) {
               System.out.println("This is true");
           } else {
               System.out.println("This is false");
           }
        }

    }
    ```
- **Exercise 2**
    ##### Input Code
    ```java
    public class FlowControlExample {

    public static void main(String[] args) {
        //Example 1
       //please give me if else statement example here
       if (true) {
           System.out.println("This is true");
       } else {
           System.out.println("This is false");
       }

       //Example 2
       //please give me if else statement example using following data
        int a = 10;
        int b = 20;
    }
    ```
    
    ##### Result Suggested by Copilot
    
    ```java
    public static void main(String[] args) {
        //Example 1
       //please give me if else statement example here
       if (true) {
           System.out.println("This is true");
       } else {
           System.out.println("This is false");
       }

       //Example 2
       //please give me if else statement example using following data
        int a = 10;
        int b = 20;
        if (a > b) {
            System.out.println("a is greater than b");
        } else {
            System.out.println("b is greater than a");
        }
    }
    ```
- **Exercise 3**
    ##### Input Code
    ```java
    public class FlowControlExample {

        public static void main(String[] args) {
           //Give examples of Control Flow Statements in java
        }
    }
    ```

    ##### Result Suggested by Copilot

    ```java
    public class FlowControlExample {

        public static void main(String[] args) {
        //Give examples of Control Flow Statements in java
        //If-Else
        int a = 10;
        int b = 20;
        if(a > b){
            System.out.println("a is greater than b");
        }else{ 
            System.out.println("b is greater than a");
        }
        //Switch
        int c = 10;
        switch(c){
            case 10:
                System.out.println("Hello World");
                break;
            default:
                System.out.println("Hello World");
        }
        //For
        for(int d = 0; d < 10; d++){
            System.out.println("Hello World");
        }
        //While
        int i = 0;
        while(i < 10){
            System.out.println("Hello World");
            i++;
        }
        //Do-While
        int j = 0;
        do{
            System.out.println("Hello World");
            j++;
        }while(j < 10);
        //Break
        for(int k = 0; k < 10; k++){
            if(k == 5){
                break;
            }
            System.out.println("Hello World");
        }
        //Continue
        for(int l = 0; l < 10; l++){
            if(l == 5){
                continue;
            }
            System.out.println("Hello World");
        }
        }

    }
    ```