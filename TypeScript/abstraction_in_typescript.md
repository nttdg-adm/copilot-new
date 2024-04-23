---
title: "Abstraction in TypeScript using GitHub Copilot"
description: "Abstraction in TypeScript using GitHub Copilot"
category: general
platforms: [copilot, copilot-chat]
level: lv3
---
 
## Abstraction in TypeScript using GitHub Copilot
[<img src="https://img.shields.io/badge/Lv3-Mature_Best_Practice-brightgreen">](https://github.com/orgs/AI-Native-Development/projects/1/)
 
### Description
Abstraction is an important concept in Object Oriented Programming (OOP) as it allows us to hide away implementation details and expose only what is necessary to the user.Define an abstract class in Typescript using the abstract keyword. Abstract classes are mainly for inheritance where other classes may derive from them. We cannot create an instance of an abstract class.

An abstract class typically includes one or more abstract methods or property declarations. The class which extends the abstract class must define all the abstract methods.
Using GitHub Copilot, we can learn Abstraction concept with example. When we ask GitHub Copilot by writing comment as `What is Abstraction in TypeScript?`, it will give you description as well as example to understand the concept.
### Example

##### Input Code
```TypeScript
//What is abstraction in TypeScript?
```

##### Result Suggested by Copilot
```TypeScript
//What is abstraction in TypeScript?
// Abstraction is a concept in object-oriented programming that allows you to hide the implementation details of a class and only expose the necessary information to the outside world. This helps in reducing complexity and making the code more maintainable and reusable.
// TypeScript supports abstraction through the use of abstract classes and methods. An abstract class is a class that cannot
// be instantiated directly and can only be used as a base class for other classes. Abstract methods are methods that are
// declared in an abstract class but do not have an implementation. The derived classes must provide an implementation for
// these abstract methods.
// Here's an example of abstraction in TypeScript:
abstract class Shape {
    abstract calculateArea(): number;
}
class Circle extends Shape {
    radius: number;

    constructor(radius: number) {
        super();
        this.radius = radius;
    }

    calculateArea(): number {
        return Math.PI * this.radius * this.radius;
    }
}
```
