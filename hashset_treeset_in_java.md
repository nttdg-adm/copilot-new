---
title: "Different Collections in java using GitHub Copilot"
description: "Implementation of HashSet and TreeSet with GitHub Copilot"
category: general
platforms: [copilot, copilot-chat]
level: lv3
---

## Implementing HashSet, TreeSet collections in java using GitHub Copilot
[<img src="https://img.shields.io/badge/Lv3-Mature_Best_Practice-brightgreen">](https://github.com/orgs/AI-Native-Development/projects/1/)

### Description
A Collection represents a single unit of objects, i.e., a group.
Java Collection framework provides many interfaces and classes.The `java.util` package contains all the classes and interfaces for the Collection framework.

    Iterable
        ├── Collection
                ├── Set
                │   ├── AbstrachSet
                │   │   ├── HashSet
                │   ├── SortedSet
                    │   ├── TreeSet

In above hierarchy diagram, Iterable, Collection ,Set and SortedSet are interfaces and AbstrachSet,HashSet and TreeSet are classes.
There is difference between List and Set. A list can contain duplicate elements whereas Set contains unique elements only.
The classes that implement the Set interface are given below.
- HashSet
    #### Description:
    Java HashSet class is used to create a collection that uses a hash table for storage. It inherits the AbstractSet class and implements Set interface. 
    Using GitHub Copilot , you can create HashSet object.HashSet contains unique elements only.
    If we give instruction as `//Create a HashSet object that stores Integer objects` , it will give correct suggestion. Also, GitHub copilot will give you suggestion about what operations can be done using methods on HashSet.
    Even if you try to add dublicate object , it will not change the HashSet.This can be shown using GitHub Copilot.

    #### Example
    - **Exercise 1**
        ##### Input Code
        ```java
        import java.util.HashSet;

        public class HashSetExample {
            public static void main(String[] args) {
                // Create a HashSet object that stores Integer objects
            }
        }
        ```
        
        ##### Result Suggested by Copilot

        ```java
        import java.util.HashSet;

        public class HashSetExample {
            public static void main(String[] args) {
                // Create a HashSet object that stores Integer objects
                HashSet<Integer> numbers = new HashSet<Integer>();
                // Add elements to the set
                numbers.add(4);
                numbers.add(7);
                numbers.add(8);
                // Print out the set
                System.out.println(numbers);
                
            }
        }
        ```

    - **Exercise 2**
        ##### Input Code
        ```java
        import java.util.HashSet;

        public class HashSetExample {
            public static void main(String[] args) {
                // Create a HashSet object that stores Integer objects
                HashSet<Integer> numbers = new HashSet<Integer>();
                // Add elements to the set
                numbers.add(4);
                numbers.add(7);
                numbers.add(8);
                // Print out the set
                System.out.println(numbers);
                // Add an element that is already in the set
            }
        }
        ```
        
        ##### Result Suggested by Copilot

        ```java
        import java.util.HashSet;

        public class HashSetExample {
            public static void main(String[] args) {
                // Create a HashSet object that stores Integer objects
                HashSet<Integer> numbers = new HashSet<Integer>();
                // Add elements to the set
                numbers.add(4);
                numbers.add(7);
                numbers.add(8);
                // Print out the set
                System.out.println(numbers);
                // Add an element that is already in the set
                numbers.add(4);
                // Print out the set
                System.out.println(numbers);
                // Remove an element from the set
                numbers.remove(7);
                // Print out the set
                System.out.println(numbers);
                // Print out the size of the set
                System.out.println(numbers.size());
            }
        }
        ```

- TreeSet
    #### Description: 
    Java TreeSet class implements the Set interface that uses a tree for storage. It inherits AbstractSet class and implements the NavigableSet interface. The objects of the TreeSet class are stored in ascending order. 
    Using GitHub Copilot , you can create TreeSet object.TreeSet contains unique elements only.
    If we give instruction as `//Create a TreeSet object that stores Double objects` , it will give correct suggestion. Also, GitHub copilot will give you suggestion about what operations can be done using methods on HashSet.

    #### Example
    - **Exercise 1**
        ##### Input Code
        ```java
        import java.util.TreeSet;

        public class TreeSetExample {
            public static void main(String[] args) {
                // Create a TreeSet object that stores Double objects
            }
        }
        ```
        
        ##### Result Suggested by Copilot

        ```java
        import java.util.TreeSet;

        public class TreeSetExample {
            public static void main(String[] args) {
                // Create a TreeSet object that stores Double objects
            TreeSet<Double> decimals = new TreeSet<Double>();
            // Add elements to the set
            decimals.add(4.0);
            decimals.add(7.0);
            decimals.add(8.0);
            // Print out the set
            System.out.println(decimals);
            }
        }
        ```

    - **Exercise 1**
        ##### Input Code
        ```java
        import java.util.TreeSet;

        public class TreeSetExample {
            public static void main(String[] args) {
                // Create a TreeSet object that stores Double objects
                TreeSet<Double> decimals = new TreeSet<Double>();
                // Add elements to the set
                decimals.add(4.0);
                decimals.add(7.0);
                decimals.add(8.0);
                // Print out the set
                System.out.println(decimals);
                // Add an element that is already in the set
            }
        }
        ```
        
        ##### Result Suggested by Copilot

        ```java
        import java.util.TreeSet;

        public class TreeSetExample {
            public static void main(String[] args) {
            // Create a TreeSet object that stores Double objects
            TreeSet<Double> decimals = new TreeSet<Double>();
            // Add elements to the set
            decimals.add(4.0);
            decimals.add(7.0);
            decimals.add(8.0);
            // Print out the set
            System.out.println(decimals);
            // Add an element that is already in the set
            decimals.add(4.0);
            // Print out the set
            System.out.println(decimals);
            // Remove an element from the set
            decimals.remove(7.0);
            // Print out the set
            System.out.println(decimals);
            // Print out the size of the set
            System.out.println(decimals.size());
            }
        }
        ```

