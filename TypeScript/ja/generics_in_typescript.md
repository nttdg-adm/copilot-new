---
title: "GitHub Copilotを使用したTypeScriptのジェネリクス"
description: "GitHub Copilotを使用したTypeScriptのジェネリクス"
category: general
platforms: [copilot, copilot-chat]
level: lv3
---

## GitHub Copilotを使用したTypeScriptのジェネリクス
[<img src="https://img.shields.io/badge/Lv3-Mature_Best_Practice-brightgreen">](https://github.com/orgs/AI-Native-Development/projects/1/)

### 説明
プログラムを書く際に、再利用可能なコンポーネントを作成することは非常に重要な要素の一つです。これにより、プログラムは柔軟性を持ち、長期的にスケーラブルになります。
ジェネリクスは再利用可能なコンポーネントを作成するのに役立ちます。ジェネリクスは、コンポーネントを特定のデータ型に制限せず、任意のデータ型で動作させる方法を提供します。つまり、コンポーネントはさまざまなデータ型で呼び出すことができます。TypeScriptのジェネリクスは、ほぼC#のジェネリクスと同じです。
GitHub Copilotを使用すると、ジェネリクスの概念を理解するための説明と例を提供してくれます。コメントとして「TypeScriptのジェネリクスとは何ですか？」と書いてGitHub Copilotに尋ねると、説明と例を教えてくれます。
異なる名前で複数の型変数を指定することができます。TypeScriptでは、ジェネリクス内で複数の型変数を定義することができます。これにより、ジェネリックコンポーネントの異なる部分に異なるデータ型を指定することができます。GitHub Copilotは、ジェネリクス内で複数の型変数を定義する例を提案してくれます。

### 例

- **演習1**
##### 入力コード
```TypeScript
//TypeScript のジェネリックスとは何ですか?
```

##### 副操縦士によって提案された結果
```TypeScript
//TypeScript のジェネリックスとは何ですか?
// TypeScript のジェネリックスを使用すると、さまざまなデータ型を処理できる再利用可能なコンポーネントを作成できます。ジェネリックを使用すると、コンポーネントの使用時に指定されるデータ型のプレースホルダーを使用して、クラス、インターフェイス、および関数を定義できます。これにより、コードがより柔軟になり、タイプセーフになります。
// TypeScript でのジェネリックスの使用例を次に示します。
function identity<T>(arg: T): T {
    return arg;
}
let output = identity<string>("Hello, TypeScript!");
console.log(output); // Output: Hello, TypeScript!
let op = identity(100);
console.log(op); // Output: 100
```

- **演習2**
##### 入力コード
```TypeScript
//TypeScript のジェネリックにおける複数の型変数
```

##### 副操縦士によって提案された結果
```TypeScript
//TypeScript のジェネリックにおける複数の型変数
// TypeScript を使用すると、ジェネリックスで複数の型変数を定義できます。これを使用して、ジェネリック コンポーネントのさまざまな部分に異なるデータ型を指定できます。これにより、柔軟性が向上し、複数のデータ型を同時に処理する汎用コンポーネントを作成できるようになります。
// TypeScript のジェネリックスで複数の型変数を使用する例を次に示します。
function swap<T, U>(tuple: [T, U]): [U, T] {
    return [tuple[1], tuple[0]];
}
let swapped = swap<string, number>(["hello", 123]);
console.log(swapped); // Output: [123, "hello"]
let swapped1 = swap<number, string>([123, "world"]);
console.log(swapped1); // Output: ["world", 123]
```