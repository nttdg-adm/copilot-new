---
title: "GitHub Copilotを使用したTypeScriptの型"
description: "GitHub Copilotを使用したTypeScriptの型"
category: general
platforms: [copilot, copilot-chat]
level: lv3
---

## GitHub Copilotを使用したTypeScriptの型
[<img src="https://img.shields.io/badge/Lv3-Mature_Best_Practice-brightgreen">](https://github.com/orgs/AI-Native-Development/projects/1/)

### 概要
TypeScriptはいくつかのシンプルな型（プリミティブ型）と、さまざまなユーザー定義型をサポートしています。これにより、JavaScriptを強く型付けされたプログラミング言語に変換することができます。JavaScriptはデータ型をサポートしていないため、TypeScriptのデータ型機能を使用することができます。TypeScriptは、オブジェクト指向プログラマーがスクリプト言語やオブジェクト指向プログラミング言語で型機能を使用したい場合に重要な役割を果たします。

以下は、TypeScriptで使用できるいくつかの組み込み型です：
1. Number: 64ビット倍精度浮動小数点値。整数と小数を両方表現するために使用できます。
2. String: Unicode文字のシーケンスを表します。
3. Boolean: 論理値trueとfalseを表します。
4. Void: 関数の戻り値の型として使用され、戻り値のない関数を表します。
5. Null: オブジェクトの値が意図的に存在しないことを表します。
6. Undefined: すべての初期化されていない変数に与えられる値を表します。

また、列挙型（enums）、クラス、インターフェース、配列、タプルなど、TypeScriptには多くのユーザー定義データ型があります。

GitHub Copilotを使用して、TypeScriptで多くの型を宣言することができます。GitHub Copilotチャットは、Ctrl + Iをクリックすることで開くことができます。GitHub Copilotは、`//TypeScript の組み込みデータ型の例を示します`という質問をすると、それに対する宣言と例を提案してくれます。

### 例

##### 入力コード
```TypeScript
//TypeScript の組み込みデータ型の例を示します
```


##### 副操縦士によって提案された結果
```TypeScript
//TypeScript の組み込みデータ型の例を示します
/**
 * TypeScript の単純な型の例
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
 * コンソールに「Hello」を出力します。
 */
function hello(): void {
    console.log("Hello");
}
hello();

// Null
let n: null = null;
console.log(n);

/**
 * TypeScript の組み込みデータ型の例
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
 * 「これは警告メッセージです」をコンソールに出力します。
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
 * 指定されたメッセージでエラーをスローします.
 * @param message - エラーメッセージ。
 * @throws 指定されたメッセージでエラーが発生しました。
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