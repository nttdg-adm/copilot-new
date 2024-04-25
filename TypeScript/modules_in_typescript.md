---
title: "Modules in TypeScript using GitHub Copilot"
description: "Functions in TypeScript using GitHub Copilot"
category: general
platforms: [copilot, copilot-chat]
level: lv3
---
 
## Modules in TypeScript using GitHub Copilot
[<img src="https://img.shields.io/badge/Lv3-Mature_Best_Practice-brightgreen">](https://github.com/orgs/AI-Native-Development/projects/1/)
 
### Description
When ES6 introduced the concept of the module, JavaScript started supporting the module concepts as a part of the JavaScript library. When TypeScript comes into the picture it also shares the module with JavaScript. The TypeScript module allows it to contain both the declaration and its code. The module executes in local environments, not in the global scope. That means when we define the functions, variables, classes, interfaces, etc., in the module, it cannot be visible outside the module until you cannot export the module using the export statement. If you want to access the variables, and functions in the module, you must import the module into your file by using the import statement.
GitHub Copilot can guide you to create module in typescript. Even it will not create file but it can suggest you where you can create file and the file content. There are different ways to import module. As you click `tab`, GitHub Copilot can suggest you all the ways to implement import module, also it will explain the way. The examples might give you an error because of the same function name, or the file you're importing isn't currently there but GitHub Copilot suggests where to write the code so you have to create those files and then add content to them.

### Example

##### Input Code
```TypeScript
// How to create module in typescript?
```

##### Result Suggested by Copilot
```TypeScript
// How to create module in typescript?
// A module in TypeScript is a way to organize and encapsulate code into reusable units. Modules allow you to
// group related code together and provide a way to import and export functionality between different parts of
// your application. Modules help in organizing and managing the codebase, making it easier to maintain and
// scale the application.
// In TypeScript, you can create a module by using the export keyword to export classes, functions, variables,
// and other entities from a file, and the import keyword to import these entities into another file. You can
// also use the export default keyword to export a single entity as the default export of a module.
// Here's an example of creating a module in TypeScript:
// File: math.ts
export function add(x: number, y: number): number {
    return x + y;
}
export function subtract(x: number, y: number): number {
    return x - y;
}
// File: app.ts
import { add, subtract } from "./math";
console.log(add(5, 3)); // Output: 8
console.log(subtract(5, 3)); // Output: 2
// In this example, we have created a module named math.ts that exports two functions, add and subtract. We then import
// these functions into another file named app.ts and use them to perform addition and subtraction operations.
// TypeScript also supports the export default syntax, which allows you to export a single entity as the default export
// of a module. Here's an example of using export default in TypeScript:
// File: math.ts
function multiply(x: number, y: number): number {
    return x * y;
}
export default multiply;
// File: app.ts
import multiply from "./math";
console.log(multiply(5, 3)); // Output: 15
// In this example, we have created a module named math.ts that exports a single function multiply as the default export.
// We then import this function into another file named app.ts using the import ... from syntax and use it to perform
// multiplication operation.
// TypeScript also supports the export * syntax, which allows you to export all entities from a module. Here's an example
// of using export * in TypeScript:
// File: math.ts
export function add(x: number, y: number): number {
    return x + y;
}
export function subtract(x: number, y: number): number {
    return x - y;
}
// File: app.ts
import * as math from "./math";
console.log(math.add(5, 3)); // Output: 8
console.log(math.subtract(5, 3)); // Output: 2
// In this example, we have created a module named math.ts that exports two functions, add and subtract. We then import
// all entities from this module into another file named app.ts using the import * as syntax and use them to perform
// addition and subtraction operations.
```