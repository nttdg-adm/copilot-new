---
title: "GitHub Copilotを使用したJavaでの異なるコレクション"
description: "GitHub Copilotを使用したHashSetとTreeSetの実装"
category: general
platforms: [copilot, copilot-chat]
level: lv3
---

## GitHub Copilotを使用したJavaでのHashSet、TreeSetコレクションの実装
[<img src="https://img.shields.io/badge/Lv3-Mature_Best_Practice-brightgreen">](https://github.com/orgs/AI-Native-Development/projects/1/)

### 説明
コレクションは、オブジェクトの単一の単位、つまりグループを表します。
Javaのコレクションフレームワークは、多くのインターフェースとクラスを提供しています。`java.util`パッケージには、コレクションフレームワークのすべてのクラスとインターフェースが含まれています。

    Iterable
        ├── Collection
                ├── Set
                │   ├── AbstrachSet
                │   │   ├── HashSet
                │   ├── SortedSet
                    │   ├── TreeSet

上記の階層図では、Iterable、Collection、Set、SortedSetはインターフェースであり、AbstrachSet、HashSet、TreeSetはクラスです。
ListとSetには違いがあります。リストは重複した要素を含むことができますが、Setはユニークな要素のみを含みます。
Setインターフェースを実装するクラスは以下のとおりです。
- HashSet
    #### 説明:
    JavaのHashSetクラスは、ハッシュテーブルを使用してコレクションを作成するために使用されます。AbstractSetクラスを継承し、Setインターフェースを実装しています。
    GitHub Copilotを使用すると、HashSetオブジェクトを作成することができます。HashSetはユニークな要素のみを含みます。
    `//Integer オブジェクトを格納する HashSet オブジェクトを作成する`という指示を与えると、正しい提案が表示されます。また、GitHub CopilotはHashSetのメソッドを使用して行うことができる操作についても提案を行います。
    重複したオブジェクトを追加しようとしても、HashSetは変更されません。これはGitHub Copilotを使用して示すことができます。

    #### 例
    - **演習1**
        ##### 入力コード
        ```java
        import java.util.HashSet;

        public class HashSetExample {
            public static void main(String[] args) {
                // Integerオブジェクトを格納するHashSetオブジェクトを作成する
            }
        }
        ```
        
        ##### Copilotによる提案結果

        ```java
        import java.util.HashSet;

        public class HashSetExample {
            public static void main(String[] args) {
                // Integerオブジェクトを格納するHashSetオブジェクトを作成する
                HashSet<Integer> numbers = new HashSet<Integer>();
                // セットに要素を追加する
                numbers.add(4);
                numbers.add(7);
                numbers.add(8);
                // セットを出力する
                System.out.println(numbers);
                
            }
        }
        ```

    - **演習2**
        ##### 入力コード
        ```java
        import java.util.HashSet;

        public class HashSetExample {
            public static void main(String[] args) {
                // Integerオブジェクトを格納するHashSetオブジェクトを作成する
                HashSet<Integer> numbers = new HashSet<Integer>();
                // セットに要素を追加する
                numbers.add(4);
                numbers.add(7);
                numbers.add(8);
                // セットを出力する
                System.out.println(numbers);
                // セットに既に存在する要素を追加する
            }
        }
        ```
        
        ##### Copilotによる提案結果

        ```java
        import java.util.HashSet;

        public class HashSetExample {
            public static void main(String[] args) {
                // Integerオブジェクトを格納するHashSetオブジェクトを作成する
                HashSet<Integer> numbers = new HashSet<Integer>();
                // セットに要素を追加する
                numbers.add(4);
                numbers.add(7);
                numbers.add(8);
                // セットを出力する
                System.out.println(numbers);
                // セットに既に存在する要素を追加する
                numbers.add(4);
                // セットを出力する
                System.out.println(numbers);
                // セットから要素を削除する
                numbers.remove(7);
                // セットを出力する
                System.out.println(numbers);
                // セットのサイズを出力する
                System.out.println(numbers.size());
            }
        }
        ```

- TreeSet
    #### 説明: 
    JavaのTreeSetクラスは、木構造を使用して要素を格納するSetインターフェースを実装します。TreeSetクラスはAbstractSetクラスを継承し、NavigableSetインターフェースを実装しています。TreeSetクラスのオブジェクトは昇順で格納されます。
    GitHub Copilotを使用すると、TreeSetオブジェクトを作成できます。TreeSetは重複する要素を含みません。
    `//Create a TreeSet object that stores Double objects`という指示を与えると、正しい提案が得られます。また、GitHub CopilotはHashSetのメソッドを使用して実行できる操作についても提案を行います。

    #### 例
    - **演習1**
        ##### 入力コード
        ```java
        import java.util.TreeSet;

        public class TreeSetExample {
            public static void main(String[] args) {
                // Doubleオブジェクトを格納するTreeSetオブジェクトを作成する
            }
        }
        ```
        
        ##### Copilotによる提案結果

        ```java
        import java.util.TreeSet;

        public class TreeSetExample {
            public static void main(String[] args) {
                // Doubleオブジェクトを格納するTreeSetオブジェクトを作成する
                TreeSet<Double> decimals = new TreeSet<Double>();
                // セットに要素を追加する
                decimals.add(4.0);
                decimals.add(7.0);
                decimals.add(8.0);
                // セットを出力する
                System.out.println(decimals);
            }
        }
        ```

    - **演習1**
        ##### 入力コード
        ```java
        import java.util.TreeSet;

        public class TreeSetExample {
            public static void main(String[] args) {
                // Doubleオブジェクトを格納するTreeSetオブジェクトを作成する
                TreeSet<Double> decimals = new TreeSet<Double>();
                // セットに要素を追加する
                decimals.add(4.0);
                decimals.add(7.0);
                decimals.add(8.0);
                // セットを出力する
                System.out.println(decimals);
                // セットに既に存在する要素を追加する
            }
        }
        ```
        
        ##### Copilotによる提案結果

        ```java
        import java.util.TreeSet;

        public class TreeSetExample {
            public static void main(String[] args) {
                // Doubleオブジェクトを格納するTreeSetオブジェクトを作成する
                TreeSet<Double> decimals = new TreeSet<Double>();
                // セットに要素を追加する
                decimals.add(4.0);
                decimals.add(7.0);
                decimals.add(8.0);
                // セットを出力する
                System.out.println(decimals);
                // セットに既に存在する要素を追加する
                decimals.add(4.0);
                // セットを出力する
                System.out.println(decimals);
                // セットから要素を削除する
                decimals.remove(7.0);
                // セットを出力する
                System.out.println(decimals);
                // セットのサイズを出力する
                System.out.println(decimals.size());
            }
        }
        ```

