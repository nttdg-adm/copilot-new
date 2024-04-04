---
title: "GitHub Copilotを使用したJavaにおける関数型プログラミング"
description: "GitHub Copilotを使用したJavaにおける関数型プログラミング"
category: general
platforms: [copilot, copilot-chat]
level: lv3
---

## GitHub Copilotを使用したJavaにおける関数型プログラミングの実装
[<img src="https://img.shields.io/badge/Lv3-Mature_Best_Practice-brightgreen">](https://github.com/orgs/AI-Native-Development/projects/1/)

### 説明
関数型プログラミング（FP）は、プログラミングのパラダイムです。副作用を持たず、常に同じ入力に対して同じ出力を返す純粋な関数の使用を重視します。計算を数学的な関数の評価として扱い、状態の変更や可変のテーブルを避けます。
基本的に、関数型プログラミングは、計算を数学的な関数の評価として扱うコンピュータプログラムの書き方のスタイルです。
数学では、関数は入力集合と出力集合を関連付ける式です。
重要なことは、関数の出力は入力にのみ依存するということです。さらに興味深いことに、2つ以上の関数を組み合わせて新しい関数を作成することができます。
関数型プログラミングの多くの機能は、常にJavaの一部ではありませんでした。効果的に関数型プログラミングを実践するためには、Java 8以降を使用することをお勧めします。

GitHub Copilotを使用することで、Javaにおける関数型プログラミングについて学ぶことができます。
GitHub CopilotのLambda式など、関数型プログラミングのさまざまな機能を探索することができます。

ラムダ式を使用してリスト内の偶数を出力する関数を作成します というコメントを追加すると、GitHub Copilotが完璧な提案をしてくれます。したがって、ラムダ式を使用しても出力に変化がないことを確認できます。

#### 例
- **演習1**
##### 入力コード
```java
import java.util.Arrays;
import java.util.List;
/**
 * Javaにおける関数型プログラミング
 */
public class Functional_Programming_in_Java {

    public static void main(String[] args) {
    //整数のリストを作成する
    List<Integer> list = Arrays.asList(1,2,3,4,5,6,7,8,9,10);
    //ラムダ式を使用して偶数を出力する関数を呼び出す
    printEven(list);
    //ラムダ式を使用せずに偶数を出力する関数を呼び出す
    printEvenWithoutLambda(list);

        
    }
    //ラムダ式を使用してリスト内の偶数を出力する関数を作成する
   
}
```

##### Copilotによる提案結果
```java
import java.util.Arrays;
import java.util.List;
/**
 * Javaにおける関数型プログラミング
 */
public class Functional_Programming_in_Java {

    public static void main(String[] args) {
    //整数のリストを作成する
    List<Integer> list = Arrays.asList(1,2,3,4,5,6,7,8,9,10);
    //ラムダ式を使用して偶数を出力する関数を呼び出す
    printEven(list);
    //ラムダ式を使用せずに偶数を出力する関数を呼び出す
    printEvenWithoutLambda(list);

        
    }
    //ラムダ式を使用してリスト内の偶数を出力する関数を作成する
    public static void printEven(List<Integer> list){
        list.stream().filter(i -> i%2 == 0).forEach(System.out::println);
    }
    
    //単純なforループを使用してリスト内の偶数を出力する関数を作成する
    public static void printEvenWithoutLambda(List<Integer> list){
        for (int i : list) {
            if(i%2 == 0){
                System.out.println(i);
            }
        }
    }
}
```

- **演習2**
##### 入力コード
```java
/**
 * 関数の例
 */
public class FunctionExample {

    public static void main(String[] args) {
        // 文字列を受け取り、その長さを返す関数を作成する

    }
}
```

##### Copilotによる提案結果
```java
/**
 * FunctionExample
 */
public class FunctionExample {

    public static void main(String[] args) {
        // 文字列を受け取り、その長さを返す関数を作成する
        Function<String, Integer> function = s -> s.length();
        // 関数を呼び出す
        System.out.println(function.apply("Hello World"));

    }
}
```