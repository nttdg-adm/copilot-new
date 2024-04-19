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
Functions are the fundamental building block of any applications in JavaScript. It helps to make code readable, maintainable, and reusable. In TypeScript, however, we have the concept of classes, namespaces, and modules, but functions still are an integral part in describing how to do things. TypeScript also allows adding new capabilities to the standard JavaScript functions to make the code easier to work.
GitHub Copilot can create function for us. If we just write instruction as `Create a function to create Fibonacci Series in typescript` as a comment, it will generate function as `generateFibonacciSeries` which creates FibonacciSeries.

We can create a function in two ways. These are:
1. Named function
2. Anonymous function

If we ask GitHub Copilot chat as `Give example of Ananymous and named function in typescript` by clicking `ctrl + I`, it will give perfect examples to you.

### Example

- **Exercise 1**
##### Input Code
```TypeScript
//Create a function to create Fibonacci Series in typescript
```


##### Result Suggested by Copilot
```TypeScript
function generateFibonacciSeries(n: number): number[] {
    const series: number[] = [];

    if (n >= 1) {
        series.push(0);
    }
    if (n >= 2) {
        series.push(1);
    }

    for (let i = 2; i < n; i++) {
        const nextNumber = series[i - 1] + series[i - 2];
        series.push(nextNumber);
    }

    return series;
}
```

- **Exercise 2**
##### Input Code
```TypeScript
//Give example of Ananymous and named function in typescript
```


##### Result Suggested by Copilot
```TypeScript
// Anonymous function
const anonymousFunc = function() {
    console.log("This is an anonymous function.");
};

// Named function
function namedFunc() {
    console.log("This is a named function.");
}

// Call the functions
anonymousFunc();
namedFunc();
```