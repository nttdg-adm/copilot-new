---
title: "Classes in TypeScript using GitHub Copilot"
description: "Classes in TypeScript using GitHub Copilot"
category: general
platforms: [copilot, copilot-chat]
level: lv3
---
 
## Classes in TypeScript using GitHub Copilot
[<img src="https://img.shields.io/badge/Lv3-Mature_Best_Practice-brightgreen">](https://github.com/orgs/AI-Native-Development/projects/1/)
 
### Description
TypeScript is object oriented JavaScript. TypeScript supports object-oriented programming features like classes, interfaces, etc. A class is a blueprint for creating objects. A class encapsulates data for the object.
JavaScript does not have a concept of class like other programming languages such as Java and C#. JavaScript ES5 or earlier didn’t support classes.But Typescript gives built in support for this concept called class. Typescript gets this feature from ES6.
We can create class using GitHub Copilot. It will save our time and gives accurate result as per your provided information.
If we add comment with instruction as `//Create a class inTypeScript`, Github copilot gives example of classes in typeScript by creating any random class. If we specify field name , class name then it will suggest the result as per your instructions.

### Example

- **Exercise 1**
##### Input Code
```TypeScript
//Create a class inTypeScript
```

##### Result Suggested by Copilot
```TypeScript
// Create a class in TypeScript
class Person {
    name: string;
    age: number;

    constructor(name: string, age: number) {
        this.name = name;
        this.age = age;
    }

    displayInfo() {
        console.log(`Name: ${this.name}, Age: ${this.age}`);
    }
}
```

- **Exercise 2**
##### Input Code
```TypeScript
//Create a class named Car having fields brand, model and price
```


##### Result Suggested by Copilot
```TypeScript
//Create a class named Car having fields brand, model and price
class Car {
    brand: string;
    model: string;
    price: number;

    constructor(brand: string, model: string, price: number) {
        this.brand = brand;
        this.model = model;
        this.price = price;
    }

    displayInfo() {
        console.log(`Brand: ${this.brand}, Model: ${this.model}, Price: ${this.price}`);
    }
}
```