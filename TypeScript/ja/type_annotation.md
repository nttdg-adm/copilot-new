---
title: "GitHub Copilotを使用したTypeScriptでの関数"
description: "GitHub Copilotを使用したTypeScriptでの関数"
category: general
platforms: [copilot, copilot-chat]
level: lv3
---

## GitHub Copilotを使用したTypeScriptでの関数
[<img src="https://img.shields.io/badge/Lv3-Mature_Best_Practice-brightgreen">](https://github.com/orgs/AI-Native-Development/projects/1/)

### 説明
TypeScriptでは、変数、関数、オブジェクトなどの識別子の型を明示的に指定するために、型注釈を使用します。
型注釈は、識別子の後に`：型`の構文を使用し、型は任意の有効な型であることができます。
識別子に型が注釈されると、その型としてのみ使用することができます。識別子が異なる型として使用される場合、TypeScriptコンパイラはエラーを発行します。
GitHub Copilotは、TypeScriptでの型注釈の使用方法を知るためのお手伝いをしてくれます。
「TypeScriptでの型注釈の使用方法は？」とGitHub Copilotに尋ねると、使用例を示してくれます。

### 例

##### 入力コード
```TypeScript
//typeScript で型アノテーションを使用するにはどうすればよいですか?
```


##### 副操縦士によって提案された結果
```TypeScript
// typeScript で型アノテーションを使用するにはどうすればよいですか?
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