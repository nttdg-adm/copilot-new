---
title: "Functional Programming in java using GitHub Copilot"
description: "Functional Programming in java with GitHub Copilot"
category: general
platforms: [copilot, copilot-chat]
level: lv3
---

## Functional Programming implementation in java using GitHub Copilot
[<img src="https://img.shields.io/badge/Lv3-Mature_Best_Practice-brightgreen">](https://github.com/orgs/AI-Native-Development/projects/1/)

### Description
Functional programming (FP) is a programming paradigm. It emphasizes the use of pure functions that don't have side effects and always return the same output for a given input. It treats computation as the evaluation of mathematical functions and avoids changing state and mutable table.
Basically, functional programming is a style of writing computer programs that treat computations as evaluating mathematical functions.
In mathematics, a function is an expression that relates an input set to an output set.
Importantly, the output of a function depends only on its input. More interestingly, we can compose two or more functions together to get a new function.
Please note that many features in functional programming haven’t always been part of Java, and it’s advisable to be on Java 8 or later to exercise functional programming effectively.

Using GitHub Copilot we can learn about functional programming in java.
We can explore various features of functional programming of GitHub Copilot such as Lambda expressions etc.
If we add comment as `write a function which prints even numbers in a list using lambda expression`, GitHub Copilot will give you perfect suggestion. So, you can check there is no change in output if we use lambda expression.

#### Example
- **Exercise 1**
##### Input Code
```java
import java.util.Arrays;
import java.util.List;
/**
 * Functional_Programming_in_Java
 */
public class Functional_Programming_in_Java {

    public static void main(String[] args) {
    //create list of integers
    List<Integer> list = Arrays.asList(1,2,3,4,5,6,7,8,9,10);
    //call the function to print even numbers using lambda expression
    printEven(list);
    //call the function to print even numbers without using lambda expression
    printEvenWithoutLambda(list);

        
    }
    // write a function which prints even numbers in a list using lambda expression
   
}
```

##### Result Suggested by Copilot
```java
import java.util.Arrays;
import java.util.List;
/**
 * Functional_Programming_in_Java
 */
public class Functional_Programming_in_Java {

    public static void main(String[] args) {
    //create list of integers
    List<Integer> list = Arrays.asList(1,2,3,4,5,6,7,8,9,10);
    //call the function to print even numbers using lambda expression
    printEven(list);
    //call the function to print even numbers without using lambda expression
    printEvenWithoutLambda(list);

        
    }
    // write a function which prints even numbers in a list using lambda expression
    public static void printEven(List<Integer> list){
        list.stream().filter(i -> i%2 == 0).forEach(System.out::println);
    }
    
    // Write a function which prints even numbers in a list with simple for loop
    public static void printEvenWithoutLambda(List<Integer> list){
        for (int i : list) {
            if(i%2 == 0){
                System.out.println(i);
            }
        }
    }
}
```

- **Exercise 2**
##### Input Code
```java
/**
 * FunctionExample
 */
public class FunctionExample {

    public static void main(String[] args) {
        // create a function that takes string and returns its length

    }
}
```

##### Result Suggested by Copilot
```java
/**
 * FunctionExample
 */
public class FunctionExample {

    public static void main(String[] args) {
        // create a function that takes string and returns its length
        Function<String, Integer> function = s -> s.length();
        // call the function
        System.out.println(function.apply("Hello World"));

    }
}
```