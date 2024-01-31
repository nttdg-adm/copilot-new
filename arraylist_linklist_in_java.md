---
title: "ArrayList, LinkList in java using GitHub Copilot"
description: "ArrayList, LinkList with GitHub Copilot"
category: general
platforms: [copilot, copilot-chat]
level: lv3
---

## ArrayList, LinkList in java using GitHub Copilot
[<img src="https://img.shields.io/badge/Lv3-Mature_Best_Practice-brightgreen">](https://github.com/orgs/AI-Native-Development/projects/1/)

### Description
A Collection represents a single unit of objects, i.e., a group.
Java Collection framework provides many interfaces and classes.The `java.util` package contains all the classes and interfaces for the Collection framework.

    Iterable
        ├── Collection
                ├── List
                │   ├──  ArrayList
                │   ├──  LinkedList

In above hierarchy diagram, Iterable, Collection and List are interfaces and ArrayList and LinkedList are classes.
List interface is the child interface of Collection interface. It inhibits a list type data structure in which we can store the ordered collection of objects. It can have duplicate values.

List interface is implemented by the classes ArrayList, LinkedList.
The classes that implement the List interface are given below.
- ArrayList
    #### Description: 
    ArrayList is a Java class implemented using the List interface. ArrayList is like an array, but there is no size limit. There are many operations which can be performed on arrayList using methods. GitHub Copilot can be used for declaring arrayList as well as doing some operations on it. 
    There are many ways to travers through list. GitHub Copilot can give suggestions for it . If we write comment as  `//Travers through list using Iterator` , it will suggest us implementation of it and also after completion of implemetation , GitHub Copilot will give suggestion for comments which represents many ways of traversal through list along with it's implementation.

    #### Example
    - **Exercise 1**
        ##### Input Code
        ```java
        import java.util.*;

        public class ArrayListExample {
        public static void main(String[] args) {
        // Create arrayList example  and print it.
        }
        }
        ```
        
        ##### Result Suggested by Copilot

        ```java
        import java.util.*;

        public class ArrayListExample {
            public static void main(String[] args) {
            //  Create arrayList example  and print it.
            ArrayList<String> cars = new ArrayList<String>();
            cars.add("Volvo");
            cars.add("BMW");
            cars.add("Ford");
            cars.add("Mazda");
            System.out.println(cars);
            }
        }
        ```
    - **Exercise 2**
        ##### Input Code
        ```java
        import java.util.*;

        public class ArrayListExample {
        public static void main(String[] args) {
        // Create arrayList example and operations on arraylist to it and print it.
        ArrayList<String> cars = new ArrayList<String>();
        cars.add("Volvo");
        cars.add("BMW");
        cars.add("Ford");
        cars.add("Mazda");
        System.out.println(cars);
        // Travers through list using Iterator
        }
        }
        ```
        
        ##### Result Suggested by Copilot

        ```java
        import java.util.*;

        public class ArrayListExample {
            public static void main(String[] args) {
            //  Create arrayList example  and print it.
            ArrayList<String> cars = new ArrayList<String>();
            cars.add("Volvo");
            cars.add("BMW");
            cars.add("Ford");
            cars.add("Mazda");
            System.out.println(cars);
            // Travers through list using Iterator
            Iterator<String> it = cars.iterator();
            while(it.hasNext()){
                System.out.println(it.next());
            }
            // Travers through list using for loop
            for(int i=0;i<cars.size();i++){
                System.out.println(cars.get(i));
            }
            // Travers through list using for each loop
            for(String i:cars){
                System.out.println(i);
            }  
            // Travers through list using forEach() method
            cars.forEach((n) -> System.out.println(n));
            // Travers through list using forEachRemaining() method
            Iterator<String> it1 = cars.iterator();
            it1.forEachRemaining((n) -> System.out.println(n));
            // Travers through list using listIterator() method
            ListIterator<String> it2 = cars.listIterator();
            while(it2.hasNext()){
                System.out.println(it2.next());
            }
            }
        }
        ```
- LinkedList
    #### Description: 
    Java LinkedList class uses a doubly linked list to store the elements.
    The LinkedList class is almost identical to the ArrayList.
    For many cases, the ArrayList is more efficient as it is common to need access to random items in the list, but the LinkedList provides several methods to do certain operations more efficiently. Using GitHub Copilot , we can get methods which are not in arrayList. If we write comment `//Give examples of methods of linked list that are not in arraylist`, it will give suggestions of methods like `addFirst(), addLast(), removeFirst(), etc`.

    #### Example
    - **Exercise 1**
        ##### Input Code
        ```java
        import java.util.*;

        public class LinkedListExample {
        public static void main(String[] args) {
            // Create a LinkedList object called cars that will store strings 
            // (the names of car brands)
        }
        }
        ```
        
        ##### Result Suggested by Copilot

        ```java
        import java.util.*;

        public class LinkedListExample {
            public static void main(String[] args) {
                // Create a LinkedList object called cars that will store strings 
                // (the names of car brands)
                LinkedList<String> cars = new LinkedList<String>();
                // Add elements to the end of the list
                cars.add("Volvo");
                cars.add("BMW");
                cars.add("Ford");
                cars.add("Mazda");
                // Print out the list
                System.out.println(cars);
            }
        }
        ```
    - **Exercise 2**
        ##### Input Code
        ```java
        import java.util.*;

        public class LinkedListExample {
            public static void main(String[] args) {
                // Create a LinkedList object called cars that will store strings 
                // (the names of car brands)
                LinkedList<String> cars = new LinkedList<String>();
                // Add elements to the end of the list
                cars.add("Volvo");
                cars.add("BMW");
                cars.add("Ford");
                cars.add("Mazda");
                // Print out the list
                System.out.println(cars);
                
                // Give examples of methods of linked list that are not in arraylist
        }
        }
        ```
        
        ##### Result Suggested by Copilot

        ```java
        import java.util.*;

        public class LinkedListExample {
            public static void main(String[] args) {
                // Create a LinkedList object called cars that will store strings 
                // (the names of car brands)
                LinkedList<String> cars = new LinkedList<String>();
                // Add elements to the end of the list
                cars.add("Volvo");
                cars.add("BMW");
                cars.add("Ford");
                cars.add("Mazda");
                // Print out the list
                System.out.println(cars);

                // Give examples of methods of linked list that are not in arraylist
                // Add an element to the end of the list
                cars.addLast("Honda");
                // Print out the list
                System.out.println(cars);
                // Remove the last element
                cars.removeLast();
                // Print out the list
                System.out.println(cars);
            }
        }
        ```