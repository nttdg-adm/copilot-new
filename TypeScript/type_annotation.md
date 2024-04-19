---
title: "Functions in TypeScript using GitHub Copilot"
description: "Functions in TypeScript using GitHub Copilot"
category: general
platforms: [copilot, copilot-chat]
level: lv3
---
 
## Functions in TypeScript using GitHub Copilot
[<img src="https://img.shields.io/badge/Lv3-Mature_Best_Practice-brightgreen">](https://github.com/orgs/AI-Native-Development/projects/1/)
 
### Description
TypeScript uses type annotations to explicitly specify types for identifiers such as variables, functions, objects, etc.
TypeScript uses the syntax `: type` after an identifier as the type annotation, which type can be any valid type.
Once an identifier is annotated with a type, it can be used as that type only. If the identifier is used as a different type, the TypeScript compiler will issue an error.
GitHub Copilot can help us to get to know type annotation usage in typeScript.
If we ask GitHub Copilot as `How to use type annotation in typeScript?`, it will give example of usage of it.
### Example
This example shows different types declaration in typeScript.

##### Input Code
```TypeScript
//How to use type annotation in typeScript?
```


##### Result Suggested by Copilot
```TypeScript
// Type annotations usage
let num: number = 10;
let str: string = "Hello, TypeScript!";
let bool: boolean = true;
let arr: number[] = [1, 2, 3];
let obj: { name: string, age: number } = { name: "John", age: 30 };
let func: (x: number, y: number) => number = (x, y) => x + y;

console.log(num);
console.log(str);
console.log(bool);
console.log(arr);
console.log(obj);
console.log(func(5, 3));
```