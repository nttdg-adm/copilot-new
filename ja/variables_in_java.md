---
title: "Javaでのさまざまな種類の変数の例（GitHub Copilotを使用）"
description: "GitHub Copilotを使用したシンプルなコード補完"
category: general
platforms: [copilot, copilot-chat]
level: lv3
---

## Javaでのさまざまな種類の変数の例（GitHub Copilotを使用）

[<img src="https://img.shields.io/badge/Lv3-Mature_Best_Practice-brightgreen">](https://github.com/orgs/AI-Native-Development/projects/1/)

### 説明
Javaには主に3種類の変数があります。
- ローカル変数
- スタティック変数
- インスタンス変数

GitHub Copilotは、クラス名に基づいてコメントを生成することができます。Javaでさまざまな種類の変数を示すクラスを作成し、`変数の例`という名前を付けると、GitHub Copilotは '//このクラスは変数の使用法を示すために使用されます' というコメントを提案します。

また、GitHub Copilotは、明確な指示を含むコメントを書くと正確な提案を行います。ローカル変数やスタティック変数の例を作成するための指示をコメントで与えると、必要なすべての例を作成してくれます。

#### 例

##### 入力コード
```java
public class VariableExample { 
    // 静的変数とローカル変数を作成して表示する
}
```

##### Copilotによる提案結果

```java
// このクラスは変数の使用例を示すために使用されます
public class VariableExample {
// 静的変数とローカル変数を作成して表示する
    static int staticVariable = 10;
    int localVariable = 20;
    public static void main(String[] args) {
        System.out.println("静的変数: " + staticVariable);
        VariableExample obj = new VariableExample();
        System.out.println("ローカル変数: " + obj.localVariable);
    }
    
}
```