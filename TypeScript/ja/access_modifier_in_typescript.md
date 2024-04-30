---
title: "TypeScriptにおけるアクセス修飾子"
description: "TypeScriptにおけるアクセス修飾子"
category: general
platforms: [copilot, copilot-chat]
level: lv3
---

## TypeScriptにおけるアクセス修飾子
[<img src="https://img.shields.io/badge/Lv3-Mature_Best_Practice-brightgreen">](https://github.com/orgs/AI-Native-Development/projects/1/)

### 説明
TypeScriptでは、他のプログラミング言語と同様に、クラスレベルでアクセス修飾子を使用することができます。アクセス修飾子により、クラスメンバーにアクセスできます。アクセス修飾子は、クラスメンバーのセキュリティを高め、無効な使用を防止します。データの隠蔽またはカプセル化は、クラスの機能であり、他のクラスのメンバーに対してデータメンバーの可視性を制御することができます。アクセス修飾子を使用してカプセル化の概念を実装することができます。アクセス修飾子は、定義されたクラスの外部からクラスのデータメンバーの可視性を定義します。

TypeScriptでサポートされているアクセス修飾子は次のとおりです-
1. public: パブリック データ メンバーにはユニバーサル アクセシビリティがあります。クラス内のデータ メンバーは、デフォルトではパブリックです。
2. private: プライベート データ メンバーは、これらのメンバーを定義するクラス内でのみアクセスできます。外部クラスのメンバーがプライベート メンバーにアクセスしようとすると、コンパイラはエラーをスローします。
3. protected: 保護されたデータ メンバーは、前者と同じクラス内のメンバーだけでなく、子クラスのメンバーからもアクセスできます。

GitHub Copilot を使用すると、Access 修飾子とその使用法について学ぶことができます。
GitHub Copilot に「Ctrl + I」をクリックして「Typescript の Access 修飾子とは何ですか」と尋ねると、例を挙げて説明してくれます。
＃＃＃ 例

##### 入力コード
```TypeScript
//Typescript のアクセス修飾子とは何ですか
```

##### 副操縦士によって提案された結果
```TypeScript
// Typescript のアクセス修飾子とは何ですか
class MyClass {
    public publicProperty: string;
    private privateProperty: number;
    protected protectedProperty: boolean;

    constructor() {
        this.publicProperty = "Public Property";
        this.privateProperty = 123;
        this.protectedProperty = true;
    }

    public publicMethod() {
        console.log("This is a public method.");
    }

    private privateMethod() {
        console.log("This is a private method.");
    }

    protected protectedMethod() {
        console.log("This is a protected method.");
    }
}

const myObject = new MyClass();
console.log(myObject.publicProperty); // アクセシビリティ対応
// console.log(myObject.privateProperty); // アクセスできない
// console.log(myObject.protectedProperty); // アクセスできない
myObject.publicMethod(); // アクセシビリティ対応
// myObject.privateMethod(); // アクセスできない
// myObject.protectedMethod(); // アクセスできない
```