---
title: "Generics in TypeScript using GitHub Copilot"
description: "Generics in TypeScript using GitHub Copilot"
category: general
platforms: [copilot, copilot-chat]
level: lv3
---
 
## Generics in TypeScript using GitHub Copilot
[<img src="https://img.shields.io/badge/Lv3-Mature_Best_Practice-brightgreen">](https://github.com/orgs/AI-Native-Development/projects/1/)
 
### Description
One of most important aspects is to build reusable components when we write programs.This ensures that the program is flexible as well as scalable in the long-term.
Generics helps to create reusable components. Generics provide a way to make components work with any data type and not restrict to one data type. So, components can be called or used with a variety of data types. Generics in TypeScript is almost similar to C# generics.
Using GitHub Copilot, we can learn Generics concept with example. When we ask GitHub Copilot by writing comment as `What is Generics in TypeScript?`, it will give you description as well as example to understand the concept.
We can specify multiple type variables with different names.TypeScript allows you to define multiple type variables in generics, which can be used to specify different data types for different parts of the generic component.GitHub Copilot can suggest the example where we can define multiple type variables in generics.

### Example

- **Exercise 1**
##### Input Code
```TypeScript
//What is Generics in TypeScript?
```

##### Result Suggested by Copilot
```TypeScript
//What is Generics in TypeScript?
// Generics in TypeScript allow you to create reusable components that can work with a variety of data types. Generics
// enable you to define classes, interfaces, and functions with placeholders for data types that are specified when the
// component is used. This makes your code more flexible and type-safe.
// Here's an example of using generics in TypeScript:
function identity<T>(arg: T): T {
    return arg;
}
let output = identity<string>("Hello, TypeScript!");
console.log(output); // Output: Hello, TypeScript!
let op = identity(100);
console.log(op); // Output: 100
```

- **Exercise 2**
##### Input Code
```TypeScript
//Multiple Type Variables in Generics in TypeScript
```

##### Result Suggested by Copilot
```TypeScript
//Multiple Type Variables in Generics in TypeScript
// TypeScript allows you to define multiple type variables in generics, which can be used to specify different data types
// for different parts of the generic component. This provides more flexibility and allows you to create generic components
// that work with multiple data types simultaneously.
// Here's an example of using multiple type variables in generics in TypeScript:
function swap<T, U>(tuple: [T, U]): [U, T] {
    return [tuple[1], tuple[0]];
}
let swapped = swap<string, number>(["hello", 123]);
console.log(swapped); // Output: [123, "hello"]
let swapped1 = swap<number, string>([123, "world"]);
console.log(swapped1); // Output: ["world", 123]
```