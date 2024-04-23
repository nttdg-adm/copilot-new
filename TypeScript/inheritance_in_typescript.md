---
title: "Inheritance in TypeScript using GitHub Copilot"
description: "Inheritance in TypeScript using GitHub Copilot"
category: general
platforms: [copilot, copilot-chat]
level: lv3
---
 
## Inheritance in TypeScript using GitHub Copilot
[<img src="https://img.shields.io/badge/Lv3-Mature_Best_Practice-brightgreen">](https://github.com/orgs/AI-Native-Development/projects/1/)
 
### Description
Inheritance in TypeScript is when a class can reuse the properties and methods of another class. There are 2 types of classes when we implement Inheritance. First is Child class. Child class is the class which inherits properties and methods. Second is Parent class. Parent class is whose properties and methods are inherited.
JavaScript uses prototypal inheritance, not classical inheritance like Java or C#. ES6 introduces the class syntax that is simply the syntactic sugar of the prototypal inheritance. TypeScript supports inheritance like ES6.
To inherit a class, you use the extends keyword. Using GitHub Copilot, we can learn Inheritance concept with example. When we ask GitHub Copilot by writing comment as `What is Inheritance in TypeScript?`, it will give you description as well as example to understand the concept.
### Example
This example shows different types declaration in typeScript.

##### Input Code
```TypeScript
//What is Inheritance in TypeScript?
```

##### Result Suggested by Copilot
```TypeScript
// What is Inheritance in TypeScript?
// Inheritance is a feature of object-oriented programming languages that allows you to create a new class (derived class) that inherits the properties and methods of an existing class (base class). The derived class can also have its own properties and methods in addition to the inherited ones.
// TypeScript supports inheritance through the use of the extends keyword. When a class extends another class, it inherits all the properties and methods of the base class. The derived class can then override or extend the inherited properties and methods, as well as define its own properties and methods.
// Here's an example of inheritance in TypeScript:
class Animal {
    name: string;

    constructor(name: string) {
        this.name = name;
    }

    makeSound() {
        console.log("Animal makes a sound");
    }
}
class Dog extends Animal {
    breed: string;

    constructor(name: string, breed: string) {
        super(name);
        this.breed = breed;
    }

    makeSound() {
        console.log("Dog barks");
    }

    fetch() {
        console.log("Dog fetches the ball");
    }
}
const barks = new Dog("Buddy", "Labrador");
barks.makeSound(); // Output: Dog barks
barks.fetch(); // Output: Dog fetches the ball
console.log(barks.name); // Output: Buddy
console.log(barks.breed); // Output: Labrador
```