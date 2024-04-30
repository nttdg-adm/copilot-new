---
title: "TypeScriptを使用したクラス"
description: "TypeScriptを使用したクラス"
category: general
platforms: [copilot, copilot-chat]
level: lv3
---

## TypeScriptを使用したクラス
[<img src="https://img.shields.io/badge/Lv3-Mature_Best_Practice-brightgreen">](https://github.com/orgs/AI-Native-Development/projects/1/)

### 説明
TypeScriptはオブジェクト指向のJavaScriptです。TypeScriptはクラス、インターフェースなどのオブジェクト指向プログラミングの機能をサポートしています。クラスはオブジェクトを作成するための設計図です。クラスはオブジェクトのデータをカプセル化します。
JavaScriptにはJavaやC#などの他のプログラミング言語にあるクラスの概念はありません。JavaScriptのES5以前はクラスをサポートしていませんでした。しかし、TypeScriptはES6からこの機能を組み込んでいます。
GitHub Copilotを使用してクラスを作成することができます。これにより、時間を節約し、提供された情報に基づいて正確な結果が得られます。
`//TypeScriptでクラスを作成する`という指示コメントを追加すると、GitHub Copilotはランダムなクラスを作成してTypeScriptのクラスの例を提供します。フィールド名やクラス名を指定すると、指示に従った結果が提案されます。

### 例

- **演習1**
##### 入力コード
```TypeScript
//TypeScriptでクラスを作成する
```

##### 副操縦士によって提案された結果
```TypeScript
// TypeScriptでクラスを作成する
class Person {
    name: string;
    age: number;

    constructor(name: string, age: number) {
        this.name = name;
        this.age = age;
    }

    displayInfo() {
        console.log(`Name: ${this.name}, Age: ${this.age}`);
    }
}
```

- **演習2**
##### 入力コード
```TypeScript
//ブランド、モデル、価格のフィールドを持つ Car という名前のクラスを作成します。
```


##### 副操縦士によって提案された結果
```TypeScript
//ブランド、モデル、価格のフィールドを持つ Car という名前のクラスを作成します。
class Car {
    brand: string;
    model: string;
    price: number;

    constructor(brand: string, model: string, price: number) {
        this.brand = brand;
        this.model = model;
        this.price = price;
    }

    displayInfo() {
        console.log(`Brand: ${this.brand}, Model: ${this.model}, Price: ${this.price}`);
    }
}
```