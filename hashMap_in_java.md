---
title: "Different Collections in java using GitHub Copilot"
description: "Implementation of HashSet and TreeSet with GitHub Copilot"
category: general
platforms: [copilot, copilot-chat]
level: lv3
---

## Implementing HashMap collection in java using GitHub Copilot
[<img src="https://img.shields.io/badge/Lv3-Mature_Best_Practice-brightgreen">](https://github.com/orgs/AI-Native-Development/projects/1/)

### Description
In Java, HashMap is a part of Java’s collection since Java 1.2. This class is found in java.util package.
A HashMap is a data structure that stores key-value pairs. It is part of the java.util package and is commonly used to efficiently retrieve values based on their corresponding keys. The key feature of a HashMap is its ability to perform key-based lookups in constant time, which means the time it takes to retrieve a value is not dependent on the size of the HashMap. This makes it very efficient for large collections of data.
Java HashMap class implements the Map interface which allows us to store key and value pair, where keys should be unique. 

    Map
    ├── AbstractMap
            ├── HashMap
         
GitHub Copilot can help you to create HashMap object.
Also, GitHub Copilot can give you suggestions for implementation of methods of HashMap class.

#### Example
- **Exercise 1**
##### Input Code
```java
    public class HashMapExample {

        public static void main(String[] args) {
           // Create a HashMap object called capitalCities
        }
    }
```

##### Result Suggested by Copilot

```java
    import java.util.HashMap;
    public class HashMapExample {
    public static void main(String[] args) {
       // Create a HashMap object called capitalCities
        HashMap<String, String> capitalCities = new HashMap<String, String>();
        // Add
        // keys and values (Country, City)
        capitalCities.put("England", "London");
        capitalCities.put("Germany", "Berlin");
        capitalCities.put("Norway", "Oslo");
    }
    }
```
- **Exercise 2**
##### Input Code
```java
    public class HashMapExample {

        public static void main(String[] args) {
        // Create a HashMap object called capitalCities
        HashMap<String, String> capitalCities = new HashMap<String, String>();
        // Add
        // keys and values (Country, City)
        capitalCities.put("England", "London");
        capitalCities.put("Germany", "Berlin");
        capitalCities.put("Norway", "Oslo");

        // Access an item from the HashMap
        }
    }
```

##### Result Suggested by Copilot

```java
    import java.util.HashMap;
    public class HashMapExample {
    public static void main(String[] args) {
       // Create a HashMap object called capitalCities
        HashMap<String, String> capitalCities = new HashMap<String, String>();
        // Add
        // keys and values (Country, City)
        capitalCities.put("England", "London");
        capitalCities.put("Germany", "Berlin");
        capitalCities.put("Norway", "Oslo");
        
        // Access an item from the HashMap
        System.out.println(capitalCities.get("England"));

        // Remove an item from the HashMap
        capitalCities.remove("England");
    }
    }
```