---
title: "GitHub Copilotを使用したTypeScriptにおける継承"
description: "GitHub Copilotを使用したTypeScriptにおける継承"
category: general
platforms: [copilot, copilot-chat]
level: lv3
---

## GitHub Copilotを使用したTypeScriptにおける継承
[<img src="https://img.shields.io/badge/Lv3-Mature_Best_Practice-brightgreen">](https://github.com/orgs/AI-Native-Development/projects/1/)

### 説明
TypeScriptにおける継承とは、クラスが他のクラスのプロパティやメソッドを再利用することです。継承を実装する際には、2つのタイプのクラスがあります。まず、子クラスです。子クラスはプロパティやメソッドを継承するクラスです。次に、親クラスです。親クラスはプロパティやメソッドが継承されるクラスです。
JavaScriptは、JavaやC#のようなクラシカルな継承ではなく、プロトタイプベースの継承を使用しています。ES6では、クラス構文が導入され、それは単純にプロトタイプベースの継承のシンタックスシュガーです。TypeScriptはES6のような継承をサポートしています。
クラスを継承するには、extendsキーワードを使用します。GitHub Copilotを使用すると、継承の概念を理解するための説明と例が得られます。コメントとして「TypeScriptにおける継承とは何ですか？」と書いてGitHub Copilotに尋ねると、概要と例が表示されます。

### 例

##### 入力コード
```TypeScript
//TypeScript の継承とは何ですか?
```

##### 副操縦士によって提案された結果
```TypeScript
// TypeScript の継承とは何ですか?
// 継承は、既存のクラス (基本クラス) のプロパティとメソッドを継承する新しいクラス (派生クラス) を作成できるようにするオブジェクト指向プログラミング言語の機能です。派生クラスは、継承されたものに加えて、独自のプロパティとメソッドを持つこともできます。
// TypeScript は、extends キーワードの使用による継承をサポートします。クラスが別のクラスを拡張すると、そのクラスは基本クラスのすべてのプロパティとメソッドを継承します。派生クラスは、継承されたプロパティとメソッドをオーバーライドまたは拡張したり、独自のプロパティとメソッドを定義したりできます。
// TypeScript での継承の例を次に示します。
class Animal {
    name: string;

    constructor(name: string) {
        this.name = name;
    }

    makeSound() {
        console.log("Animal makes a sound");
    }
}
class Dog extends Animal {
    breed: string;

    constructor(name: string, breed: string) {
        super(name);
        this.breed = breed;
    }

    makeSound() {
        console.log("Dog barks");
    }

    fetch() {
        console.log("Dog fetches the ball");
    }
}
const barks = new Dog("Buddy", "Labrador");
barks.makeSound(); // Output: Dog barks
barks.fetch(); // Output: Dog fetches the ball
console.log(barks.name); // Output: Buddy
console.log(barks.breed); // Output: Labrador
```