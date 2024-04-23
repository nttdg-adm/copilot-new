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
Typescript allows us to use access modifiers at the class level like other programming languages.We can get access to the class member due to access modifiers.The access modifier increases the security of the class members and prevents them from invalid use. Data Hiding or Encapsulation is the capability of a class which can control the visibility of its data members to members of other classes.We can use access modifiers to implement the concept of Encapsulation
The access modifiers define the visibility of a class’s data members outside its defining class.

The access modifiers supported by TypeScript are −
1.	public: A public data member has universal accessibility. Data members in a class are public by default.
2.	private: Private data members are accessible only within the class that defines these members. If an external class member tries to access a private member, the compiler throws an error.
3.	protected: A protected data member is accessible by the members within the same class as that of the former and also by the members of the child classes.

Using GitHub Copilot, we can learn about Access modifiers and it's usage.
If we ask GitHub Copilot as `What is Access modifiers in Typescript`by clicking `ctrl + I`, it will explain with example.
### Example

##### Input Code
```TypeScript
//What is Access modifiers in Typescript
```

##### Result Suggested by Copilot
```TypeScript
// What is Access modifiers in Typescript
class MyClass {
    public publicProperty: string;
    private privateProperty: number;
    protected protectedProperty: boolean;

    constructor() {
        this.publicProperty = "Public Property";
        this.privateProperty = 123;
        this.protectedProperty = true;
    }

    public publicMethod() {
        console.log("This is a public method.");
    }

    private privateMethod() {
        console.log("This is a private method.");
    }

    protected protectedMethod() {
        console.log("This is a protected method.");
    }
}

const myObject = new MyClass();
console.log(myObject.publicProperty); // Accessible
// console.log(myObject.privateProperty); // Not accessible
// console.log(myObject.protectedProperty); // Not accessible
myObject.publicMethod(); // Accessible
// myObject.privateMethod(); // Not accessible
// myObject.protectedMethod(); // Not accessible
```