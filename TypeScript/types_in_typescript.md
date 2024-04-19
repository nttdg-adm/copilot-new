---
title: "Types in TypeScript using GitHub Copilot"
description: "Types in TypeScript using GitHub Copilot"
category: general
platforms: [copilot, copilot-chat]
level: lv3
---
 
## Spring Boot Actuator using GitHub Copilot
[<img src="https://img.shields.io/badge/Lv3-Mature_Best_Practice-brightgreen">](https://github.com/orgs/AI-Native-Development/projects/1/)
 
### Description
TypeScript supports some simple types (primitives), different types of User defined types. It provides data types for the JavaScript to transform it into a strongly typed programing language. JavaScript doesn't support data types. We can use the data types feature in JavaScript with the help of TypeScript. TypeScript plays an important role when the object-oriented programmer wants to use the type feature in any scripting language or object-oriented programming language.
The following are some of the built-in types in TypeScript: 
1. Number: Double precision 64-bit floating point values. It can be used to represent both, integers and fractions.
2. String: It represents a sequence of Unicode characters
3. Boolean: It represents logical values, true and false
4. Void: It is used on function return types to represent non-returning functions
5. Null: It represents an intentional absence of an object value.
6. Undefined: It denotes value given to all uninitialized variables.

There are many user defined data types in TypeScript such as Enumerations (enums), classes, interfaces, arrays, and tuple.

GitHub Copilot can be used to declare many types in typeScript.
GitHub Copilot chat gets open by clicking *Ctrl + I*. GitHub Copilot can give suggestions for it . If we ask GitHub Copilot as `//Give example of built in data types in TypeScript` , it will suggest us declaration of it and gives example of each

### Example
This example shows different types declaration in typeScript.

##### Input Code
```TypeScript
//Give example of built in data types in TypeScript
```


##### Result Suggested by Copilot
```TypeScript
/**
 * Examples of simple types in TypeScript
 */

// Number
let num: number = 10;
console.log(num);

// String
let str: string = "Hello";
console.log(str);

// Boolean
let bool: boolean = true;
console.log(bool);

// Void
/**
 * Prints "Hello" to the console.
 */
function hello(): void {
    console.log("Hello");
}
hello();

// Null
let n: null = null;
console.log(n);

/**
 * Examples of built-in data types in TypeScript
 */

// Boolean
let isDone: boolean = false;
console.log(isDone);

// Number
let decimal: number = 6;
console.log(decimal);

// String
let color: string = "blue";
console.log(color);

// Array
let list: number[] = [1, 2, 3];
console.log(list);

// Tuple
let x: [string, number];
x = ["hello", 10];
console.log(x);

// Enum
enum Color {Red, Green, Blue}
let c: Color = Color.Green;
console.log(c);

// Any
let notSure: any = 4;
console.log(notSure);

// Void
/**
 * Prints "This is my warning message" to the console.
 */
function warnUser(): void {
    console.log("This is my warning message");
}
warnUser();

// Null and Undefined
let u: undefined = undefined;
let n: null = null;
console.log(u);
console.log(n);

// Never
/**
 * Throws an error with the given message.
 * @param message - The error message.
 * @throws Error with the given message.
 */
function error(message: string): never {
    throw new Error(message);
}
error("This is an error message");

// Object
declare function create(o: object | null): void;
create({ prop: 0 });
create(null);

// Type assertions
let someValue: any = "this is a string";
let strLength: number = (someValue as string).length;
console.log(strLength);

// Union
let union: string | number;
union = "hello";
console.log(union);
union = 10;
console.log(union);
```