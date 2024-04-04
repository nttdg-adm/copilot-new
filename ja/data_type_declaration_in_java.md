---
title: "GitHub Copilotを使用したJavaのさまざまなデータ型の例"
description: "GitHub Copilotを使用したシンプルなコード補完"
category: general
platforms: [copilot, copilot-chat]
level: lv3
---

## GitHub Copilotを使用したJavaのさまざまなデータ型の例
[<img src="https://img.shields.io/badge/Lv3-Mature_Best_Practice-brightgreen">](https://github.com/orgs/AI-Native-Development/projects/1/)

### 説明
Javaでは、データ型は2つのグループに分けられます：
- プリミティブデータ型 - byte、short、int、long、float、double、boolean、charを含みます
- ノンプリミティブデータ型 - String、配列、クラスなどがあります

プリミティブデータ型は、変数の値のサイズと型を指定します。
GitHub Copilotを使用してJavaでデータ型を宣言する方法を学ぶことができます。単に「Javaでのデータ型の例を示す」というコメントを書くだけで、すべてのデータ型が生成され、それぞれのグループの上に「//primitive data types」と「//Non-Primitive Data Types」というコメントが追加されます。
プリミティブデータ型はサイズを指定します。intデータ型の宣言の上に「size of」というコメントを書き始めると、「//size of int = 4 bytes」という正確な提案が表示され、各プリミティブデータ型のサイズについての提案が続きます。

#### 例
- **演習1**
##### 入力コード
```java
    public class DataTypeExample {

        public static void main(String[] args) {
           // Javaにおけるデータ型の例を示します
        }
    }
```

##### Copilotによる提案結果

```java
    public class DataTypeExample {
    public static void main(String[] args) {
       
        // Javaにおけるデータ型の例を示します
        // プリミティブデータ型
        int a = 10;

        float b = 10.5f;

        double c = 10.5;
        
        char d = 'A';
        
        boolean e = true;
        
        long f = 1000000000000000000L;
        
        short g = 12345;
        
        byte h = 123;
        // ノンプリミティブデータ型
        // String
        String i = "Hello World";
        // 配列
        int[] j = {1,2,3,4,5};
    }
    }
```

- **演習2**
##### 入力コード
```java
    public class DataTypeExample {

        public static void main(String[] args) {
        // Javaにおけるデータ型の例を示します
        // intのサイズ
        int a = 10;
        
        float b = 10.5f;
        
        double c = 10.5;
        
        char d = 'A';
        
        boolean e = true;
        
        long f = 1000000000000000000L;
        
        short g = 12345;
        
        byte h = 123;
        // ノンプリミティブデータ型
        // String
        String i = "Hello World";
        // 配列
        int[] j = {1,2,3,4,5};
        }
    }
```

##### Copilotによる提案結果

```java
    public class DataTypeExample {
    public static void main(String[] args) {
       
    
        // Javaにおけるデータ型の例を示します
        // プリミティブデータ型
        // intのサイズ = 4バイト
        int a = 10;
        // floatのサイズ = 4バイト
        float b = 10.5f;
        // doubleのサイズ = 8バイト
        double c = 10.5;
        // charのサイズ = 2バイト
        char d = 'A';
        // booleanのサイズ = 1バイト
        boolean e = true;
        // longのサイズ = 8バイト
        long f = 1000000000000000000L;
        // shortのサイズ = 2バイト
        short g = 12345;
        // byteのサイズ = 1バイト
        byte h = 123;
        // ノンプリミティブデータ型
        // String
        String i = "Hello World";
        // 配列
        int[] j = {1,2,3,4,5};
    }
    }
```